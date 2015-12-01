#ReadMe
##AD PowerShell User Creator
I have taken this script originally from 
https://gallery.technet.microsoft.com/scriptcenter/New-User-Creation-tool-14fa73cd.
This script was originally written by Rich Prescott (https://social.technet.microsoft.com/profile/rich%20prescott/) 
Then there were several modifications made, so we can add unix attributes such as UID and GID when we are creating this user. 

##Installing Identity Management for Windows Server 2012

To install or remove Identity Management for UNIX by using Dism.exe
On a domain controller that runs Windows Server 2012 R2 or Windows Server 2012, Right-click Windows PowerShell and click Run as Administrator .

Type one of the following, and then press ENTER:

To install the administration tools for Identity Management for UNIX

```powershell
Dism.exe /online /enable-feature /featurename:adminui /all
```

Dism.exe /online /disable-feature /featurename:adminui to remove the administration tools for Identity Management for UNIX.

noteNote
This installs or removes only the administration tools. Using Dism.exe, Server for NIS and Password Synchronization must be installed separately.

```shell
Dism.exe /online /enable-feature /featurename:nis /all to install Server for NIS.
Dism.exe /online /disable-feature /featurename:nis to remove Server for NIS.
Dism.exe /online /enable-feature /featurename:psync /all to install Password Synchronization.
Dism.exe /online /disable-feature /featurename:psync to remove Password Synchronization.
```

A restart of the computer is required when you install or remove Identity Management for UNIX. The /quiet parameter restarts the computer automatically after installation or removal is finished.
