# metasploit-lab
Metasploit-lab documentation, including service enumeration and authorized bruteforce testing in controlled environment

##Environment

- Attacker machine: Kali Linux
- Target machine: Authorized virtual machine (lab environment)
- Network: Private / isolated lab network
- Tools: Metasploit Framework, Nmap

## Objective

The objective of this lab is to practice service enumeration and basic security testing
using the Metasploit Framework in a controlled and authorized environment.

## Service Enumeration

An initial network scan was conducted to identify open ports and active services
on the authorized target virtual machine.

The scan revealed the following open TCP ports and services:

- **21/tcp** – FTP service
- **22/tcp** – SSH service
- **139/tcp** – NetBIOS Session Service
- **445/tcp** – Microsoft Directory Services (SMB)
- **8000/tcp** – HTTP alternative service

The presence of multiple exposed services indicates a larger attack surface,
which is typical for intentionally vulnerable lab environments.

### SCAN RESULTS
<img width="998" height="460" alt="image" src="https://github.com/user-attachments/assets/c34c21ed-0f90-4c77-9395-5a6308f0075e" />

## Brute Force Simulation (SMB)

Based on the service enumeration results, the SMB service exposed on port 445
was selected for authentication testing.

An authorized brute-force simulation was performed using the Metasploit Framework
to evaluate the strength of the SMB authentication mechanism. A predefined
password wordlist was used during the test.

The initial attempt failed due to an incorrect service port configuration.
After correcting the target port to the standard SMB port (445), the brute-force
process was executed successfully.

Multiple authentication attempts were tested against the target service.
No valid credentials were discovered during this simulation, indicating that
the tested credentials were not sufficient to authenticate to the SMB service.

<img width="997" height="597" alt="image" src="https://github.com/user-attachments/assets/5503236a-98bb-4636-9953-4e964d5ccfdc" />
<img width="1010" height="267" alt="image" src="https://github.com/user-attachments/assets/f015a9f4-a794-4433-99c2-7a0c1dbe7fc5" />




