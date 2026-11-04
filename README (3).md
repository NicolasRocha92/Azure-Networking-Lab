<div align="center">

# ☁️ Microsoft Azure Compute & Networking

### Virtual Machines, ICMP Connectivity, Firewalls, and Wireshark

</div>

## Project Overview

This tutorial documents my hands-on practice with Azure virtual machines and basic network troubleshooting. I used a Windows virtual machine and an Ubuntu Linux virtual machine to observe ICMP connectivity, investigate firewall behavior, and inspect network packets using Wireshark.

## Environments and Technologies Used

- Microsoft Azure (Virtual Machines, Virtual Networks, Network Security Groups)
- Remote Desktop
- Wireshark
- Windows PowerShell and Command Prompt
- Linux terminal, ping, and UFW

## Operating Systems Used

- Windows 10
- Ubuntu Linux

## Objectives

- Inspect Windows and Linux virtual machines in Azure.
- Test network connectivity using ICMP ping.
- Capture and interpret ICMP packets in Wireshark.
- Explore how firewall and network security settings affect traffic.
- Observe DNS and other network traffic.

## Steps and Screenshots

### Step 1: Review the Azure virtual machines

I viewed the Ubuntu Linux virtual machine in the Azure portal and checked its running status and configuration.

![Step 1: Review the Azure virtual machines](01-Screenshot%202026-10-11%20155840.png)

### Step 2: Review the Windows virtual machine

I viewed the Windows virtual machine in Azure, which served as the workstation for the network tests.

![Step 2: Review the Windows virtual machine](02-Screenshot%202026-10-11%20155940.png)

### Step 3: Capture ICMP traffic with Wireshark

On the Windows VM, I used Wireshark alongside a PowerShell ping test to observe ICMP packets and connectivity to the Linux VM.

![Step 3: Capture ICMP traffic with Wireshark](03-ChatGPT%20Image%20Oct%2011%2C%202026%2C%2004_38_51%20PM.png)

### Step 4: Inspect Linux network security settings

I opened the Linux VM network settings in Azure to review the inbound security rules relevant to connectivity testing.

![Step 4: Inspect Linux network security settings](04-Screenshot%202026-10-11%20165213.png)

### Step 5: Observe a failed ping test

I captured the ICMP traffic while ping requests timed out, demonstrating how network filtering or configuration can affect connectivity.

![Step 5: Observe a failed ping test](05-ChatGPT%20Image%20Oct%2011%2C%202026%2C%2004_55_37%20PM.png)

### Step 6: Retest ICMP connectivity

I continued testing with ping and Wireshark and observed replies during a later test, comparing the network behavior.

![Step 6: Retest ICMP connectivity](06-ChatGPT%20Image%20Oct%2011%2C%202026%2C%2004_56_16%20PM.png)

### Step 7: Check the Linux firewall

I used the Linux terminal to inspect the UFW firewall status while Wireshark continued capturing traffic.

![Step 7: Check the Linux firewall](07-ChatGPT%20Image%20Oct%2011%2C%202026%2C%2005_00_44%20PM.png)

### Step 8: Inspect DNS resolution

I used a Linux terminal to look up a domain name and reviewed the corresponding DNS packets in Wireshark.

![Step 8: Inspect DNS resolution](08-ChatGPT%20Image%20Oct%2011%2C%202026%2C%2005_04_33%20PM.png)

### Step 9: Inspect Windows network configuration

I ran `ipconfig /renew` in Windows PowerShell to examine the client networking configuration and DHCP behavior.

![Step 9: Inspect Windows network configuration](09-ChatGPT%20Image%20Oct%2011%2C%202026%2C%2005_06_31%20PM.png)

### Step 10: Review captured network protocols

I examined additional traffic in Wireshark, including application and network protocol exchanges, to practice packet inspection.

![Step 10: Review captured network protocols](10-ChatGPT%20Image%20Oct%2011%2C%202026%2C%2005_09_06%20PM.png)

## Skills Demonstrated

- Provisioning and inspecting cloud-based Windows and Linux systems
- Basic network troubleshooting with ping and command-line tools
- Reading Wireshark packet captures
- Understanding ICMP requests and replies
- Reviewing firewall and network security settings
- Observing DNS and other network protocols

## Conclusion

This lab strengthened my understanding of cloud networking and how to troubleshoot connectivity problems by combining command-line tests, Azure networking settings, and packet captures.

> **Note:** Screenshots document the visible test results. Firewall settings used for testing should be restored to a secure configuration after completing a lab.
