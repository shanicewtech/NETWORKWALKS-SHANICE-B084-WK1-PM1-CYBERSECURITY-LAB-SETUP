# NETWORKWALKS-SHANICE-B084-WK1-PM1-CYBERSECURITY-LAB-SETUP
Building an isolated virtual lab for penetration testing and ethical hacking practice

📌 Project Overview

This project documents the setup and configuration of a virtual cybersecurity laboratory using Oracle VirtualBox and Kali Linux as part of the Networkwalks Cybersecurity Internship, Week 1 assessment.

The purpose of this project is to establish a controlled virtual environment for cybersecurity learning, penetration testing, network reconnaissance, vulnerability assessment, and ethical hacking practice.

The laboratory uses a dedicated NAT Network to provide network connectivity for the Kali Linux virtual machine while preparing the environment for future cybersecurity exercises.

🎯 Objectives

The main objectives of this project were to:

Install and configure Oracle VirtualBox.

Install and import Kali Linux as a virtual machine.

Create a dedicated NAT Network using the 10.0.0.0/24 subnet.

Configure the Kali Linux network adapter.

Assign a static IPv4 address to the Kali Linux virtual machine.

Enable clipboard sharing and file drag-and-drop.

Configure a shared folder between the host and guest operating systems.

Verify network connectivity and internet access.

Create a clean virtual machine snapshot.

Document the laboratory configuration and setup process.

🛡️ Purpose of the Lab

The laboratory provides an isolated and controlled environment for cybersecurity learning and authorized security testing.

The environment will serve as a foundation for future activities, including:

Network reconnaissance.

Port scanning.

Vulnerability assessment.

Packet analysis.

Web application security testing.

SQL injection practice.

Ethical hacking exercises.

Security tool experimentation.

Important: All security testing must be performed on systems owned by the user or where explicit authorization has been granted.

🏗️ Lab Architecture

The laboratory consists of a Windows host operating system running Oracle VirtualBox, with Kali Linux operating as the virtual cybersecurity machine.

The Kali Linux virtual machine connects to a dedicated NAT Network configured with the IPv4 subnet 10.0.0.0/24.

The network provides internet connectivity and allows additional virtual machines to be connected to the same network for future authorized security testing.

⚙️ Lab Configuration

Component

Configuration

Host Operating System

Windows

Virtualisation Software

Oracle VirtualBox

Guest Operating System

Kali Linux 2026.3

Virtual Network

NAT Network

Network Name

NatNetwork

IPv4 Network Prefix

10.0.0.0/24

Kali Linux IP Address

10.0.0.2/24

Subnet Mask

255.255.255.0

Default Gateway

10.0.0.1

DNS Server

8.8.8.8

DHCP

Enabled on NAT Network

IPv6

Disabled

Snapshot Name

My fresh Kali Linux

Shared Folder

/downloads

Shared Clipboard

Bidirectional

Drag and Drop

Bidirectional

🪜 Lab Setup Procedure

Step 1: Install 7-Zip

7-Zip was installed to extract the Kali Linux virtual machine package where required.

Tool: 7-Zip

Step 2: Install Oracle VirtualBox

Oracle VirtualBox was installed to provide the virtualisation environment required to run Kali Linux as a guest operating system.

Step 3: Configure the NAT Network

A dedicated NAT Network named NatNetwork was created in Oracle VirtualBox.

The following network configuration was applied:

Network Name: NatNetwork

IPv4 Prefix: 10.0.0.0/24

DHCP: Enabled

IPv6: Disabled

The NAT Network provides a virtual network for connected machines and allows them to communicate with one another while supporting outbound internet connectivity.

Step 4: Download and Import Kali Linux

Kali Linux was downloaded from the official Kali Linux website and imported into Oracle VirtualBox as a virtual machine.

The virtual machine was configured to use the previously created NAT Network.

Network Adapter Configuration:

Enable Network Adapter: Enabled

Attached to: NAT Network

Network Name: NatNetwork

Cable Connected: Enabled

Step 5: Configure Kali Linux Network Settings

The Kali Linux network configuration was completed using a static IPv4 address.

The following settings were configured:

Network Setting

Value

IPv4 Address

10.0.0.2

Subnet Mask

255.255.255.0

Default Gateway

10.0.0.1

DNS Server

8.8.8.8

The static IP configuration provides a consistent address for identifying and accessing the Kali Linux virtual machine within the laboratory network.

Step 6: Enable Shared Clipboard and Drag-and-Drop

The VirtualBox shared clipboard and drag-and-drop features were enabled to improve communication between the Windows host and Kali Linux guest operating systems.

The following settings were applied:

Shared Clipboard: Bidirectional

Drag and Drop: Bidirectional

These settings allow supported text and file transfers between the host and guest environments.

Step 7: Configure Shared Folders

A shared folder was configured in Oracle VirtualBox to allow files to be transferred between the Windows host operating system and Kali Linux.

The host's /downloads folder was configured as the shared folder for the virtual machine.

This provides a convenient method for transferring files without requiring separate external storage devices.

Step 8: Create a Virtual Machine Snapshot

After completing the initial Kali Linux installation and configuration, a virtual machine snapshot was created.

Snapshot Name: My fresh Kali Linux

The snapshot provides a recovery point that allows the virtual machine to return to its saved configuration if future cybersecurity exercises affect the system.

🔎 Lab Verification

Network configuration and connectivity were verified using Linux terminal commands.

Test

Command

Purpose

Check IP Address

ip -4 addr

Inspect assigned IPv4 addresses

Check Routing Table

ip route

Verify routing information and default gateway

Test Gateway

ping -c 4 10.0.0.1

Test connectivity to the NAT Network gateway

Test Internet Connectivity

ping -c 4 8.8.8.8

Test external network connectivity

Test DNS Resolution

nslookup google.com

Verify DNS resolution

Expected Network Configuration

IP Address: 10.0.0.2/24

Gateway: 10.0.0.1

DNS Server: 8.8.8.8

The network connectivity tests were used to verify that Kali Linux could communicate through the configured virtual network and access the internet.

🐞 Troubleshooting and Verification

During the setup process, network connectivity was an important configuration area to verify.

The following checks were included in the troubleshooting process:

Confirming that the NAT Network was correctly created in VirtualBox.

Checking that the Kali Linux network adapter was attached to NatNetwork.

Verifying the assigned IPv4 address.

Inspecting the routing table.

Testing connectivity to the default gateway.

Testing external internet connectivity.

Checking DNS resolution.

For Kali Linux versions 2026.1 and newer running on VirtualBox 7, the instructor provided the following commands as a possible workaround if internet connectivity issues occur after static IP configuration:

sudo nmcli connection modify "Wired connection 1" ipv4.dad-timeout 0
sudo nmcli connection down "Wired connection 1"
sudo nmcli connection up "Wired connection 1"

Note: The network connection name may differ depending on the system configuration. The actual connection name should be identified before executing these commands.

💡 What I Learned

Through this project, I gained practical experience in setting up and configuring a virtual cybersecurity laboratory.

The key concepts and skills developed include:

1. Virtualisation

Understanding how Oracle VirtualBox allows multiple operating systems to run within a host computer.

2. Network Configuration

Learning how to create a NAT Network and configure virtual machine network adapters.

3. Static IP Addressing

Understanding IPv4 addresses, subnet masks, default gateways, and DNS configuration.

4. Linux Networking Commands

Using Kali Linux terminal commands to inspect IP addresses, routing information, and network connectivity.

5. Virtual Machine Snapshots

Understanding the importance of creating recovery points before conducting future cybersecurity exercises.

6. File Sharing and Integration

Configuring shared folders, shared clipboard, and drag-and-drop functionality between Windows and Kali Linux.

7. Technical Documentation

Learning how to document system configurations, commands, verification procedures, and technical activities in a structured manner.

🔐 Security and Ethical Use

This laboratory was established strictly for educational purposes and authorized cybersecurity testing.

All future penetration testing, vulnerability assessments, and exploitation exercises will be conducted within controlled environments or on systems where appropriate authorization has been obtained.

🔗 Tools and Resources

7-Zip: https://www.7-zip.org/download.html

Oracle VirtualBox: https://www.virtualbox.org/wiki/Downloads

Kali Linux: https://www.kali.org/get-kali/

Networkwalks: https://www.networkwalks.com/

👤 Author

Shanice Williams

Cybersecurity Intern | Batch B084

Networkwalks Cybersecurity Internship

📌 Project Information

Item

Details

Programme

Cybersecurity at Networkwalks

Batch

B084

Assessment

Week 1

Project Module

PM1

Project Title

Cybersecurity Lab Environment Setup

Virtualisation Platform

Oracle VirtualBox

Guest Operating System

Kali Linux

Repository

GitHub
