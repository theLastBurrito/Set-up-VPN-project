  <h2>Set up VPN Project</h2>

# Project Objective
- Set up and configure a private VPN on a Kali Linux virtual machine using WireGuard.
- Secure the connection between the server and client over the internet, ensuring encrypted and protected data transmission.
- Create a virtual VPN lab for testing security, IP forwarding, and communication between the VPN server and client.
- Test and verify successful connectivity from the client to the VPN server within the virtual private network.
The final objective is to gain hands-on experience with basic VPN setup, key pair management (public and private keys), and verifying that the VPN configuration works as expected.

# Tools Used
- <b>Kali Linux: The primary operating system used to run WireGuard and other network tools needed for VPN setup and testing.
- <b>WireGuard: A modern, lightweight VPN software that uses advanced cryptographic protocols to ensure high security.
- <b>VMware: Virtualization software used to run Kali Linux as a virtual machine.

# Skills Gained 
- Understanding of VPN and network security: Learn how VPNs work and the role of encryption in securing connections.
- Installation and configuration of WireGuard: Gain proficiency in installing WireGuard, configuring the main configuration file, and managing key pairs.
- Network configuration on Kali Linux: Set up iptables rules, configure NAT, and enable IP forwarding to support VPN functionality.
- Linux administration skills: Become comfortable with basic Linux commands and text editors within the terminal to manage configuration files.
- Troubleshooting and verification skills: Learn to check VPN connectivity, view WireGuard connection info using wg show, and troubleshoot as needed.

# Step
Update your system to ensure all packages are current and install WireGuard
<img src="https://github.com/user-attachments/assets/7f21c138-a391-41a4-b473-af8d7248481e" alt="Description" width="500">

# Generate Key Pairs
Create a directory for keys and ....
- Generate server key pair

<img src="https://github.com/user-attachments/assets/852b0994-7664-41a0-8f74-13d11a852708" alt="Description" width="500">

- Generate client key pair
  
<img src="https://github.com/user-attachments/assets/a707c4d5-d52b-4b2a-b374-6de07f341fc9" alt="Description" width="500">

# Configure the WireGuard Server
Create the configuration file for the WireGuard server

<img src="https://github.com/user-attachments/assets/d9bb4c27-5adf-4496-ab1e-7d046e76f363" alt="Description" width="500">

Edit wg0.conf with the following configuration

<img src="https://github.com/user-attachments/assets/fe66a7ba-c661-4133-97cf-b041917b6b6a" alt="Description" width="500">

Enable IP forwarding on the server

<img src="https://github.com/user-attachments/assets/90b748f9-1bbc-4fbb-912b-efc2344ea55c" alt="Description" width="500">

# Configure the WireGuard Client
Create the client configuration file

<img src="https://github.com/user-attachments/assets/74f58eaf-b8ab-4d25-a1f5-3f04d7815551" alt="Description" width="500">

Add the following configuration in client.conf

<img src="https://github.com/user-attachments/assets/d4046dbe-2bb8-41c7-993a-9580e4130e96" alt="Description" width="500">

# Start WireGuard Service on the Server
Bring up the WireGuard interface on the server

<img src="https://github.com/user-attachments/assets/319bf27a-3b67-4cd1-8008-fb3ce4f3ad10" alt="Description" width="500">

Verify the WireGuard status on the server

<img src="https://github.com/user-attachments/assets/cf9e2bf3-7141-481b-8105-c268d1bf8fb9" alt="Description" width="500">

# Connect the Client to the VPN
Copy the client configuration to the client machine, if not on the same machine, and bring up the WireGuard interface

<img src="https://github.com/user-attachments/assets/c0f9e4df-3dca-45f2-bc5a-25a3bc3215eb" alt="Description" width="500">

Verify the client connection by pinging the VPN server

<img src="https://github.com/user-attachments/assets/a4b8df06-e5f4-4fac-b174-00b24aaea798" alt="Description" width="500">
