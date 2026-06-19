---
title: Network security
description: The MID Server communicates on port 443 using SSL to the instance and requires no inbound connections.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/servicenow-ai-platform-security/network-security.html
release: australia
product: ServiceNow AI Platform Security
classification: servicenow-ai-platform-security
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
---

# Network security

The MID Server communicates on port 443 using SSL to the instance and requires no inbound connections.

To properly secure your MID server in a network, do the following:

-   Install the MID Server on a secured server behind a corporate firewall for protection against unauthorized access from the internet.
-   Configure the firewall on the MID Server to accept no inbound connections other than the ones required for corporate management of the operating system and hardware.
-   The system that hosts the MID Server must be able to access the ServiceNow download site at **install.servicenow.com**.

    **Note:** This URL is to the ServiceNow download site, which is not accessible from this topic.

    The MID Serve host machine must be able to access that site to download the installer package. It contacts **install.servicenow.com** every 60 minutes to see if a newer version is available and if so, it performs an automatic upgrade. A MID Server upgrade also takes place when you upgrade an instance.


