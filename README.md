# Scripts to uninstall and reinstall Microsoft Store
I create scripts uninstall and reinstall  Microsoft Store to make MS store minimalistic and remove all unwanted MS apps, and only install the apps that I need.
# How it is work?
- Simply open Powershell as admin
- To uninstall MS Store, Copy paste the following:

```
Get-AppXPackage | Remove-AppxPackage
```

Repeate it for more than one time to remove MS store

- Copy/Paste the following to reinstall minimalistic MS Store:

```
Get-AppxPackage -allusers Microsoft.WindowsStore | Foreach {Add-AppxPackage -DisableDevelopmentMode -Register "$($_.InstallLocation)\AppXManifest.xml"}
```
