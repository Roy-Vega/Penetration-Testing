# Active Directory Laboratory - Summary

This project builds an AD lab in VMWare Workstation, using one domain controller (Windows Server 2022) and two domain users (Windows 11).

Below is a brief summary of the process.

#### Domain Controller:
- Changed the PC name.
- Made the PC a domain controller.
- Added Certificate Services.
- Created an OU to separate groups.
- Created a domain admin account, service account, and two low-level users part of the domain users group.
- Set up group policy for the entire domain.
- Set a static IPv4 address.
- Set up SQL Service account (SPN).
- Created an SMB file share.

#### User Machines:
- Created a local account.
- Renamed the PC.
- Joined machines to the domain by hardcoding (manually) IP address and setting a static DNS for domain-joined.
- Joined devices to the local AD domain.
- Checked if users joined Domain on DC.
- Set up local administrators on both user's devices.
- Enabled network discovery on both user's devices.
- Added a shared drive on one of the user devices.

After successfully building the laboratory, the following attacks were tested:
- Capturing hashes with Responder.
- Cracking hashes.
- LLMNR Poisoning.
- SMB Relay.
- Shell access through Psexec Metasploit.
- IPv6 DNS attacks with Mitm6.
- Domain Enumeration with ldapdomaindump, BloodHound, PlumHound, PingCastle.
- Pass Attacks.
- Kerberoasting.
- Token Impersonation.

It is important to note that the user devices on Windows 11 blocked various attacks, so the domain firewall and antivirus needed to be disabled to allow some attacks.
