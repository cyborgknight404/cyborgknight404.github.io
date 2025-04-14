---
layout: post
title: "Log Parser Tool – Simple Log Scrubbing for Suspicious Entries"
author: Cyborg Knight
date: 2025-04-10
permalink: /posts/log-parser-tool
tags: [tool, python, log-analysis, detection, scripting]
categories: [cybersecurity, scripting, portfolio]
image: /assets/images/log-parser-pokemon-card.png
description: "A simple Python log parser that scans for suspicious entries and scrubs your syslog like a digital detective’s starter kit."
---

# 🔍 Log Parser Tool – Simple Log Scrubbing for Suspicious Entries

I built a basic **Python CLI tool** to scan syslogs and flag potentially suspicious activity. It’s simple, but useful—and it’s helping me level up my scripting and blue team chops.

---

## 🛠️ Features

- Scans `syslog` or any `.log` file line by line
- Matches against a keyword list (customizable)
- Flags suspicious entries to a new log with timestamps
- CLI arguments for input/output files

---

## 🧪 Sample Use Case

