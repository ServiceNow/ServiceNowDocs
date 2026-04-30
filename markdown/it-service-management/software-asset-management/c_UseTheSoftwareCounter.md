---
title: Use a software counter for the legacy Software Asset Management plugin
description: Use a software counter for the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin to count the licenses for a specific version of software and receive summary or detailed results.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Software license reconciliation counters for the legacy Software Asset Management plugin, Legacy Software Asset Management plugin, ITSM Software Asset Management, Asset Management, IT Service Management]
---

# Use a software counter for the legacy Software Asset Management plugin

Use a software counter for the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin to count the licenses for a specific version of software and receive summary or detailed results.

When a software counter runs for the first time, it can take several minutes to process records. The license counts are cached so that on subsequent runs, the counter processes only changed records, both those from Discovery or altered entitlements, making it faster. The Software Counter form contains check boxes to enable faster counting through the use of quick counters. For more information on using quick counters, see [Setting Up Quick Counters](c_SetUpQuickCounters.md).

Use a software counter to count the licenses for a specific version of software and receive summary or detailed results. For example, an asset manager can look at summary information to discover which departments are not in compliance. Then, department managers can look at detailed information to determine the people or individual computers that are not in compliance.

Software counters return results by Licensing Type:

-   Entitled in use: Number of people who have been allocated a license and installed the software.
-   Entitled not in use: Number of people who have been allocated a license but did not install the software.
-   Not entitled: Number of people using an unauthorized copy of the software.
-   Not allocated: Number of licenses not assigned.

**Note:** For information about the scheduled job that runs all counters each day or the steps to run all counters manually, see [Scheduling Software Counts](../task/t_ScheduleASoftwareCount.md).

The Software Counters list is color coded:

-   Green - in compliance
-   Orange - within 5% of being out of compliance
-   Red - not compliant

![SAM software license compliance check](../image/SAMSoftwareLicComplianceCheck.png "SAM software license compliance check")

**Parent Topic:**[Software license reconciliation counters for the legacy Software Asset Management plugin](c_UseCountersSWLicenseReconcil.md)

