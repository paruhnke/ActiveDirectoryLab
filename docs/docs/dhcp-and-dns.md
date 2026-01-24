# DHCP and DNS Configuration

## Purpose
DHCP and DNS provide automated network configuration and name resolution for the Active Directory environment. These services allow domain-joined clients to receive IP addresses automatically and locate domain resources reliably.

## Configuration Summary
- DHCP installed on the Domain Controller
- DHCP scope created for the internal network
- Clients receive IP configuration from the Domain Controller
- DNS installed and integrated with Active Directory
- Domain Controller configured as the primary DNS server for clients

The Windows 10 client uses DHCP for network configuration and relies on the Domain Controller for DNS resolution.

## Key Decisions
- **DHCP hosted on the Domain Controller:**  
  Centralizing DHCP simplifies management in a small lab and ensures consistent IP configuration for domain-joined systems.

- **DNS integrated with Active Directory:**  
  Active Directory depends on DNS for locating domain services. AD-integrated DNS supports dynamic updates and reduces manual configuration.

- **Clients use the Domain Controller as DNS:**  
  This ensures clients can resolve domain services such as authentication and Group Policy processing.

- **DHCP scope limited to internal network:**  
  Keeps lab traffic isolated and prevents interference with the home network.

## Outcome
- Client machines automatically receive valid IP addresses
- Domain name resolution functions correctly
- Clients can locate and authenticate to the Domain Controller
- Group Policy and other domain services apply successfully
