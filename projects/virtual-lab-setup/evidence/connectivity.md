---
layout: default
title: Lab Topology and Connectivity Record
permalink: /projects/virtual-lab-setup/evidence/connectivity/
---
# Lab Topology and Connectivity Record

This summary is reconstructed from figures 1–5 and 7 of my Pathway assignment.

| Component | Configuration recorded |
|---|---|
| VirtualBox host-only network | 192.168.56.0/24 |
| Kali Linux | 192.168.56.103/24, one host-only adapter |
| Metasploitable 2 | 192.168.56.101, one host-only adapter |
| Guest-to-guest test | Four ICMP requests, four replies, zero packet loss |
| External reachability check | No ICMP replies during the test |
