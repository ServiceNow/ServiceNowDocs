---
title: Certificate Inventory and Management process flow
description: Certificate Inventory and Management allows Discovery to automatically scan for certificates on specific ports through your existing CI-based Discovery schedules. In addition, you can create new Discovery schedules to scan individual URLs.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Exploring Certificate Inventory and Management, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Certificate Inventory and Management process flow

Certificate Inventory and Management allows Discovery to automatically scan for certificates on specific ports through your existing CI-based Discovery schedules. In addition, you can create new Discovery schedules to scan individual URLs.

## How Certificate Inventory and Management works

In Version 1.1.7 Certificate Inventory and Management, you can also scan for certificate authorities \(CA\) and import certificates from files.

With the Australia release, you can download Version 1.2.0 Certificate Inventory and Management. You can discover certificates used in the HTTP\(s\) Endpoint \[cmdb\_ci\_endpoint\_http\] table and bulk import a list of SSL Certificates. You can create events and alerts for expiring and expired certificates and be notified in Slack of expiring and expired certificates.

## Process flow diagram

![Workflow of Certificate Inventory and Management](../image/cert_mgmt_flow_v2.png)

The Certificate Inventory and Management process flow is segmented into two distinct phases:

-   [Pre-discovery phase](cert-inventory-mgmt-process-pre-discovery.md): The initial segment of the process varies based on the source of certificate discovery. This phase focuses on actions required for identifying certificates from different sources within the IT infrastructure.
-   [Post-discovery phase](cert-inventory-mgmt-process-post-discovery.md): This phase involves subsequent actions taken after the certificates have been successfully discovered. It includes processes such as cataloging, tracking, and managing certificates to ensure their secure and efficient integration into the system.

