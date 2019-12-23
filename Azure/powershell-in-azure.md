# Powershell in Azure


## Installation for Windows
Two modules: AzureRm (old) and Az module (new, 2019)  

For windows
```powershell
Install-Module -Name Az -AllowClobber -Scope CurrentUser -Force

#check if AZ module is installed
Get-InstalledModule -Name Az -AllVersions

```

## Installation for Mac

With Mac 10.12 or higher, use [PowerShellCore on macOS](https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-core-on-macos?view=powershell-6)  
```bash
# using homebrew
brew cask install powershell

# to verify
pwsh
```

Now in poweshell, check the powershell version table:  
```powershell
$PSVersionTable

# powershell output -->
PS /Users/anhkimhoang/Documents/GitHub/cloud-engineer-lab> $PSVersionTable

Name                           Value
----                           -----
PSVersion                      6.2.3
PSEdition                      Core
GitCommitId                    6.2.3
OS                             Darwin 18.7.0 Darwin Kernel Version 18.7.0: Tue Aug 20 16:57:14 PDT 2019; root:xnu-4903.271.2~…
Platform                       Unix
PSCompatibleVersions           {1.0, 2.0, 3.0, 4.0…}
PSRemotingProtocolVersion      2.3
SerializationVersion           1.1.0.1
WSManStackVersion              3.0

# run the same command to download as you would, the -Force will force update to the latest version
Install-Module -Name Az -AllowClobber -Scope CurrentUser -Force
```

Misc commands, for future maitenance and uninstallation  
```bash
# to update
brew update
brew cask update powershell

# to uninstall 
brew cask uninstall powershell
```

## Logging into to Azure from Powershell  
```powershell
Connect-AzAccount
``` 

## Create a VM in PowerShell
```powershell
# AZ module command is much easier to create a VM

# First create a resourcegroup
New-AzResourceGroup -Name testWebRG -Location EastUS

# New create a new VM
New-AzVM -ResourceGroupName "testWebRG" -Name "testNewVm" -Location "EastUS" -VirtualNetworkName "newTestVirtualNetwork" -SubnetName "default" -SecurityGroupName "newNSG" -PublicIpAddressName "mytestwebserver" -OpenPorts 80, 443, 3389

# powershell output --->
```

## Start and Stop a VM in PowerShell
```powershell
# to stop a vm
Stop-AzVM -ResourceGroupName "testWebRG" -Name "testNewVm"

# to start a vm
Start-AzVM -ResourceGroupName "testWebRG" -Name "testNewVm"
```
