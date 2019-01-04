# iOS-Mobile-Installation-Logs-Parser 



Script parses all the logs in the /private/var/installd/Library/Logs/MobileInstalation/*.log*

Script will produce a currently installed apps report, a uninstalled apps reports and historical  
reports for both types per app. 

The types of rows extracted from the logs are for installed apps,  
moved containers, made live containers and destroyed containers.

Usage:  
1) Put the script in the same directory as the mobile_installation.log.* files.
2) Run the script.  
3) Script will produce a SQLite database named mib.db.
4) Script will produce two directories named Apps_Historical and Apps_State.
Apps_Historical contains text files per app with coresponding app entries.

In order to run the script again the script generated directories and SQLite db file need  
to be deleted or moved out of the running directory.  
