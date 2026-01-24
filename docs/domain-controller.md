# Domain Controller Configuration

## Purpose
The Domain Controller serves as the central authentication and directory service for this lab. It manages user accounts, computers, DNS, and provides core Active Directory functionality for the domain environment.

## Configuration Summary
- Windows Server 2019 virtual machine
- Active Directory Domain Services installed
- New forest and single domain created
- DNS installed and integrated with Active Directory
- Dual network interfaces:
  - External NIC for internet access
  - Internal NIC for domain traffic

The Domain Controller also hosts additional services used by the lab, including DNS and DHCP.

## Key Decisions
- **Single Domain Controller:**  
  A single DC was used to keep the lab focused and manageable while still demonstrating core Active Directory concepts.

- **DNS integrated with Active Directory:**  
  DNS is required for Active Directory to function properly. Integrating DNS with AD simplifies name resolution and supports dynamic updates.

- **Domain Controller hosting multiple roles:**  
  In a real enterprise environment, roles may be separated across servers. In this lab, DNS, DHCP, and routing services were hosted on the Domain Controller to reduce complexity and resource usage.

- **Static IP on internal network interface:**  
  A static IP ensures consistent DNS resolution and reliable communication between domain-joined systems.

## Outcome
- The domain was successfully created and is fully functional
- Users and computer objects can be managed through Active Directory Users and Computers
- Client machines can join the domain and authenticate using domain credentials
- DNS resolution works correctly for domain resources
