<h1>Homelab Setup (Cisco Packet Tracer)</h1>

<h2>Brief Objective</h2>
The objective of this project was to establish a strong foundation in basic networking skills, providing hands-on experience in managing and securing a network environment. This setup allowed me to explore fundamental networking concepts, gain technical knowledge in device configuration, and understand the role of network security in a controlled lab environment using Cisco Packet Tracer. <br />


<h2>Skills Learned</h2>

- <b>Network Security</b> 
- <b>Networking Configuration</b>
- <b>Firewall Security Management</b>

<h2>Steps</h2>

**Network Topology:** <br/>
<br />
![1](https://github.com/user-attachments/assets/94a280cf-390d-4409-bbd8-ebe076b27759) <br />
<br />

**Basic Network Configuration:** <br/>
To enhance network security and mitigate risks, I implemented network segmentation by utilizing the dhcp pool command to assign IP addresses to clients based on their connection type. This approach effectively separates wired and wireless networks, ensuring that if the wireless network were compromised, its impact would be isolated from the rest of the network infrastructure. <br/>
<br />
![2](https://github.com/user-attachments/assets/baa757d0-352c-48ec-9555-030913706154) <br />
<br />

**Wireless Router Configuration:** <br/>
To further secure the network, I configured the wireless router with specific settings to fortify the perimeter against unauthorized access and ensure a stable, secure connection for authorized devices.  <br/>
<br />
![3](https://github.com/user-attachments/assets/641089fc-aaff-432a-9688-a753c0e4fa3e) <br />
<br />
![4](https://github.com/user-attachments/assets/26c564de-88ff-402b-8493-95f8959856f2) <br />
<br />

**Printer Configuration:** <br/>
To ensure reliable access to the network printer, I assigned a static IP address to the device. This guarantees that the printer’s IP address remains unchanged during power cycles, preventing connection issues for end devices that rely on a consistent IP address. The printer’s IP address was selected to be outside the DHCP pool to avoid any potential IP conflicts with other devices on the network. <br />
<br />
![5](https://github.com/user-attachments/assets/fc089eb3-c586-4dc2-9779-7a01f86c581d) <br />
<br />

**DHCP Server Configuration:** <br/>
The DHCP service was disabled on the router, and the server was configured through the firewall for centralized management. The DHCP pool’s starting IP address was set to 192.168.1.102, as the IP address 192.168.1.101 had already been reserved for the printer, ensuring no conflicts. <br />
<br />
![6](https://github.com/user-attachments/assets/43d432e4-dd06-49c2-a1d6-d5152cf1b622) <br />
<br />

**DNS Configuration:** <br/>
Through the DNS service, I configured a resource record on the server (IP address 192.168.1.254) to facilitate internet access from client devices, allowing them to resolve domain names when accessing web resources. <br/>
<br />
![7](https://github.com/user-attachments/assets/738fadb6-e5f9-45d6-8f5d-58faab525240) <br />
<br />
![8](https://github.com/user-attachments/assets/1f28549d-f832-4f92-8417-87d0367eae9d) <br />
<br />

**Access Point Configuration:** <br/>
To extend wireless coverage and ensure connectivity for mobile devices (tablet and smartphone), I deployed an additional access point. This is especially important in large home office environments, where range limitations or interference from walls can disrupt wireless connectivity. The access point was configured with a broadcast name and secured using WPA2-PSK authentication to prevent unauthorized access.  <br/>
<br />
![9](https://github.com/user-attachments/assets/e9a7e249-2e15-4548-b429-5eae338b2b7b) <br />
<br />

**Firewall Configuration for SSH Access:** <br/>
Using the command-line interface (CLI) of the firewall, I configured essential parameters including the hostname, password, username, and time settings. This setup lays the groundwork for future remote SSH access to the firewall’s command console, enabling secure remote management of the network infrastructure. <br/>
<br />
![10](https://github.com/user-attachments/assets/5e0df239-a1ff-4828-92ff-84ea57562b71) <br />
<br />

**Network Zone Security:** <br/>
I implemented a network zone security by assigning varying trust levels to each zone in the network. The internal network, where the most trusted devices reside, was given the highest security level. The DMZ, which contains partially trusted devices and external users, was assigned a medium level of trust, while the untrusted zone received the lowest security level. These security levels were configured through the CLI, ensuring a clear and structured segregation of network resources. <br />
<br />
![11](https://github.com/user-attachments/assets/9500a620-0db7-49c9-b1b3-d1a346854e99) <br />
<br />

**Remote SSH Configuration:**
To enable secure remote administration, I configured SSH access to the firewall’s command console. Using the AAA (Authentication, Authorization, and Accounting) protocol, I generated RSA key pairs to facilitate secure communication between the firewall and remote devices, ensuring encrypted and authenticated access. <br />
<br />
![12](https://github.com/user-attachments/assets/8a7bdf84-01fa-430f-b01f-36ce184ed062) <br />

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
