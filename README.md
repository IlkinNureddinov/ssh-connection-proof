  Overview
This project demonstrates the successful configuration of SSH access on a Cisco router.
The goal was to establish a secure, encrypted remote connection without relying on insecure protocols like Telnet.

I completed the setup by configuring SSH on the router, generating RSA keys, and verifying the secure connection via SSH client.

  Topology
Device: Cisco Router 1921

IP Address: 192.168.1.1

SSH Port: Default (22)

  Configuration Steps
Configure a hostname and domain name:

Router(config)# hostname R1
R1(config)# ip domain-name ilkin.local

Generate RSA keys:

R1(config)# crypto key generate rsa modulus 1024 

Set SSH version and create user credentials:

R1(config)# ip ssh version 2
R1(config)# username ilkin password cisco123

Enable SSH on the VTY lines:

R1(config)# line vty 0 4
R1(config-line)# login local
R1(config-line)# transport input ssh

Save the configuration:

R1# write memory

Proof of SSH Connection
Successfully connected to the router via SSH from my PC.


Skills Demonstrated
Basic SSH server setup on Cisco devices

Secure remote access configuration

Networking best practices for security (encryption over Telnet)

Future Plans
Extend the project by integrating SSH authentication via public keys

Build a complete home lab including routers, switches, and a Linux server

📬 Contact
Ilkin Nureddinov 
https://github.com/IlkinNureddinov
