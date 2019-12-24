#Analyze Resource Utilization and Consumption

Search and download Azure "Monitor" to monitor apps and infrastructure.  

## Performance Counters 

CPU, Memory, Disk, Network are the basic performance counters.  

## Create a Baseline for Resources  

Baseline is the idea of having each of your resources stored as a script in CLI or as an ARM template.  You can make changes in these script or template than directly modifying them on Azure.  You just need to redeploy the templates from Github.  

### Using Powershell VM Examples  

[Azure Virtual Machine PowerShell samples](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/powershell-samples)  

Powershell scripts are better for documenting your environment and for moving to another subscription, service and still run the script to redeploy your entire environment.  

Sample script for VM 
```powershell
# Variables for common values
$resourceGroup = "myResourceGroup"
$location = "eastus"
$vmName = "myVM"

# Create user object
$cred = Get-Credential -Message "Enter a username and password for the virtual machine."

# Create a resource group
New-AzResourceGroup -Name $resourceGroup -Location $location

# Create a virtual machine
New-AzVM `
  -ResourceGroupName $resourceGroup `
  -Name $vmName `
  -Location $location `
  -ImageName "Win2016Datacenter" `
  -VirtualNetworkName "myVnet" `
  -SubnetName "mySubnet" `
  -SecurityGroupName "myNetworkSecurityGroup" `
  -PublicIpAddressName "myPublicIp" `
  -Credential $cred `
  -OpenPorts 3389

```

## Using Alerts 

1. Go to the Resource Group >> Alerts.  
2. Create new alert rule and select resource to target.    
3. Set alert criteria. You can set it as web app stop and use SMS.  

## Create Metrics

## Create Action Groups  

- action groups can trigger Azure Function, webhook, sms, LogicApp, etc.
- can assign action groups to multiple alerts  

