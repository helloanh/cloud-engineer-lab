# Virtual Network


## Create a virtual network with subnets
1. Create new virtual network with one default subnet named frontend (public subnet).  For example: 190.0.0.0/16 as the virtual network.  190.0.0.0/23 for frontend subnet. 
2. Create another subnet -- call this one backend (private subnet).  190.0.2.0/23 for backend subnet.
3. Create a new public IP address and give it a dns label.  
4. Create a new route table and add a route that routes all backend private subnet traffic to "Virtual appliance" as the hop type (this will be the firewall) and give the IP of this virtual appliance/firewall.  Asumming you already have a firewall or just assign it to a new unused IP address for now.  Assume 190.0.2.0/23 is the address for private subnet and 190.0.4.1 is our firewall.    
5. Associate route table with backend private subnet.     
![backend subnet](images/backend-subnet.png) 

## VNET Peering
Peering is when you connect two virtual networks together. This means all the resources in one virtual network can access the resources in another network and vice versa.

Azure supports the following types of peering:    

**Virtual network peering**: Connect virtual networks within the same Azure region.  
**Global virtual network peering**: Connecting virtual networks across Azure regions.      
### To Add Peering 

Two types of peering:  
1. VNET Peering within the same region: 0.01 per GB for inbound and outbound transfer.  
2. Global VNET Peering:
		- inbound and outbound have different costs    
		
![peering](images/peering.png)

When we use VN Gateway to connect to a network, we are using the same tech to connect.  From your corporate on-premise network into Azure, use VN Gateway from the Azure end to connect to the physical gateway from your on-premise network.   

ForVPN Gateway Type (VNET-to-VNET connection) - this is charged based on time provisioned and available.    

![vpn-gateway](images/vpn-gateway.png)  



