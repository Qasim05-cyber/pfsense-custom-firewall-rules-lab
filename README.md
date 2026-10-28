 # Configuring Custom Firewall Rules with pfSense

This project demonstrates practical firewall administration in an isolated lab environment. I configured restrictive LAN rules, inbound WAN rules for DMZ services, OpenVPN access, and a targeted ICMP rule using pfSense EasyRule.

## Objectives

- Plan and configure LAN firewall rules
- Permit HTTP, DNS, SSH/SFTP, and ICMP traffic
- Configure WAN access to a DMZ web and SFTP server
- Permit OpenVPN connections
- Validate rules with ping, nslookup, WinSCP, FileZilla, Thunderbird, OpenVPN, and Nmap
- Review blocked traffic in the pfSense firewall log
- Use EasyRule to create a precise ICMP pass rule

## Firewall Rules

LAN: TCP 80 for web browsing, TCP/UDP 53 for DNS, TCP 22 for SSH/SFTP, and ICMP for diagnostics.

WAN: TCP 80 to 172.40.0.20, TCP 22 to 172.40.0.20, UDP 1194 to 202.20.1.1, and a targeted ICMP exception to 202.20.1.1.

OpenVPN: VPN clients were allowed to access the LAN network 172.30.0.0/24 using any protocol.

## Verification Results

- LAN DNS and ICMP connectivity verified
- Corporation Techs website accessed successfully
- SFTP access verified with WinSCP and FileZilla
- OpenVPN connection established
- Thunderbird reached the internal mail service through the VPN
- Nmap identified TCP 22 and TCP 80 as open on TargetLinux01
- A blocked ICMP request was identified in the firewall log
- pfSense EasyRule created a precise ICMP pass rule

## Evidence

Screenshots from the completed lab report document the planner worksheets, firewall rules, connectivity tests, SFTP sessions, OpenVPN connection, Nmap results, VPN mail access, firewall log entry, and EasyRule configuration.

## Skills Demonstrated

pfSense, firewall rules, network security, stateful firewalling, ACL design, LAN and WAN segmentation, DMZ, OpenVPN, SFTP, Nmap, and firewall log analysis.

## Summary

This lab strengthened my ability to design least-privilege firewall rules, expose only required DMZ services, validate network behavior, and investigate blocked traffic using firewall logs.
