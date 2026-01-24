# Client Machine Configuration

## Purpose
The client machine represents a typical domain-joined workstation in an enterprise environment. It is used to validate authentication, DNS, DHCP, and overall Active Directory functionality.

## Configuration Summary
- Windows 10 virtual machine
- Single internal network interface
- IP configuration received via DHCP
- Joined to the Active Directory domain
- Domain user login tested successfully

The client machine does not connect directly to the internet and relies on the Domain Controller for network services.

## Key Decisions
- **Internal-only network interface:**  
  The client VM is isolated from the home network and communicates only with the Domain Controller and other internal resources.

- **DHCP-based IP configuration:**  
  Automating IP assignment mirrors real enterprise environments and avoids manual configuration errors.

- **Domain authentication over local accounts:**  
  Logging in with domain credentials validates that Active Directory, DNS, and networking are functioning correctly.

- **Single client scope:**  
  One client VM was used to confirm domain functionality while keeping the lab simple and resource-efficient.

## Outcome
- Client successfully joined the domain
- Domain user accounts can authenticate on the client machine
- DNS resolution functions correctly for domain resources
- Internet access is available through the Domain Controller via NAT
