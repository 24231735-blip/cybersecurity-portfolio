---
layout: default
title: Virtual Lab Setup and Connectivity Validation
permalink: /projects/virtual-lab-setup/
---
# Virtual Lab Setup and Connectivity Validation

## Objective

Build a controlled network for a classroom exercise and verify communication between two virtual machines while limiting their network exposure.

## Environment and tools

Oracle VirtualBox hosted Kali Linux and Metasploitable 2. Each guest used one host-only adapter on the 192.168.56.0/24 lab subnet. Kali used 192.168.56.103 and the lab target used 192.168.56.101. The guest configurations had no NAT or bridged adapters.

## Method

1. Inspected the network settings for each VM in VirtualBox and confirmed both were attached to the same host-only network.
2. Checked the active interface and address inside Kali.
3. Sent four ICMP echo requests from Kali to the lab target and recorded the result.
4. Reviewed both adapter configurations alongside an external reachability check to assess the isolation boundary.

## Results and evidence

Kali received four replies from the target with zero packet loss. The external test returned no replies. I used the adapter settings as the main evidence of the configured boundary because a failed ping alone cannot establish why an external host did not respond.

[Topology and connectivity record](evidence/connectivity/)

## What I would improve

I would save both guests’ adapter settings and routing tables alongside the ping result. That would let a reviewer verify the network boundary and reproduce the configuration checks without relying on an external ping as a proxy for isolation.
