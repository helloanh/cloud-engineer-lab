# Virtual Network


## Create a virtual network with subnets
1. Create new virtual network with one default subnet named frontend (public subnet).  For example: 190.0.0.0/16 as the virtual network.  190.0.0.0/23 for frontend subnet. 
2. Create another subnet -- call this one backend (private subnet).  190.0.2.0/23 for backend subnet.
3. Create a new public IP address and give it a dns label.  
4. Create a new route table and add a route that routes all backend private subnet traffic to "Virtual appliance" as the hop type (this will be the firewall) and give the IP of this virtual appliance/firewall.  Asumming you already have a firewall or just assign it to a new unused IP address for now.  Assume 190.0.2.0/23 is the address for private subnet and 190.0.4.1 is our firewall.    
5. Associate route table with backend private subnet.     
![backend subnet](images/backend-subnet.png) 

## VNET Peering

