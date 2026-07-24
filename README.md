# Date : 24/07/26
## Ex.-No-2-Interconnecting-Two-LANs-Using-a-Router-Basic-Router-Configuration


# Objective
To configure a router to connect two separate LANs and enable communication between them using static IP addressing.
________________________________________
# Apparatus/Tools Required
•	Cisco Packet Tracer<br>
•	2 PCs<br>
•	2 Switches<br>
•	1 Router (e.g., 1841 or 2911)<br>
•	Straight-through cables<br>
________________________________________
# Network Topology Diagram
 Description:<br>
•	PC0 → Switch0 → Router (FastEthernet0/0)<br>
•	PC1 → Switch1 → Router (FastEthernet0/1)<br>
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/4bf2e902-9e39-4451-89da-87e8c49eba25" />

________________________________________
# IP Addressing Table
Device	Interface	IP Address	Subnet Mask<br>
PC0	NIC	192.168.1.10	255.255.255.0<br>
PC1	NIC	192.168.2.10	255.255.255.0<br>
Router0	FastEthernet0/0	192.168.1.1	255.255.255.0<br>
Router0	FastEthernet0/1	192.168.2.1	255.255.255.0<br>
________________________________________
# Procedure
1.	Open Cisco Packet Tracer and add 2 PCs, 2 Switches, and 1 Router.
2.	Connect each PC to a switch, and each switch to the router using straight-through cables.
3.	Assign IP addresses to both PCs according to the IP table.
4.	Configure the router interfaces:
o	FastEthernet0/0 → 192.168.1.1
o	FastEthernet0/1 → 192.168.2.1
5.	Use no shutdown on both router interfaces to activate them.
6.	Set each PC’s default gateway:<br>
o	PC0 → 192.168.1.1<br>
o	PC1 → 192.168.2.1<br>
7.	Test connectivity using ping from PC0 to PC1.<br>
________________________________________
# Commands Used (Router CLI)
bash<br>
CopyEdit<br>
Router> enable<br>
Router# configure terminal<br>
Router(config)# interface fastethernet0/0<br>
Router(config-if)# ip address 192.168.1.1 255.255.255.0<br>
Router(config-if)# no shutdown<br>

Router(config)# interface fastethernet0/1<br>
Router(config-if)# ip address 192.168.2.1 255.255.255.0<br>
Router(config-if)# no shutdown<br>
________________________________________
# Output (Screenshots)
•	Router CLI configuration<br>
•	IP configurations on PCs<br>
•	Successful ping between PC0 and PC1<br>
<img width="1919" height="1079" alt="Screenshot 2026-07-24 110236" src="https://github.com/user-attachments/assets/d89ce3f8-516f-42f1-a101-8cc15e90433b" />
<img width="1919" height="1079" alt="Screenshot 2026-07-24 110943" src="https://github.com/user-attachments/assets/643444a0-cd53-44cf-93a6-f4acb32e4414" />
<img width="700" height="712" alt="Screenshot 2026-07-24 110128" src="https://github.com/user-attachments/assets/22dc74b6-3ecb-42c1-90b8-1f8c81c78251" />
<img width="1919" height="1079" alt="Screenshot 2026-07-24 111109" src="https://github.com/user-attachments/assets/f0214c01-1d75-4bd2-b3f3-a5d1035fc912" />

________________________________________
# Result
Successfully configured a router to connect two LANs. Communication between PC0 and PC1 across different networks was tested and verified.

