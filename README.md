Note: This parser has been deprecated in favor of iLEAPP.
Donwload iLEAPP in order to support the mobile installation logs artifact.

# iOS-Mobile-Installation-Logs-Parser 

![alt text](/images/mib_done.PNG "Usage example")

Script parses all the logs in the /private/var/installd/Library/Logs/MobileInstalation/*.log*

Script will produce a currently installed apps report, a uninstalled apps report and historical  
reports for both types per app. 

The types of rows extracted from the logs are for installed apps,  
moved containers, made live containers and destroyed containers.

Usage:  
  
1) Python 3.6.4 or newer.
2) Put the script in the same directory as the extracted mobile_installation.log.* files.
3) Run the script.  
4) Script will produce a SQLite database named mib.db.
5) Script will produce two directories named Apps_Historical and Apps_State. Apps_Historical contains text files per app with coresponding app entries. App_State contains two text files, one for installed apps and another for uninstalled apps.

In order to run the script again the script generated directories and SQLite db files need to be deleted or moved out of the running directory.  

Update on 1/17/2019  
Added:  
- Uninstall identifier events  
- Attempting delta patch events with version numbers  
- System reboot events  

Update 11/30/2019  
Added:  
- GUI version. Requires pip install easygui
