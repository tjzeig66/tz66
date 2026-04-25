### Network Configuration (Domain Controller & Client VM\

1.  Configured IPv4 settings on the Domain Controller (Windows Server 2022):

-Used Command Prompt on DC and typed in ipconfig to find IPv4, Subnet mask, and Default gateway

-Configured static IPv4 address

-Configured Subnet Mask

-Configured Default Gateway

### Network Connectivity (Client VM)

-Went to control panel 

-under network and sharing center 

-Went to change adapter options 

-Went to IPv4 Properties 

-used DCs static IP address as the client VMs Preferred DNS server

[Client DNS Configuration](screenshots/IPv4-DNS-DC-IP.png)

-made sure the client VM is connected by using ping command along with the IPv4 address in the command prompt

---

### Domain Join Process (Client VM)
1. Opened system properties on clien VM

2. selected "Rename this PC (advanced) and click on change

3. select domain option and enter AD domain name (tjzeig.local)

4. provide domain administrator credentials

[Domain Join Configuration](screenshots/domain-join-window.png)

6. Restarted pc to complete domain join
7. client VM logged into DC to prove domain join

[Domain Join Success](screenshots/domain-joined-success.png)
