# Powershell in Azure

Two modules: AzureRm (old) and Az module (new, 2019)  

For windows
```powershell
Install-Module -Name Az -AllowClobber -Scope CurrentUser -Force

#check if AZ module is installed
Get-InstalledModule -Name Az -AllVersions

```


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

# myoutput
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
```

Misc commands, for future maitenance and uninstallation  
```bash
# to update
brew update
brew cask update powershell

# to uninstall 
brew cask uninstall powershell
```
