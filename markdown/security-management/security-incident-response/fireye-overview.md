---
title: FireEye Endpoint Security integration
description: FireEye Endpoint Security \(HX series\) helps organizations to inspect and analyze which contains known and unknown threats on any endpoint.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# FireEye Endpoint Security integration

FireEye Endpoint Security \(HX series\) helps organizations to inspect and analyze which contains known and unknown threats on any endpoint.

Skilled attackers today bypass traditional defences most security teams have relied on for years to protect their endpoints. Even when a traditional defence stops a known threat, it can’t determine what that threat was trying to do. FireEye HX Endpoint Security helps your security team hunt down and stop known and unknown advanced threats against your endpoints.

The Gold Standard Security Incident Response integration with FireEye HX, makes it easier and efficient for Security Analysts to investigate and remediate security incidents in an instant without having to navigate between tools. You can use network containment to perform remediation actions on the endpoints, implement profiles to gather specific details about the host, and perform specific queries or actions on the endpoint.

## Key features

-   Ability to perform host enrichment actions to gather more details about the endpoint such as host details, network statistics, user details, file details, process details, and service details.
-   Ability to perform Enterprise Security Search to sight potential malicious observables across endpoints, and take remediation actions.
-   Ability to gather Triage and Data Acquisition for in-depth endpoint inspection and analysis.

## Limitations

Following are the known limitations of this integration:

1.  Mid Application field value should be entered manually.
2.  Isolate Host and Get Running Services cannot be performed on Linux agent.
3.  Remove Isolation does not support for Linux agent.
4.  Triage Acquisition does not support for Linux agent.
5.  Users need to configure Show Enrichment Data related links. It is not available out of the box.
6.  For Sightings search only five active searches can be present at once. Remaining will be queued and will start after the completion of any one of the ongoing sightings.
7.  Sightings are available out of the box, which will be active false by default.
8.  Hash is not supported for Get Running Processes.

