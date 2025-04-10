---
layout: default
title: Proxmox Lab Build – From Scrap to SOC
permalink: /posts/proxmox-lab-build
---

# ⚙️ Proxmox Lab Build – From Scrap to SOC

Here’s how I turned an old 2008 Mac Pro into a functional home lab running **Proxmox VE** and built for **cybersecurity testing** and **network services**.

---

## 🧱 The Hardware

- Mac Pro 2008 (2.8GHz Xeon) with 8GB → upgraded with RAM from a second donor machine
- 120GB SSD (Proxmox boot), 1TB + 2TB drives for VMs and storage
- Minor hardware fixes (bent bay realignment, thermal cleaning)

---

## 🖥️ The Stack (So Far)

- **Proxmox VE** as base hypervisor
- **Security Onion**, **Ubuntu**, and **Kali** for SOC-style simulations
- NAS-like services for local backups + file hosting
- Planning to add **Pi-hole**, **Unbound**, and segmented VLANs

---

## 🔄 Challenges

- EFI bootloader weirdness on Mac hardware
- Drive mounting issues from dead SATA bay
- RAM compatibility and thermals

---

## 🚀 Why It Matters

This box now functions as:
- A SOC simulation stack
- A log/packet analysis playground
- A real-world reflection of what you'd find in entry-level security ops

---

*This project evolves constantly, and I'll be adding detection pipelines, log forwarding, and attacker emulation over time.*
