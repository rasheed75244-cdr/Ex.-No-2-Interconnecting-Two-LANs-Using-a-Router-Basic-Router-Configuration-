# Date :
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
<img width="541" height="455" alt="image" src="https://github.com/user-attachments/assets/737e6cd1-e8e5-450d-9c6b-9b54c2a846ae" />
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
<img width="873" height="880" alt="image" src="https://github.com/user-attachments/assets/9b11d973-9d6f-4962-a0ba-a988da8e2e9c" />
•	IP configurations on PCs<br>
<img width="890" height="892" alt="image" src="https://github.com/user-attachments/assets/95119232-2ca4-4d86-9ba0-1d94644111e9" />
<img width="887" height="902" alt="image" src="https://github.com/user-attachments/assets/cce6f377-6763-4e58-8e7d-8d147666949f" />
•	Successful ping between PC0 and PC1<br>
<img width="1341" height="1013" alt="Screenshot 2026-10-29 131516" src="https://github.com/user-attachments/assets/70bdd423-323c-44f7-ab6e-ca8d78e54228" />
<img width="1727" height="1002" alt="Screenshot 2026-10-29 131607" src="https://github.com/user-attachments/assets/a899e37a-2026-4cde-8db7-e0d3d6641a3a" />


________________________________________
# Result
Successfully configured a router to connect two LANs. Communication between PC0 and PC1 across different networks was tested and verified.

