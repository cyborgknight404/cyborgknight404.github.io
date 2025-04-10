---
layout: default
title: Projects
description: What I’ve built, broken, and refined
---

# 🛠️ Cybersecurity Projects

These are the primary technical projects I’m building to develop real-world, hands-on security skills—focusing on log analysis, blue team tooling, and home lab architecture.

---

<div class="card">
  <h3><a href="/projects/log-parser">🔍 Log Parser (Python)</a></h3>
  <p>A Python script that scans syslogs for suspicious entries based on keyword matching.</p>
  <ul>
    <li>🚀 CLI tool with customizable input/output</li>
    <li>📂 Flagged entries saved to a separate log file</li>
    <li>🛠 In progress: regex support and config options</li>
  </ul>
  <a href="/downloads/log-parser.py" download target="_blank">⬇️ Download Script</a>
</div>

<div class="card">
  <h3><a href="/projects/proxmox-lab">⚙️ Proxmox Cybersecurity Home Lab</a></h3>
  <p>A full-featured virtual cybersecurity environment using an old Mac Pro as a Proxmox host. Built for testing SIEMs, endpoint monitoring, and attack detection.</p>
  <ul>
    <li>🖥️ Security Onion, Suricata, Zeek, and Wazuh stack</li>
    <li>🔗 Simulated attacker + endpoint VMs</li>
    <li>🛠 Under active development</li>
  </ul>
  <a href="https://github.com/cyborgknight404/proxmox-lab" target="_blank">🔗 View GitHub Repo</a>
</div>

---

<style>
.card {
  background: #fff;
  padding: 1.5rem;
  margin-bottom: 1.5rem;
  box-shadow: 0 2px 8px rgba(0,0,0,0.05);
  border-radius: 8px;
}

.card h3 a {
  text-decoration: none;
  color: #111;
}

.card h3 a:hover {
  text-decoration: underline;
}
</style>
