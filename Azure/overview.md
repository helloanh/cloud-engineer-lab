# Overview

```bash
# create container with predefined resource group with IIS server in windows docker image
az container create --resource-group WebResourcEGroup --name demo-iis --os-type Windows --image mcr.microsoft.com/windows/servercore/iis:nanoserver --dns-name-label demoiisanhtest --ports 80
```

## Azure Facts 
**Regions and Geos**  
- released in 2010    
- 54 regions around the world    
- most of any cloud provider   
- not all regions are available to all customers  

## Three different cloud:  
1. Public cloud
2. US government cloud (3)
3. German cloud
4. Other restricted regions

### Public Cloud  
- anyone with a credit card  
- about 28 regions    
- 6 have restrictions  
- minor differences between what is offered   
- data respects national boundaries ("geos"). all data stay in the specific country due to legal international laws  

### US Goverment Cloud
- 8 regions currently  
- only US govts - state, local, federal  
- completely separate network than Azure Public Cloud 
- versions for govt, defense, secret intelligence community  

### German Cloud
- 4 regions currently 
- Germany has strict data protection policies
- data trustee
- configuration differences with global Azure

### Private Cloud 
- Azure goverment 
- Azure stack
- internal or corporate cloud
- only avail to select people not the general public

- you can download your own Azure stack and use the commands on your own on-premise data center   

### Other clouds  
**Hybrid** - mix of on-premises (private) computing with cloud  
- primary data center on-premises, and backup ready to go in the cloud  
- extending your SQL server database using cloud storage  
- public websites in Azure connecting to private WCF services on-premises
- mix and match   


## Cloud Concepts: Availibility and Scaling
1. economy of scale
	- it's cheaper for MS to run the server than you going out to buy them yoruself  

	-cheaper (per server):      
		- hardware about 30% cost when buy in bulk  
		- electricity 15-20% cost of runnign a server    
		- labor costs   
		- utilization    

2. availability 
	- a target percentage of time that your application / service will be responding to requests without problems. 
	- same as "uptime" of the entire solution up to the internet boundary 
	- 90% avail - 2.4 hours day of downtime  
	- 99% avail - 14.4 mins per day of downtime  

	**high availability** 

	- intention of creating a syst that avoid downtime
	- thoguht, planning, more expensive
	- 99.9% (3 nines) - 1.45 mins per day  
	- 99.90% (4 nines) - 8.6 seconds per day  
	- 100% genera said to be not possible

	** challenges**
	- your app needs updating
	- malicious actors - DDoS and hacks
	- mistakes happen

3. scalability
	- the ability of a system to handle growth of users or work for users

## Cloud Concepts: Elasticity, Faults, and Recovery
1. elasticity 
	- the ability of a system to automatically grow and shrink based on application demand  
	- can grow and shrink - autoscaling based on user demand  

2. faults
	- hardware fails
	- power outages and storms
	- internet outages
	- bad deployments
	- security updates and patches

3. disaster recovery 
	Questions to ask for recovery
	- how long are your down time for? how long is acceptable 
	- how much data do you lose?  

	Capital Expenditure (CapEx)  - expense business incurs to create a benefit in the future   

	Operational expenditure (OpEx) - day to day cost to run a business. 






