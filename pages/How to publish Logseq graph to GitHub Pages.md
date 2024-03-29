-
- ## A github action and CLI to publish logseq graphs as a SPA app - [[2023-04-20 Thu]]
	- Ref: https://github.com/logseq/publish-spa
	- ==publish.yml==
		- ```yml
		  name: Publish-scheduled
		  
		  # Controls when the workflow will run
		  on:
		    schedule:
		      - cron: '10 */1 * * *'
		  
		    # Allows you to run this workflow manually from the Actions tab
		    workflow_dispatch:
		  
		  permissions:
		    contents: write
		  jobs:
		    test:
		      if: ${{ vars.LAST_COMMIT != github.GITHUB_SHA }}
		      runs-on: ubuntu-latest
		      name: Publish Logseq graph
		      # Steps represent a sequence of tasks that will be executed as part of the job
		      steps:
		        - uses: actions/checkout@v3
		        - uses: logseq/publish-spa@v0.1.0
		        - name: add a nojekyll file # to make sure asset paths are correctly identified
		          run: touch $GITHUB_WORKSPACE/www/.nojekyll
		        - name: Deploy 🚀
		          uses: JamesIves/github-pages-deploy-action@v4
		          with:
		            folder: www
		  ```
	-  Backup files were exported
		- `Problem`
			- Contents in backup folders show up in queries on the published pages.
		- ==Solution==
			- Add backup folders to `.gitignore`
			- ```
			  logseq/bak/
			  logseq/.recycle/
			  ```
- ## Use Logseq built-in `Export graph`
	- Ref: https://github.com/pengx17/logseq-publish
	- Full content of [[GitHub]] Action script: `.github/workflows/deploy.yml`
		- ```yml
		  # This is a basic workflow to help you get started with Actions
		  
		  name: CI
		  
		  # Controls when the workflow will run
		  on:
		    push:
		      branches: [main]
		  
		    # Allows you to run this workflow manually from the Actions tab
		    workflow_dispatch:
		  
		  # A workflow run is made up of one or more jobs that can run sequentially or in parallel
		  jobs:
		    # This workflow contains a single job called "build"
		    build:
		      # The type of runner that the job will run on
		      runs-on: ubuntu-latest
		  
		      # Steps represent a sequence of tasks that will be executed as part of the job
		      steps:
		        # Checks-out your repository under $GITHUB_WORKSPACE, so your job can access it
		        - uses: actions/checkout@v3
		        - name: Logseq Publish 🚩
		          uses: pengx17/logseq-publish@main
		        - name: add a nojekyll file
		          run: touch $GITHUB_WORKSPACE/www/.nojekyll
		        - name: Deploy 🚀
		          uses: JamesIves/github-pages-deploy-action@v4
		          with:
		            branch: gh-pages # The branch the action should deploy to.
		            folder: www # The folder the action should deploy.
		            clean: true
		            single-commit: true
		  
		  ```
	- But the published site does not look like a real website, but an online version of [[Logseq]].
- ## Publish with Hugo
	- Ref: https://github.com/briansunter/graph/blob/master/.github/workflows/aws-deploy.yml
	- Ref: https://github.com/peaceiris/actions-hugo
	-
	- [[GitHub]] Action script:
		- ```yml
		  # This is a basic workflow to help you get started with Actions
		  
		  name: CI
		  
		  # Controls when the workflow will run
		  on:
		    push:
		      branches: [main]
		  
		    # Allows you to run this workflow manually from the Actions tab
		    workflow_dispatch:
		  
		  # A workflow run is made up of one or more jobs that can run sequentially or in parallel
		  jobs:
		    # This workflow contains a single job called "build"
		    build:
		      # The type of runner that the job will run on
		      runs-on: ubuntu-latest
		  
		      # Steps represent a sequence of tasks that will be executed as part of the job
		      steps:
		        # Checks-out your repository under $GITHUB_WORKSPACE, so your job can access it
		        - uses: actions/checkout@v3
		          with:
		            submodules: true  # Fetch Hugo themes (true OR recursive)
		            fetch-depth: 0    # Fetch all history for .GitInfo and .Lastmod
		        - name: Setup Hugo
		          uses: peaceiris/actions-hugo@v2
		          with:
		            hugo-version: '0.110.0'
		            extended: true
		        - name: Build
		          run: hugo --minify
		        - name: Logseq Publish 🚩
		          uses: pengx17/logseq-publish@main
		        - name: add a nojekyll file
		          run: touch $GITHUB_WORKSPACE/www/.nojekyll
		        - name: Deploy 🚀
		          uses: JamesIves/github-pages-deploy-action@v4
		          with:
		            branch: gh-pages # The branch the action should deploy to.
		            folder: www # The folder the action should deploy.
		            clean: true
		            single-commit: true
		  
		  ```