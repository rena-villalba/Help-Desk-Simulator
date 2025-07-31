# Lab Setup Instructions

## Prerequisites

- VirtualBox installed and configured.
- One VM running Windows Server (2019 or 2022) acting as the Domain Controller.
- One VM running Windows 10/11 Pro or Enterprise as the client.
- Both VMs are in the same internal network.
- The client VM is already joined to the domain.
- Active Directory is installed and functional along with the necessary tools.
- GPO has been configured on the DC to lock user accounts after 4 failed login attempts and a password policy.
