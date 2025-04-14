---
layout: default
title: "Proxmox on a 2008 Mac Pro: A Weekend of Perseverance"
description: "One vintage Mac Pro, one tangled mess of Ethernet cables, and one stubborn weekend later—how I turned chaos into a working homelab."
permalink: /posts/proxmox-on-2008-mac-pro
tags: [proxmox, homelab, mac pro, virtualization, self-hosting]
image: /assets/images/proxmox-macpro-thumbnail.png
date: 2025-04-14
---

This weekend, I went to war with an old 2008 Mac Pro and (eventually) won.

The Setup Attempt That (Almost) Broke Me
Over the past week, I sank an embarrassing number of hours into trying to get Proxmox VE up and running on one of my old Mac Pros. My first attempt was on a 2.8GHz model using a 120GB SSD that I had previously used in this machine. The install itself wasn’t too bad, but getting the thing networked was another story.

The Mac lives upstairs in my office, and Proxmox requires a wired connection (no built-in Wi-Fi support). That meant dragging an absurdly long Ethernet cable down the stairs and into the main Eero router—fun times on a weeknight. I got the OS running but didn’t have the energy to dive deeper at that point.

While I was poking around, I also discovered that one of the hard drive bays had a bent SATA connector. I was able to carefully bend the metal behind the connector back into place—surprisingly, it worked. All four drive bays are now populated and functional.

The Swap That Backfired
By Friday night, I got ambitious. I had another identical Mac Pro with a 3.0GHz processor lying around, and I figured, “Why not use the faster one?” I swapped over all the components and powered it on—nothing. No video output, even though I heard the chime and saw the fans spin.

I tried different SSDs (including a 512GB pulled from a dead Mac Mini), video cards, RAM configurations—nothing. I gave it a solid go, but eventually gave up and reverted everything back to the original 2.8GHz machine.

Back on the First Mac — and Still Fighting
Saturday morning, I finally got the original Mac to boot again. I had the bright idea of dual-booting with macOS, just in case I needed a fallback. That led me down a rabbit hole—installing Debian 12 on a separate partition, manually configuring everything before adding Proxmox. Sounds smart in theory. In practice, it was a nightmare.

Debian and Proxmox refused to cooperate with my partitioning scheme, throwing errors at every turn. I wasted hours troubleshooting before I finally admitted defeat and wiped the SSD clean. Full-disk Proxmox install. No fallback. No regrets.

After that, things actually started working.

Sunday: The Payoff
Once Proxmox was installed properly, I set a static IP for the server and started container installs. Here's what I’ve got running so far:

Pi-hole – up and blocking ads across the network

Home Assistant – working, still need to dial in the integrations

Plex – up and running as my main media server

Tautulli – tracking Plex usage like a champ

Plex Meta Manager – initial setup done, needs refinement

Each of these had their own quirks during install, but I'll cover the specific setup processes and configs in another post.

Storage Layout
With all four drive bays now usable, I set up the following storage configuration:

512GB SSD: Main boot drive running Proxmox

2×2TB HDDs: ZFS mirror pool for media storage (redundancy FTW)

1TB HDD: Local backup drive for the server itself

It’s not enterprise-grade, but it’s solid for a homelab, and the ZFS mirror should keep my media safe from single-drive failures.

TL;DR
Proxmox does technically run on a 2008 Mac Pro, but it’s not plug-and-play.

Forget dual-booting with macOS. Just dedicate the full SSD and save yourself the stress.

Expect to spend a solid weekend troubleshooting if you go this route.

Once installed, Proxmox is solid—and now I’ve got a local homelab server chugging away.

ZFS mirror for media. Backup drive for peace of mind.

Next up: breaking down how I configured each container and what I’d do differently next time.
