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
![Screenshot 2025-05-08 132739](https://github.com/user-attachments/assets/44d391d1-775f-4960-986c-d30774c2b2db)
![Screenshot 2025-05-08 132946](https://github.com/user-attachments/assets/a3e47e39-7d8c-49c6-b361-a0ecf6037c53)

4. Next I set up DHCP servers at site 1 and 3 to assign IP addresses to the computers and laptops at those sites. I turned on the DHCP service for both and configured them with an IP address, subnet mask, made gateway their respective IP address from each site, and made the DNS server the IP address from the DNS at site 2 for both.
![Screenshot 2025-05-08 133845](https://github.com/user-attachments/assets/1d3b7ab4-7b49-4c54-9ab0-b140418b1d42)

5. Then I set up two multilayer switches and four switches connected to those using copper cross over cables at site 1. Then used only one multilayer switch and two switches connected to it at site 3. I connected both DHCP servers to the mulitlayer switches at each site and put in all the computers and laptops connecting them in groups to a switch using copper straight through wire.
![Screenshot 2025-05-08 134713](https://github.com/user-attachments/assets/586893c2-d43f-49a3-8cf0-6ca63663e6aa)

6. Lastly I need to test if I can ping a server from a router at a different site. I tested the DHCP server at site 3 from the router at site 1 and did the opposite for the DHCP server and site 1 from the router at site 3 as well.
![Screenshot 2025-05-08 135219](https://github.com/user-attachments/assets/1e6b6fa0-1d18-4396-b291-a8db769985c0)
