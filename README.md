In Lecture 26, we covered the SIEM landscape, Splunk’s architecture, the Sysmon + Universal Forwarder pipeline, SPL, and the detection-engineering loop. Lab 13 is where all of that stops being slides and starts being a thing running on your own VMs.

By the end of this lab you will have:

A Splunk Enterprise instance running in Docker on your Ubuntu VM (the same Ubuntu VM from Project 02)
A Splunk Universal Forwarder on your Windows VM shipping Sysmon events over port 9997
Atomic Red Team installed and generating real ATT&CK-mapped attacker behavior on demand
Three working SPL queries that detect those behaviors
A saved dashboard with a required process-over-time panel and at least one additional panel of your own design
Format: Hands-on. Assigned Thursday, April 23 (day of L26 delivery). Due and locked Tuesday, May 5 at 11:59 PM.

Why this lab exists: Project 03 asks you to build a working detection & response capability on top of your existing MedTech environment from Project 02. Lab 13 is the training-wheels version — you stand up the same toolchain P03 uses, run a couple of canned attacks against it, and prove the pipeline works end-to-end. When P03 drops, the hard part (does Splunk work at all? does the UF talk to it? is Sysmon forwarding?) is already done.

What you’ll learn:

How to stand up Splunk Enterprise in a container and configure the receiver port
How the Universal Forwarder ships Windows Event Log + Sysmon data to a central indexer
How to write SPL queries that filter, aggregate, and visualize event data
How to generate reproducible attacker behavior using Atomic Red Team (MITRE ATT&CK-mapped)
How to turn an SPL search into a dashboard panel, and a collection of panels into a dashboard
Relevant SLOs:

SLO 10: Detect malicious activity in computer systems and networks
SLO 5: Perform system administration tasks on command-line and scripts
