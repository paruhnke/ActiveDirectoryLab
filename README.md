# Active Directory Home Lab

## Overview
This project documents a full Active Directory home lab built using Oracle VirtualBox. The lab simulates a small enterprise Windows domain environment and demonstrates core Active Directory, networking, and automation concepts.

The goal of this lab was to gain hands-on experience with:
- Active Directory Domain Services
- Windows networking
- DNS, DHCP, and NAT
- PowerShell automation

## Technologies Used
- Oracle VirtualBox
- Windows Server 2019
- Windows 10
- Active Directory Domain Services (AD DS)
- DNS & DHCP
- Routing and Remote Access (NAT)
- PowerShell

## Lab Architecture
This lab consists of:
- One Domain Controller with two network interfaces
- One Windows 10 client joined to the domain
- An internal private network with internet access routed through the Domain Controller

## Documentation
- [Networking Design](docs/networking.md)
- [Domain Controller](docs/domain-controller.md)
- [DHCP and DNS](docs/dhcp-and-dns.md)
- [Client Machine](docs/client-machine.md)
