# Configure-or-Customize-Horizon-CS-Logs-with-registry.-Enables-io.netty-logging-on-Connection-Server

This script helps in eliminating manual efforts in updating each of the CS with customized logging. 

Please feel free to set a different allowed decimal values for following registry. Name is self explanatory. 

REG ADD "HKEY_LOCAL_MACHINE\SOFTWARE\VMware, Inc.\VMware VDM\Log" /t REG_DWORD /f /v "MaxDaysKept" /d 10 
REG ADD "HKEY_LOCAL_MACHINE\SOFTWARE\VMware, Inc.\VMware VDM\Log" /t REG_DWORD /f /v "MaxDebugLogs" /d 20 
REG ADD "HKEY_LOCAL_MACHINE\SOFTWARE\VMware, Inc.\VMware VDM\Log" /t REG_DWORD /f /v "MaxDebugLogSizeMB" /d 100

log_scripts folder has log4j2.xml and log4j.default which gets replaced. 

Feel free to customize it based on the needs of your horizon environment to enable collection of more useful data required for troubleshooting.

IT is strongly recommended to test this with non production environment, prior to applying it in production.
