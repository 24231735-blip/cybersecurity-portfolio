---
layout: default
title: Nmap Service Inventory and Defensive Review
permalink: /projects/nmap-service-scan/
---
# Nmap Service Inventory and Defensive Review

## Objective

Document the services visible on one lab VM and use that inventory to explain how a defender could reduce unnecessary network exposure.

## Environment and tools

I used Nmap from Kali Linux against my Metasploitable 2 guest on the [VirtualBox host-only lab network](../virtual-lab-setup/).

## Method

1. Confirmed that the lab target was reachable from Kali.
2. Collected a TCP port inventory for the target and reviewed the port states.
3. Ran a service identification pass, saved the output, and grouped the observations by service purpose.
4. Documented defensive actions and distinguished the observed inventory from changes I would propose for a production system.

## Results and evidence

The TCP port scan reported 23 open and 977 closed ports in the tested set. The service identification pass completed in about 11.7 seconds. I used the output to identify legacy remote access, web, and file sharing services that a defender could review with the system owner.

[Selected observations and defensive actions](evidence/service-inventory/)

## What I would improve

I would review the inventory with the system owner, document which services are required, and schedule removal or restriction of unnecessary ones. After an approved change, I would collect a fresh inventory and compare it with the baseline. I would also check package inventories before using a service banner to make a patching decision.
