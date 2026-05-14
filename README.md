# active-directory-lab
Windows Server 2022 Active Directory domain deployed on Proxmox – step-by-step guide
# Active Directory Domain Lab on Proxmox

## Objective
Deploy a Windows Server 2022 Active Directory domain on Proxmox to understand enterprise identity management, Group Policy, and user administration.

## Technologies Used
- Proxmox VE 8.x
- Windows Server 2022 Standard Evaluation (Desktop Experience)
- Active Directory Domain Services
- Group Policy Management
- Windows 10 client VM

## Lab Topology
| Component          | IP Address      | Role                        |
|--------------------|-----------------|-----------------------------|
| Domain Controller   | 192.168.0.120   | DC, DNS, homelab.local      |
| Client VM           | DHCP            | Domain-joined workstation   |
| Gateway             | 192.168.0.1     | Archer router               |

## Step-by-Step Implementation

### 1. Create the Windows Server VM
- Uploaded Windows Server 2022 and VirtIO ISOs
- Created VM with 4GB RAM, 2 cores, 40GB SCSI disk
- Attached both ISOs and set boot order to CD/DVD first

![VM Creation](<img width="597" height="447" alt="VMvm-creation" src="https://github.com/user-attachments/assets/6e616d53-c27e-45d7-bc7b-06b3c3efc5ef" />
)

### 2. Install Windows Server
- Selected Desktop Experience, loaded VirtIO SCSI driver to detect disk
- After first boot, loaded VirtIO network driver for Ethernet
- Set Administrator password: `Homelab2024!`

![Windows Desktop](<img width="983" height="615" alt="windows-desktop" src="https://github.com/user-attachments/assets/f057eb8a-0440-47a5-8273-81e691678796" />
)
