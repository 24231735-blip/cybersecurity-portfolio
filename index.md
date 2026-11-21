---
layout: default
title: Cybersecurity Portfolio
---
# Cybersecurity Portfolio

Master of Cyber Security student at Universiti Malaya · Aspiring SOC analyst

[About](#about-me) · [Skills](#technical-skills) · [Training](#certifications-and-training) · [Projects](#projects) · [Reflection](#learning-journey) · [Career](#career-objective) · [Contact](#contact-information)

## About me

I’m Fatimah Abubakar Alfa, a Master of Cyber Security student at Universiti Malaya and a First Class Cybersecurity graduate from Nile University of Nigeria. My interest in security operations grew during a network security internship, where I observed how a SYN flood could disrupt a service. I wanted to understand what analysts see during an incident, how they decide which signals matter, and what evidence they need before escalating.

My work as a data analyst also shapes how I approach cybersecurity. Validating records and investigating inconsistencies taught me to check the quality of evidence before drawing conclusions. I bring that habit to my lab work, where I document what I tested, what I observed, and what I would investigate next. I’m currently building practical skills in network monitoring, log analysis, and incident triage as I work toward a role in security operations.

## Technical skills

| Skill | Current level and experience |
|---|---|
| VirtualBox and Linux networking | Working knowledge. I configured a [host-only virtual lab](projects/virtual-lab-setup/) and verified connectivity. |
| Nmap | Working knowledge. I documented a [service inventory](projects/nmap-service-scan/) for a lab VM. |
| Wireshark | Working knowledge from traffic analysis during a network security internship. |
| Splunk | Working knowledge from internship exposure to security monitoring and log analysis. |
| Wazuh | Beginner. I’m developing familiarity with alert review and endpoint monitoring. |
| Data validation and reporting | Confident. I use these skills in professional data analysis and bring them to documenting security findings. |

## Certifications and training

- Google Cybersecurity Professional Certificate.
- NITDA cybersecurity training through Coursera.
- Sapphital data security training.

## Projects

- [Virtual Lab Setup and Connectivity Validation](projects/virtual-lab-setup/) documents how I isolated two virtual machines and verified communication between them.
- [Nmap Service Inventory and Defensive Review](projects/nmap-service-scan/) shows how I translated lab scan observations into a baseline and hardening priorities.

## Learning journey

The virtual lab changed how I think about scope. Before doing the practical work, I understood that testing should stay within an authorised environment. Setting up a host-only network made that requirement concrete. I had to check the adapter mode on both virtual machines, confirm their local addresses, and demonstrate that they could communicate. The four successful ping replies gave me a clear record of reachability at the time of the test. Reviewing the adapter configuration separately helped me understand why a connectivity check and an isolation check answer different questions.

The service inventory taught me how to move from a tool result to a defensive decision. My scan recorded 23 open TCP ports, but the number alone told me very little about which changes to prioritise. When I reviewed the service identifications, I could group the findings by purpose and consider which services a system owner would actually need. Telnet was a useful example because its presence gave me a specific follow-up to document. I would confirm whether anyone depended on it, replace it with an approved encrypted remote access service, and verify the change through a new inventory.

One practical problem was that my first service-version scan appeared to stall. I already had a successful ping and a separate record of open ports, which helped me narrow the problem to the service identification stage. I reran that stage with a lighter probe profile and disabled reverse DNS lookups. The rerun finished in about 11.7 seconds and produced a saved result I could review. That resolved the immediate problem of getting usable output. Because I changed two settings together, I could not isolate the cause of the first delay. In a repeat exercise I would save the baseline output and change one setting at a time.

I still find alert correlation in a SIEM challenging. I can read individual events, but deciding which events belong to the same incident requires more practice. The lab reinforced the value of keeping an inventory, because a baseline gives an analyst a reference point when a service appears unexpectedly. I want to become better at combining that kind of asset context with the timestamps and identities in an alert.

By 31 January 2027, my goal is to complete two Wazuh triage exercises using test data. For each exercise I will write a one-page investigation note that records the alert, relevant events, a short timeline, my severity assessment, and whether I would escalate. I will measure completion by checking that both notes contain enough detail for another reader to follow how the evidence led to my decision.

## Career objective

My immediate goal is to work as a Tier 1 SOC analyst, where I can investigate alerts, document findings, and support incident escalation. I want to become comfortable following an alert from the first indicator through to a decision about its severity and next steps. My data analysis background gives me experience checking evidence and communicating findings, and I want to apply those skills to security events.

My next steps are to build a small log-monitoring lab, practise investigating test alerts, and document two investigations using a consistent format that records the evidence, timeline, and escalation decision. I will also use entry-level SOC job descriptions to identify gaps in my skills and prioritise what I practise. Over time, I want to move into detection engineering and explore how explainable machine learning can support alert triage.

## Contact information

[GitHub](https://github.com/24231735-blip)
