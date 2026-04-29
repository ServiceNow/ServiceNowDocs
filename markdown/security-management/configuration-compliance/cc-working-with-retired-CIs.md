---
title: Working with retired configuration items in Configuration Compliance
description: Decommissioned configuration items \(CIs\) are moved to retired, archived, or deleted state in the Configuration Management Database \(CMDB\). Configuration Compliance contains test results \(TRs\) that are made up of CIs. When the state of a CI is updated to retired, the associated TRs are closed with the substate 'CI decommissioned'.
locale: en-US
release: australia
product: Configuration Compliance
classification: configuration-compliance
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Automatic closing of test results, Use, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Working with retired configuration items in Configuration Compliance

Decommissioned configuration items \(CIs\) are moved to retired, archived, or deleted state in the Configuration Management Database \(CMDB\). Configuration Compliance contains test results \(TRs\) that are made up of CIs. When the state of a CI is updated to retired, the associated TRs are closed with the substate 'CI decommissioned'.

**Note:** Starting with v14.9 of Configuration Compliance, the following terms have been renamed:

|Terminology prior to v14.9|Terminology v14.9 onwards|
|--------------------------|-------------------------|
|Test Result Group|Remediation Task|
|Group Rules|Remediation Task Rules|
|Policy|Test group|

If the CMDB changes the life cycle stage status of a CI to retired, you can choose to automatically close the associated TRs. For more information on automatically closing the associated TRs, see [Automatically close test results related to retired CIs](../task/cc-auto-close-vis.md).

The retired CI is eventually archived or permanently deleted from the CMDB.

Impact of retiring the CIs:

-   **Impact on discovered items:** When the CI is retired, the related DI is marked as 'CI decommissioned'.
-   **Impact on test results:** When the state of a DI is updated to 'CI decommissioned', the associated TR is closed and the Notes section is automatically updated.

    **Note:** The state of a DI is automatically updated to 'CI decommissioned' whenever the life cycle state of a CI is updated. On the other hand, the state of a TR is updated to Closed only when the **sn\_vulc.auto\_close\_test\_results\_linked\_to\_retired\_CIs** property is set to true. For more information on automatically closing the associated TRs, see [Automatically close test results related to retired CIs](../task/cc-auto-close-vis.md).


The scheduled job **Close Test Results for decommissioned CIs** is run daily for the updated DIs. If the auto-close configuration option is enabled for retired CIs, it identifies the DI containing a decommissioned CI, and closes the related TR with the substate 'CI decommissioned'. If all the TRs in a remediation task are closed and their substate is CI decommissioned, the remediation task is also closed with the substate 'Canceled'.

**Note:** If a CI moves back to the original state from the 'Retired' state, the 'Discovered Items' entry is updated as well. TRs are automatically opened when data is ingested again from the scanner.

