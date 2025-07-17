- Performed on: [[2025-02-19 Wed]] NOTAM at 4:00 - 6:00 AM, `1st attempt`==Failed==
- `2nd attempt`, ==Failed==
- TODO Update AviMet 8 config, `3rd attempt`
  date:: [[2025-07-23 Wed]]
  remark:: was [[2025-06-16 Mon]], Postponed, SMG requirements not ready.
- ## Steps
	- 1.  先將CDUA和CDUB C:\Avimet\config文件夾整體拷貝到服務器硬盤其他路徑，用作更新前的備份記錄。
	- 2.  在CDUA上，運行C:\Avimet\config目錄下AW50StopAllSrv.bat批處理，停止掉所有服務。
	  3.  在CDUB上，運行C:\Avimet\config目錄下AW50StopAllSrv.bat批處理，停止掉所有服務。此時，Avimet8系統所有數據開始中斷，包括顯示界面，曆史數據存儲及對外輸出數據。
	- 4.  將需要更新的ini配置文件覆蓋拷貝到服務器CDUA和CDUB C:\Avimet\config路徑下。
	- 5.   在CDUA上，運行C:\Avimet目錄下AW50StartAllSrv.bat批處理，開始所有服務。
	- 6.   在CDUB上，運行C:\Avimet目錄下AW50StartAllSrv.bat批處理，開始所有服務。
	- 7.   此時，系統數據開始恢複。大約20分鍾後，自觀數據完全恢複。