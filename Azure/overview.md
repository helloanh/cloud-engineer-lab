# Overview

```bash

# create container with predefined resource group with IIS server in windows docker image

az container create --resource-group WebResourcEGroup --name demo-iis --os-type Windows --image mcr.microsoft.com/windows/servercore/iis:nanoserver --dns-name-label demoiisanhtest --ports 80
```

## Azure Facts  

### Regions and Geos  

- released in 2010    
- 54 regions around the world    
- most of any cloud provider   
- not all regions are available to all customers  

#### Three different cloud:  
1. Public cloud
2. US government cloud (3)
3. German cloud
4. Other restricted regions


#### Public Cloud  
- anyone with a credit card  
- about 28 regions    
- 6 have restrictions  
- minor differences between what is offered   
- data respects national boundaries ("geos"). all data stay in the specific country due to legal international laws  

#### US Goverment Cloud
- 8 regions currently  
- only US govts - state, local, federal  
- completely separate network than Azure Public Cloud 
- versions for govt, defense, secret intelligence community  

#### German Cloud
- 4 regions currently 
- Germany has strict data protection policies
- data trustee
- configuration differences with global Azure

#### Private Cloud 
- Azure goverment 
- Azure stack
- internal or corporate cloud
- only avail to select people not the general public

- you can download your own Azure stack and use the commands on your own on-premise data center   

#### Other clouds  

**Hybrid** - mix of on-premises (private) computing with cloud  
- primary data center on-premises, and backup ready to go in the cloud  
- extending your SQL server database using cloud storage  
- public websites in Azure connecting to private WCF services on-premises
- mix and match   


