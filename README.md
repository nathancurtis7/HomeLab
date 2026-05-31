# Cybersecurity Home Lab

## Overview
This repo documents my personal cybersecurity home lab used to emulate real threat actor behaviour and enhance my understanding of how real attacks are conducted.
The lab is designed to mirror a small enterprise-style environment using both Splunk/Sentinel to gain experience with more than just one SIEM tool.

## Lab Infrastructure
  - **Attacker Laptop**
    - Running Kali Linux VM and Splunk ubuntu server VM
    - Used to attack the victim machine

  - **Victim Laptop**
    - Running Windows11 with reduced security baseline to allow for exploitation
    - Event logs are recorded here and sent to Splunk/Sentinel through Splunk Universal Forwarder and Azure Monitor Agent

  - **Networking**
    - Isolated lab network using private RFC1918 addressing (`10.10.10.0/24`)
    - The two laptops are connected via a managed switch, ethernet cables and 

## Disclaimer
All activity is conducted within an isolated lab environment.
No testing is performed against production or external systems.
