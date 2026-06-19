---
title: Operating system security
description: Learn how the MID Server stores its ServiceNow AI Platform username and password in its configuration file, named config.xml, for secure authentication to the instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/servicenow-ai-platform-security/operating-system-security.html
release: zurich
product: ServiceNow AI Platform Security
classification: servicenow-ai-platform-security
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
---

# Operating system security

Learn how the MID Server stores its ServiceNow AI Platform username and password in its configuration file, named `config.xml`, for secure authentication to the instance.

The MID Server must be deployed in a secure and hardened operating system for protection against unauthorized access to the credentials:

-   Limit the access to the operating system to a few, trusted administrators.
-   Monitor the operating system logs to detect any unauthorized access, particularly attempts to access the config.xml file, as this file contains important MID Server configuration information.
-   Install operating system security patches regularly with the latest anti-virus software and update AV definitions regularly.
-   The MID Server requires a current Java framework to run. Keep Java updated regularly.
-   Remove or disable unnecessary services and applications.
-   Install an OS firewall to limit access to unauthorized ports.
-   Follow the security guidelines published in the operating system hardening guides from the vendors.

