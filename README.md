# Scanning and Identifying Network Nodes


 

<h2>Description</h2>
Identifying local network configuration
Determining the configuration of the local host and its subnet, using tools such as ifconfig, ip, arp, netdiscover, and pathping. Running the scans from the KALI Linux VM and the DC1 Windows Server.

![Screenshot 2023-09-17 055703](https://github.com/Aaron504/Scanning-and-Identifying-Network-Nodes/assets/141078110/ecf2c37d-1dfa-42d2-9e51-4e3b74604a61) 
![Screenshot 2023-09-17 060129](https://github.com/Aaron504/Scanning-and-Identifying-Network-Nodes/assets/141078110/667e8c73-5104-47d1-b02f-4e0e8701c8c5) 
The ARP cache shows only machines that have communicated with the local host. To verify whether any other hosts are present, you can perform a "sweep" of the local network. One means of doing this is to use ping in a for/next loop. You can also use the netdiscover tool bundled with Kali.

![Screenshot 2023-09-17 060723](https://github.com/Aaron504/Scanning-and-Identifying-Network-Nodes/assets/141078110/c59bc48b-2ec7-4796-bd9d-fef85f82d543)

Running the following command to test the reliability (packet loss) and latency (delay) of the connection between the DC1 VM and the PT1-Kali VM (the test takes 30-45 seconds to run):

![Screenshot 2023-09-17 061243](https://github.com/Aaron504/Scanning-and-Identifying-Network-Nodes/assets/141078110/cdfa1253-2c42-4704-acfa-02b2a1022d07)







<h2>Use nmap to discover hosts</h2>
From a penetration tester or threat actor perspective, network reconnaissance will typically aim to discover the following:

Default gateway (the router connecting the subnet to other networks).

DNS server (used to resolve host names on the network).

Whether any network directory/authentication and application servers are present.

Whether any host/client access devices are present.

Whether any other types of devices (embedded systems or appliances) are present.

![Screenshot 2023-09-17 061824](https://github.com/Aaron504/Scanning-and-Identifying-Network-Nodes/assets/141078110/63b746f6-ec42-4767-af14-fe9bd53ef98c)
![Screenshot 2023-09-17 061846](https://github.com/Aaron504/Scanning-and-Identifying-Network-Nodes/assets/141078110/cb0bef28-f152-4472-8c0a-b0fdf657b151)

Query DNS
DNS provides name resolution to internal networks as well as the Internet. DNS is used any time a user or application refers to a host by name. DNS queries name records to find the IP address associated with a hostname or fully qualified domain name. These name records can also reveal information about how a network is configured. In this task, you will gather DNS information by using the dig utility.

![Screenshot 2023-09-17 062358](https://github.com/Aaron504/Scanning-and-Identifying-Network-Nodes/assets/141078110/db6efcd8-0de0-42a0-9cd2-ed83d67485c7)





