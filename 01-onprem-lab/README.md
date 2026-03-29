# On-Prem Virtual Infrastructure Lab

## Objective
Build a virtualized lab environment to simulate cloud infrastructure.

## Environment
- Hyper-V
- Windows Server 2019 (Management)
- Fedora Server (CLI only)

## Hardware
- Intel i5-7500
- 48GB RAM
- 500GB SSD (Host OS)
- 1TB SSD (VM storage)
- 2x 4TB HDD

## Status
✔ Hyper-V configured  
✔ Windows Server VM installed  
✔ Fedora Server VM installed  

## Security
### SSH Hardening

Configured secure SSH access on the Fedora VM:

- Disabled password authentication
- Disabled root login
- Enabled SSH key authentication only

This ensures that the server can only be accessed using a private SSH key, which significantly improves security compared to password-based login.

### Verification

- Successfully connected to the server using SSH key authentication
- Confirmed that password login is no longer allowed
