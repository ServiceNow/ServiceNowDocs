---
title: Set up quick counters for the legacy Software Asset Management plugin
description: Quick counter settings can help speed up the software counting process that is used by the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Software license reconciliation counters for the legacy Software Asset Management plugin, Legacy Software Asset Management plugin, ITSM Software Asset Management, Asset Management, IT Service Management]
---

# Set up quick counters for the legacy Software Asset Management plugin

Quick counter settings can help speed up the software counting process that is used by the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin.

The following check boxes are available in the Parameters section of the Software Counter form:

-   Verify entitlements: When this check box is selected, the software counter will generate entitlement details in the software counter summaries, displaying the number of entitlements in use and entitlements not in use. If the check box is cleared, the software counter will display Entitlement not known with a count of total installs. The counter will not check for entitlements.
-   Generate details: When this check box is selected, the software counter will generate [software counter details](../task/t_ViewSoftwareCounterDetail.md)for each software counter result type. If the check box is cleared, no details will be available.

Clearing these check boxes in addition to setting the Grouping parameter to None will enable software counters to run more quickly.

**Parent Topic:**[Software license reconciliation counters for the legacy Software Asset Management plugin](c_UseCountersSWLicenseReconcil.md)

