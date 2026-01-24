# Networking Design

## Purpose
The networking design of this lab separates internal domain traffic from external internet access. This setup simulates a small enterprise environment where the Domain Controller manages internal communication while also providing controlled internet access.

## Configuration Summary
The lab uses a dual-NIC configuration on the Domain Controller:

- **External NIC**
  - Connected to the host network
  - Receives an IP address via DHCP from the home router
  - Provides internet connectivity to the Domain Controller

- **Internal NIC**
  - Connected to an isolated internal network
  - Uses a static IP address
  - Handles all domain-related traffic between the Domain Controller and client machines

The Windows 10 client VM uses a single internal network interface and receives its IP configuration from the Domain Controller.

## Key Decisions
- **Separate internal and external traffic:**  
  Using two NICs on the Domain Controller prevents domain traffic from directly interacting with the home network.

- **Internal-only client network:**  
  Client machines do not connect directly to the internet, which mirrors common enterprise network designs.

- **Domain Controller as gateway:**  
  Internet access for internal clients is routed through the Domain Controller using NAT, allowing centralized control of traffic.

- **Static IP on internal NIC:**  
  Ensures consistent DNS and gateway configuration for Active Directory services.

## Outcome
- Client machines can communicate with the Domain Controller and each other
- The Domain Controller has internet access for updates and management
- Internal clients can access the internet through NAT while remaining isolated from the home network
- Active Directory and DNS function reliably within the internal network
