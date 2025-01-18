<h1>Homelab Setup (Cisco Packet Tracer)</h1>

<h2>Brief Objective</h2>
The objective of this project was to establish a strong foundation in basic networking skills, providing hands-on experience in managing and securing a network environment. This setup allowed me to explore fundamental networking concepts, gain technical knowledge in device configuration, and understand the role of network security in a controlled lab environment using Cisco Packet Tracer.
<br />


<h2>Skills Learned</h2>

- <b>Network Security</b> 
- <b>Networking Configuration</b>
- <b>Firewall Security Management</b>

<h2>Network Topology</h2>


<h2>Steps</h2>

**Basic Network Configuration:** <br/>
To enhance network security and mitigate risks, I implemented network segmentation by utilizing the 'dhcp pool' command to assign IP addresses to clients based on their connection type. This approach effectively separates wired and wireless networks, ensuring that if the wireless network were compromised, its impact would be isolated from the rest of the network infrastructure. <br/>

<br />
<br />
**Wireless Router Configuration:** <br/>
To further secure the network, I configured the wireless router with specific settings to fortify the perimeter against unauthorized access and ensure a stable, secure connection for authorized devices.  <br/>

<br />
<br />
**Printer Configuration:** <br/>
To ensure reliable access to the network printer, I assigned a static IP address to the device. This guarantees that the printer’s IP address remains unchanged during power cycles, preventing connection issues for end devices that rely on a consistent IP address. The printer’s IP address was selected to be outside the DHCP pool to avoid any potential IP conflicts with other devices on the network

<br />
<br />
**DHCP Server Configuration:** <br/>
The DHCP service was disabled on the router, and the server was configured through the firewall for centralized management. The DHCP pool’s starting IP address was set to 192.168.1.102, as the IP address 192.168.1.101 had already been reserved for the printer, ensuring no conflicts.

<br />
<br />
**DNS Configuration:** <br/>
Through the DNS service, I configured a resource record on the server (IP address 192.168.1.254) to facilitate internet access from client devices, allowing them to resolve domain names when accessing web resources. <br/>

<br />
<br />
**Access Point Configuration:** <br/>
To extend wireless coverage and ensure connectivity for mobile devices (tablet and smartphone), I deployed an additional access point. This is especially important in large home office environments, where range limitations or interference from walls can disrupt wireless connectivity. The access point was configured with a broadcast name and secured using WPA2-PSK authentication to prevent unauthorized access.  <br/>

<br />
<br />
**Firewall Configuration for SSH Access:** <br/>
Using the command-line interface (CLI) of the firewall, I configured essential parameters including the hostname, password, username, and time settings. This setup lays the groundwork for future remote SSH access to the firewall’s command console, enabling secure remote management of the network infrastructure. <br/>

<br />
<br />
**Network Zone Security:** <br/>
I implemented a network zone security by assigning varying trust levels to each zone in the network. The internal network, where the most trusted devices reside, was given the highest security level. The DMZ, which contains partially trusted devices and external users, was assigned a medium level of trust, while the untrusted zone received the lowest security level. These security levels were configured through the CLI, ensuring a clear and structured segregation of network resources. <br />

<br />
<br />
**Remote SSH Configuration:**
To enable secure remote administration, I configured SSH access to the firewall’s command console. Using the AAA (Authentication, Authorization, and Accounting) protocol, I generated RSA key pairs to facilitate secure communication between the firewall and remote devices, ensuring encrypted and authenticated access.

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
