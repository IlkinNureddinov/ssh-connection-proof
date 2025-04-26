# ssh-connection-proof
Configuring Router and Connect with SSH 
hostname R1
ip domain-name ilkin.local
crypto key generate rsa modulus 1024 
username ilkin privilege 15 secret Cisco123
line vty 0 4
login local
transport input ssh
ip ssh version 2
