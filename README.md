# Anders.Gaming.LibTech3
[hannes's](http://www.crossfire.nu/user/view/id/6710) modified [Tech3 Demo API - 0.1](http://www.crossfire.nu/news/4632/tech3-demo-api-01)

used by [Wolfenstein: Enemy Territory demo tools](http://178.62.235.156:5111/)

# Download

[binaries](https://github.com/mittermichal/Anders.Gaming.LibTech3/releases)

# Changelog
- 0.1.1
  - cut ettv demo (*.tv_84) with selected player's POV.
  - cut from command-line arguments
  - detection of duplicate bullet events from ETTV demos

# Usage

##cut
cuts demo

Anders.Gaming.LibTech3 cut demo_path output_path start end cut_type (client_num)

where cut_type values are:
- SNAPNUMBER = 0
- SNAPTIME = 1 - most useful
-	SNAPCOUNT = 2

client_num is ignored if it's POV demo 

example:
Anders.Gaming.LibTech3.exe demo01-10-31.tv_84 demo01-10-31.dm_84 56621000 56632000 1 0

##indexer
parses demo

Anders.Gaming.LibTech3 indexer options

where options are:

	exportBulletEvents = 0
	exportPlayers = 1
	exportDemo = 0
	exportObituaries = 1
	exportChatMessages = 0
	exportJson = 1
	exportSQL = 0
	exportJsonFile = stdout
	exportSQLFile = out.db
	logFile = stdout
	exportPaths = 0

	indexType = demo
	indexTarget

example:

Anders.Gaming.LibTech3.exe indexer indexTarget/demo.dm_84/exportJsonFile/out.json/exportBulletEvents/1
