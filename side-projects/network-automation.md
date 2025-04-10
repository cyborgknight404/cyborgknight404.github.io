---
layout: default
title: Network Automation (WIP)
description: Smarter DNS, traffic filtering, and home-to-lab segmentation.
permalink: /side-projects/network-automation
---

## 🧠 What It Is

This is my ongoing attempt to make my home network smarter, quieter, and more blue team friendly—without dropping enterprise-level cash or overengineering everything.

It's a mix of **Pi-hole**, **Unbound**, **static assignments**, and plans for full **VLAN segmentation** between home, lab, and “untrusted” devices.

---

## ⚙️ Stack So Far

- **🚫 Pi-hole** for DNS filtering + ad/tracker blocking  
- **🧭 Unbound** as a recursive DNS resolver (no upstream leak)  
- **🖥️ Static IP mapping** for all lab VMs and admin boxes  
- **📡 Syslog forwarding** from network activity to Security Onion

---

## 🔐 Next Steps

- Build out **VLAN separation** for IoT vs lab vs admin  
- Add a **failover Pi-hole or bind9 secondary**  
- Route logs from DHCP/DNS into detection tooling (Wazuh/Elastic)  
- Test **DNS tunneling detection** on filtered vs unfiltered clients

---

## 🧪 What I'm Testing

- How granular DNS blocking impacts endpoint telemetry  
- If Pi-hole can log enough for alert correlation  
- Writing alert logic for **DNS exfil**, **sinkhole hits**, and **blocked domains**

---

## 🤔 Why It’s Worth Doing

This kind of project:
- Sharpens **network visibility**  
- Forces you to think in layers (isolation, logging, detection)  
- Makes you build the glue between devices and your lab stack

Also: I like making traffic disappear when advertisers try to sniff around.

---

## 🛠 Status

Still in heavy flux. Documenting configs once I settle on a structure worth reusing.
