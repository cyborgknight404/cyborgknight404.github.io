---
layout: default
title: Log Parser Tool – Simple Log Scrubbing for Suspicious Entries
permalink: /posts/log-parser-tool
tags: [tool, python, log-analysis, detection, scripting]
date: 2025-04-10
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

