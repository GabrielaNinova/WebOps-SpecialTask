# WebOps-SpecialTask

All Scripts to be added to folder "C:\Temp"

1.CreateLocation.ps1 - PowerShell script which creates "C:\inetpub\wwwroot" directory, if it does not exist.
-dummyfile.html file to be copied to "C:\Temp"

2.CopyFile.ps1 - PowerShell script which copies a dummy .html file from "C:\" to the created directory "C:\inetpub\wwwroot"
-Script should be run as administrator in Powershell using "Start-Process powershell -Verb runas -ArgumentList "-file C:\Temp\2.CopyFile.ps1"

3.IISWebsite.ps1 - PowerShell script which creates a basic IIS Website with just http binding 
-Script should be run as administrator in PowerShell using "Start-Process powershell -verb runas -ArgumentList "-file C:\Temp\3.IISWebsite.ps1"

-port 80 -protocol http are set as default using the script.
Another way to do it is using the command below:
New-WebBinding -Name "website" -IPAddress * -HostHeader localhost -Port 80 -Protocol http
