# Cisco-network--labs
Cisco Packet Tracer Labs and Network Configurations

Project Overview:
This project guides you through building a small network using physical hardware (and Cisco Packet Tracer).
 
Device 	Interface 	IPv4 Address 	Subnet Mask (IPv4) 	Default Gateway (IPv4) 	Notes 
R1	    G0/0	      192.168.1.1	255.255.255.0	 	 
	      G0/1	      10.0.0.1	255.255.255.252	 	 
R2	    G0/0	      192.168.2.1	255.255.255.0	 	 
	      G0/1	      10.0.0.2	255.255.255.252	 	 
SW1	 	 	 	 	 
PC1	    F0/0	      192.168.1.10	255.255.255.0	      192.168.1.1	 
PC2	    F0/0	      192.168.1.20	255.255.255.0	      192.168.1.1	 
PC3	    F0/0	      192.168.1.30	255.255.255.0	      192.168.1.1	 
PC4    	F0/0	      192.168.1.40	255.255.255.0	      192.168.1.1	 
PC5    	F0/0	      192.168.1.50	255.255.255.0	      192.168.1.1	 
SW2	 	 	 	 	 
PC1	    F0/0	      192.168.2.10	255.255.255.0	      192.168.2.1	 
PC2	    F0/0	      192.168.2.20	255.255.255.0	      192.168.2.1	 
PC3	    F0/0	      192.168.2.30	255.255.255.0	      192.168.2.1	 
PC4  	  F0/0	      192.168.2.40	255.255.255.0	      192.168.2.1	 
PC5	    F0/0	      192.168.2.50	255.255.255.0	      192.168.2.1	 



In this project there were used next devices:
a)	2 switches (Cisco Catalyst 2960-24TT)
b)	2 routers (Cisco ISR 4331)
c)	10 PCs
d)	Cables

In the given diagram/topology, three network addresses are shown. Two of them are used to create connections between the PCs, switches, and routers on each side. The third network is used to connect the two routers (R1 and R2). In total, this topology creates two LANs, with five PCs on each side.

3 Network addresses (and Subnet masks):
192.168.1.0/24 (255.255.255.0)
192.168.2.0/24 (255.255.255.0)
10.0.0.0/30 (255.255.255.252)

1.	Configuration of Switches and Routers
On each Switches:
>enable
#conf t
#hostname SW1 (and SW2)
#enable secret cisco
#write memory

The same configurations are done on R1 and R2


2.	Configuration of PCs
IP addresses were assigned to each PC. 
On Network address 192.168.1.0 - .10; .20; .30; .40; .50
Default gateway 192.168.1.1

On Network address 192.168.2. - .10; .20; .30; .40; .50
Default gateway 192.168.2.1

Also, IP addresses were assigned to each Router interface:
>enable
#conf t
#intface g0/0
(c-if)#ip address 192.168.1.1 255.255.255.0

After configuring connection between two Routers they were “routed” via Network addresses.
Ip route 192.168.1.0 255.255.255.0 10.0.0.1
R1
G0/0 – 192.168.1.1  (255.255.255.0)
G0/1 – 10.0.0.1  (255.255.255.252)

R2
G0/0 – 192.168.1.1  (255.255.255.0)
G0/1 – 10.0.0.1  (255.255.255.252)

3.	Test Connectivity
Ping bwn PC1 of SW1 and PC1 of SW2 
  
 
Ping bwn PC3 of SW2 and PCPC3 of SW1 
  
 
Ping bwn R1 and R2 
 
All ping operations returned successful results, confirming that the network was set up correctly.


