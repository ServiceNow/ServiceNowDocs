---
title: VirusTotal integration setup
description: VirusTotal is a free service that analyzes suspicious files and URLs and facilitates the quick detection of viruses, worms, trojans, and all kinds of malware. It integrates easily with Security Operations.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [VirusTotal integration, Threat Intelligence integrations, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# VirusTotal integration setup

VirusTotal is a free service that analyzes suspicious files and URLs and facilitates the quick detection of viruses, worms, trojans, and all kinds of malware. It integrates easily with Security Operations.

Before you can use the VirusTotal integration, you must activate the plugin and add the appropriate API key. If necessary, you can also update your X509 SSL certification.

If the VirusTotal lookup source is used and malware is encountered, an observable is created. For IP lookups, an additional list of URLs that share the IP address is created, and observables are created for each of the URLs.

**Note:**

-   The Threat Intelligence plugin is required in order to implement VirusTotal integration.
-   The VirusTotal integration has been upgraded to Version 3 APIs.

