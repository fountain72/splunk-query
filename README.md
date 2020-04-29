# splunk-query

splunkQ --help
usage: splunkQ [-h] [-u USER] [-s SERVER] -q QUERYCMD [-e EARLIEST] [-l LATEST]
 
        This script will help you query all different splunk servers to fetch what you need.
 
        Type -h or --help for a full list of available options.
 
        Alex Lu 03/18/2020 version 1.0
 
        Alex Lu 03/31/2020 version 1.1
 
        Alex Lu 04/20/2020 version 1.2
 
        Alex Lu 04/28/2020 version 1.3
 
        Server has four options:
 
Please edit the code to add your splunk servers.
 
optional arguments:
  -h, --help            show this help message and exit
  -u USER, --user USER  Username to run the script against.  This must be a valid NTID username
  -s SERVER, --server SERVER
                        Specify a Splunk Server to query
  -q QUERYCMD, --querycommand QUERYCMD
                        Specify a query command to use
  -e EARLIEST, --earliest EARLIEST
                        Specify earliest start
  -l LATEST, --latest LATEST
                        Specify latest
                        
+ Adding default user with service account “t2cmsplunk”. But you still can use your NT login, when you use “ -u “ option.
+ Adding earliest and latest option. These are optional, not mandatory.

###Example
 
####-e-5m@m -l now  
this will add “earliest=-5m@m latest=now” into your query command if your original command doesn’t include the timeframe.
Please note: if you give “-“ please leave no space with option “-e” or “-l”
                       “+” is fine.

####-e 04/28/2020:23:00:00 -l 04/28/2020:23:00:01
This will add “earliest=04/28/2020:23:00:00 latest=04/28/2020:23:00:01” into your query command

 
