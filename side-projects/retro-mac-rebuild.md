---
layout: default
title: Retro Mac Pro Rebuild
description: Repurposing a 2008 Mac Pro into a hybrid lab server and utility box.
permalink: /side-projects/retro-mac-rebuild
---

## 💾 What It Is

This side project was about turning a pair of aging 2008 Mac Pros into something useful: a **hybrid NAS, utility server, and Proxmox host** for cybersecurity experiments and home network services.

---

## 🧱 Hardware Salvage

- Combined parts from **two Mac Pro towers** (Model A1186, early 2008)
- Swapped RAM between machines to max out capacity
- Used the unit with a **functional power supply + better airflow**
- Manually fixed a bent drive bay to restore SATA connectivity
- Installed a **120GB SSD** for OS boot and **two HDDs** for data/storage

---

## 🖥️ What It's Doing

- Hosting lightweight **file shares** and static web content
- Running base Proxmox services and test VMs
- Future candidate for local-only DNS, backup scripts, or asset monitoring

---

## 🤔 Why It Matters

- Hands-on practice with **legacy hardware diagnosis and recovery**
- Reinforces practical skills in cabling, airflow, power, and thermal handling
- Useful testing ground for isolated workloads without burning up newer hardware

---

## 🔄 Next Steps

- Install **smartmontools** and setup SMART disk monitoring
- Add a backup routine to sync file shares to a separate volume
- Create a **shared ISO + VM template vault** for lab redeployments

---

## 🧠 Notes to Self

This machine isn’t built for speed—but it’s **quiet, functional, and reliable**. A perfect scratchbox for experiments that don’t require horsepower but benefit from having a real box on the network.

Still booted off the first Proxmox ISO flashdrive I ever created.
