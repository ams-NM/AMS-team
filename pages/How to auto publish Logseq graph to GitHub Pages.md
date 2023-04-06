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
	- [[GitHub]] Action script:
		- ```yml
		  ```