---
title: Post-discovery phase
description: Following the discovery phase, the system manages TLS certificates, offering flexibility for both manual and automated request options, catering to various certificate-related tasks and processes.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2025-08-18"
reading_time_minutes: 1
breadcrumb: [Certificate Inventory and Management process flow, Exploring Certificate Inventory and Management, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Post-discovery phase

Following the discovery phase, the system manages TLS certificates, offering flexibility for both manual and automated request options, catering to various certificate-related tasks and processes.

The TLS certificate chains, signed by the certificate authority and root, populate the Unique Certificate \[cmdb\_ci\_certificate\] and Installed Certificate \[sn\_disco\_certmgmt\_cmdb\_installed\_certificate\] tables. Subsequently, a scheduled job reviews the Unique Certificate table for expiring and expired certificates, initiating the creation and assignment of certificate tasks and incidents.

You have the option to manually request new certificates and renew existing ones. For more information, see [Manual flow for certificate requests](manual-cert-requests.md).

In Version 1.3.8, the capability to automate requests for new certificates, renewals, or revoking certificates has been introduced. For more information, see [Automated certificate management for TLS certificates](automated-cert-requests.md).

To optimize system performance, a table cleaner automatically removes old certificate records from these two tables after a specified number of days:

-   Discovered Certificate \[sn\_disco\_certmgmt\_certificate\_history\] table: older than 30 days
-   Installed Certificate \[sn\_disco\_certmgmt\_cmdb\_installed\_certificate\] table: older than 90 days

**Note:** You can toggle various behaviors related to Certificate Inventory and Management depending on your needs, using specific certificate properties as shown in [Discovery properties](../reference/r_DiscoveryProperties.md) and [System properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

The system scans for certificates that are expired or archived for more than six months. If a replacement certificate exists, the system removes outstanding tasks for these obsolete certificates.

The same six-month grace period applies for expired and archived certificates and certificate tasks in the **failed** state.

