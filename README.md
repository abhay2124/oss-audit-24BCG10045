# oss-audit-24BCG10045

Student Name: Dalvendra singh 
Registration Number: 24BCG10045 
Chosen Software: Python 
Slot: E11 
Date of Submission: 31-03-2026


This repository contains a collection of shell scripts and a comprehensive audit report of the Python Programming Language, completed as a Capstone Project for the OSS NGMC Course.
These scripts are designed to demonstrate practical Linux skills—focusing on transparency, automation, and the free sharing of tools—which align with the core philosophy of open-source software.

Automation Scripts Overview
The five shell scripts included in this project connect to the broader open-source themes of system management and efficiency

1. Python Environment Auditor
Inspired by the Linux Footprint analysis in the report, this script identifies the current Python landscape on a Linux system.
   Functionality: Locates the main interpreter (e.g., /usr/bin/python3), identifies standard library paths, and lists system-wide vs. user-level packages.
   Security Check: Verifies if the Python binary is owned by root with 755 permissions to ensure system integrity.

2. Service Management Utility
Automates the management of Python-based daemons and web servers using systemd.
  Commands: Provides a streamlined interface for start, stop, restart, and status operations.
  Boot Management: Includes a feature to enable services to ensure they persist across system reboots.

3. Dependency & Security Updater
Implements the Two-Tier Update Model discussed in the audit.
  System Level: Triggers sudo apt upgrade python3 (or the dnf equivalent) to pull security patches for the CPython interpreter.
  Package Level: Updates third-party packages installed via pip to resolve vulnerabilities in the broader ecosystem.

4. Open Source License Header Injector
Promotes ethical software sharing by automating the inclusion of the Python Software Foundation (PSF) License headers in new projects
  Purpose: Ensures that the required copyright notices are retained, fulfilling the minimal obligations of the permissive PSF license.

5. Log Aggregator & Monitor
Monitors Python application logs typically stored in /var/log/.
  Utility: Provides real-time monitoring and filtering of application-level logs to help developers audit software behavior and catch bugs faster.


Dependencies
To run these scripts successfully, ensure your Linux environment (tested on Kali/Debian-based systems) has the following:
  Interpreter: /bin/bash.System 
  Tools: dpkg (for Script 2), stat, du, and cut (for Script 3), grep and tail (for Script 4).
  Permissions: Some scripts (like Script 3) may require sudo or root privileges to audit system-level directories like /root or /boot




Instructions to Run
  Follow these steps for each script in your Linux terminal:
    Navigate to the directory containing the scripts:
      Bashcd ~/Desktop
    Grant execution permissions to the scripts:
      Bashchmod +x script1_system_identity.sh script2.sh script3.sh script4.sh script5.sh
    Execute the scripts: 
    Script 1: ./script1_system_identity.sh 
    Script 2: ./script2.sh (Edit the PACKAGE variable in the script to check different tools) 
    Script 3: ./script3.sh 
    Script 4: ./script4.sh [logfile_path] [keyword] (e.g., ./script4.sh /var/log/syslog error) 
    Script 5: ./script5.sh (Follow the on-screen prompts)
