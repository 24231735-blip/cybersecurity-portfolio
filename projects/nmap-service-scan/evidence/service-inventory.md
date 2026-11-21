---
layout: default
title: Selected Service Inventory Observations
permalink: /projects/nmap-service-scan/evidence/service-inventory/
---
# Selected Service Inventory Observations

This summary is reconstructed from Figure 8 and Table 1 of my Pathway assignment. The actions are proposed.

| TCP port | Service observed | Defensive action |
|---|---|---|
| 21, 2121 | FTP | Disable unused file transfer services and migrate required transfers to an approved encrypted service. |
| 22 | SSH | Review the installed package and limit access to approved administrators. |
| 23 | Telnet | Retire the legacy remote login service. |
| 80, 8180 | Web and application services | Check ownership and package versions, then patch, remove, or restrict based on need. |
| 139, 445 | SMB file sharing | Restrict access to approved clients and review share permissions. |
