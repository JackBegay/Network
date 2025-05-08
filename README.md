### Network Creation

## Objective
Using Cisco's Packet Tracer, my goal was to create a mock network that could be used for a medium sized company accross multiple sites. It needed to have one router per site and two sites having a DHCP servers with multiple computers or laptops connected to their sites router. I also wanted one site to have only servers, one DNS and one HTTP. I need to configure all the routers and servers at each site with their IPv4 addresses, subnet masks, and gateways. Once finished I want to be able to ping a server from a router at a different site. 

## Skills Learned
- Knowledge in building a network
- Ability to configure routers and servers
- Proficiency in connecting network and end devices

## Tools Used
- Cisco Packet Tracer

## Steps
1. First I put the router at site 2 holding the HTTP and DNS servers, which needed a dual port for the WAN interface cards to connect to both of the other routers. I configured the router using the CLI and typed in the IP address for site 2, as well as the IP addresses for both the serial connections to the two other sites.
![Screenshot 2025-05-07 174405](https://github.com/user-attachments/assets/cb9f61b1-af9e-4ed6-b2e3-062eee3294cc)

2. The other two routers were configured similarly with site 1 using IP address 192.168.4.1 and site 3 using 192.168.3.1 . Once configured I also connected the routers directly to site 2 using serial cables and input the serial ip addresses for both.
![Screenshot 2025-05-08 124914](https://github.com/user-attachments/assets/96a34f9b-0e78-429b-8c1a-49597e8b4df2)
![Screenshot 2025-05-08 124948](https://github.com/user-attachments/assets/b9b938db-c58c-488e-a4f0-63edf3ccbf11)

3. After this I set up a DNS and HTTP server at site 2 that is connected to the router through a multilayer switch. I turned on HTTP service for one server and DNS for the other and connected them to the multilayer switch using copper straight through wire into the ethernet ports. In IP configuration on the DNS server I gave it an IP address, corresponding Class C subnet mask, gateway, and made the DNS server its own IP address. For the HTTP server everything was the same except its own IP address.
