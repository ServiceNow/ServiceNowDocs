---
title: Scan configuration
description: Scan configuration defines the various settings for the Cloud Configuration Governance scan.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Using Cloud Configuration Governance, Cloud Configuration Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Scan configuration

Scan configuration defines the various settings for the Cloud Configuration Governance scan.

When you execute a scan configuration, Cloud Configuration Governance identifies the targeted cloud resource types from the policy sets attached with the scan configuration. Then, it invokes the respective resource collectors and configuration collectors to import the configuration data of the targeted resource types. After completing the configuration data import, Cloud Configuration Governance compares the imported configuration data against the non-compliant configurations defined in the policies. If Cloud Configuration Governance detects a match, it reports a violation in the audit violation report.

You can reduce the amount of configuration data imported into the system by specifying a set of service account-datacenter combinations for the scan configuration. If specified, Cloud Configuration Governance imports the data from the specified service account-datacenter combinations only. In addition, you can also use tag-based cloud resource filters to identify the cloud resources whose configuration data must be imported for the scan.

For more information on creating scan configuration, see [Create a scan configuration](../task/create-ccg-scan-configuration.md).

