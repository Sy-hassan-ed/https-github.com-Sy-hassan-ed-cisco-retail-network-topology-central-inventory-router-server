# https-github.com-Sy-hassan-ed-cisco-retail-network-topology-central-inventory-router-server
Network Design and Configuration Details
IP Addressing Scheme
The network consists of 6 retail stores and a centralized Headquarters (HQ) network. Each retail store operates in its own subnet to ensure organized traffic management and avoid IP conflicts.

Location	Router LAN IP	Subnet	PC IP Range
Store 1	192.168.1.1	192.168.1.0/24	192.168.1.10 – 192.168.1.12
Store 2	192.168.2.1	192.168.2.0/24	192.168.2.10 – 192.168.2.12
Store 3	192.168.3.1	192.168.3.0/24	192.168.3.10 – 192.168.3.12
Store 4	192.168.4.1	192.168.4.0/24	192.168.4.10 – 192.168.4.12
Store 5	192.168.5.1	192.168.5.0/24	192.168.5.10 – 192.168.5.12
Store 6	192.168.6.1	192.168.6.0/24	192.168.6.10 – 192.168.6.12
HQ LAN	10.0.0.1	10.0.0.0/24	10.0.0.10 – 10.0.0.13 (PCs)
HQ Server	10.0.1.2	10.0.1.0/24	Server IP: 10.0.1.2

Each router’s LAN interface acts as the default gateway for the devices in its subnet. The use of /24 subnet masks provides ample IP addresses for current devices and future growth while simplifying network segmentation.

Router Naming
Each retail store router is named after cities based in Islamabad for easy identification, such as:

I-8 Store Router

G-9 Store Router

F-10 Store Router

The centralized HQ router is named Central_HQ_Router. Naming routers based on location and role simplifies network management and troubleshooting.

Routing Protocols
The network implements both RIP (Routing Information Protocol) and OSPF (Open Shortest Path First) routing protocols:

RIP is used for its simplicity and ease of setup but has limitations such as slow convergence and a maximum hop count of 15, which restricts scalability.

OSPF addresses RIP’s limitations by offering faster convergence, hierarchical network design through areas, and support for larger and more complex topologies. OSPF is the primary protocol used to ensure efficient routing in this project.

VPN and Security
A VPN (Virtual Private Network) is established between the first retail store’s router and the HQ router to secure data transmission over potentially unsecured links. This ensures confidentiality and integrity of sensitive communications between locations.

Although a firewall was considered to further enhance network security, it was not implemented because each retail store router is connected through separate, unique paths to the centralized router, inherently providing a level of security and isolation.

Project Benefits
Demonstrates a scalable and realistic retail network topology with multiple branch offices.

Showcases proper subnetting and IP addressing for efficient network segmentation.

Highlights the advantages and limitations of different routing protocols (RIP and OSPF).

Implements VPN for secure communication between key network points.

Provides a strong foundation for understanding enterprise network design, routing, and security.

Overall Project Scope
This topology models a medium-sized retail enterprise with multiple branch stores interconnected through a centralized HQ, illustrating the complexities and best practices in modern network design. It can be expanded or modified to include advanced features such as firewall integration, advanced routing policies, and cloud connectivity.
