# Suspicious PowerShell commands

<ins>**-EncodedCommand / -enc**</ins> - Execute Base64 encoded PowerShell commands  
**Detect** - PowerShell logs (4104), long Base64 strings, suspicious parent process  

<ins>**IEX (Invoke-Expression)**</ins> - Execute string as code  
**Detect** - Script block logging (4104), IEX with web requests or encoded data  

<ins>**Invoke-WebRequest (iwr)**</ins> - Download data from internet  
**Detect** - Network logs, PowerShell 4104, connections to suspicious domains  

<ins>**DownloadString (WebClient)**</ins> - Fetch and execute remote script  
**Detect** - 4104 with DownloadString + IEX chain, outbound connections  

<ins>**Start-BitsTransfer**</ins> - Download files via BITS service  
**Detect** - BITS logs, unusual jobs, downloads from external sources  

<ins>**Set-ExecutionPolicy Bypass**</ins> - Disable script execution restrictions  
**Detect** - 4104 logs, execution policy changes, suspicious scripts  

<ins>**Set-MpPreference**</ins> - Modify Windows Defender settings  
**Detect** - Event logs (5007), Defender config changes  

<ins>**Add-MpPreference -ExclusionPath**</ins> - Add antivirus exclusion path  
**Detect** - Event logs (5007), new exclusions added  

<ins>**net user**</ins> - Manage Windows user accounts  
**Detect** - Security logs (4720–4726), account changes  

<ins>**net localgroup**</ins> - Manage groups and user privileges  
**Detect** - Security logs (4728, 4732), group membership changes  

<ins>**New-LocalUser**</ins> - Create local user account  
**Detect** - Event ID 4720, unusual account creation  

<ins>**Add-LocalGroupMember**</ins> - Add user to local group  
**Detect** - Event IDs 4728, 4732, privilege escalation patterns  

<ins>**Start-Process -WindowStyle Hidden**</ins> - Run process in hidden window  
**Detect** - Process creation (4688), hidden window flags, suspicious parent  

<ins>**powershell -w hidden -nop -noni**</ins> - Hidden PowerShell execution flags  
**Detect** - 4688 + command line flags, no profile usage  

<ins>**rundll32**</ins> - Execute code via DLL functions  
**Detect** - 4688, unusual DLL paths, suspicious command line  

<ins>**mshta http://...**</ins> - Execute remote script via HTA  
**Detect** - 4688, outbound HTTP, mshta spawning child processes