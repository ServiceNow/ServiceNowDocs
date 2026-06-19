---
title: Virtual infrastructure security
description: Use virtualization with the flexibility to install multiple MID Servers in virtualized operating systems and networks in shared physical hardware.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/servicenow-ai-platform-security/virtual-infrastructure-security.html
release: australia
product: ServiceNow AI Platform Security
classification: servicenow-ai-platform-security
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
---

# Virtual infrastructure security

Use virtualization with the flexibility to install multiple MID Servers in virtualized operating systems and networks in shared physical hardware.

Access to the hypervisor and virtual infrastructure management consoles must be protected to prevent unauthorized cloning of the virtualized MID Server:

-   Limit the access to the hypervisor and virtual infrastructure management consoles by the trusted few admins.
-   Only allow connections to the internal trusted network for management console such as ESX Server and VirtualCenter.
-   Use VLANs to prevent network attacks.
-   Follow the security guidelines published in the virtualization hardening guides from the vendors.

