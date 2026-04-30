---
title: Automatically close test results related to retired CIs
description: If the Configuration Management Database \(CMDB\) changes the life cycle stage status of a configuration item \(CI\) to retired, you can choose to automatically close the associated test results \(TRs\).
locale: en-US
release: xanadu
product: Configuration Compliance
classification: configuration-compliance
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Automatic closing of test results, Configuration Compliance remediation, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Automatically close test results related to retired CIs

If the Configuration Management Database \(CMDB\) changes the life cycle stage status of a configuration item \(CI\) to retired, you can choose to automatically close the associated test results \(TRs\).

## Before you begin

Role required: sn\_vulc.admin

## About this task

To automatically close the associated TRs, you must enable the system property **sn\_vulc.auto\_close\_test\_results\_linked\_to\_retired\_CIs** to auto-close TRs that are associated with retired CIs. If this option is enabled, new and existing TRs reported for the same CI, are automatically created or updated in the 'Closed' state. These are based on the Asset ID in the scanner payload and Discovered Items entry status. For more information on the impact of retired CIs, see [Working with retired configuration items in Configuration Compliance](../concept/cc-working-with-retired-CIs.md).

**Note:** The state of a DI is updated to 'CI decommissioned' whenever the life cycle state of a CI is updated. On the other hand, the state of a TR is updated to Closed only when the **sn\_vulc.auto\_close\_test\_results\_linked\_to\_retired\_CIs** system property is enabled.

## Procedure

1.  Navigate to **System properties** &gt; **All properties** and filter by **sn\_vulc.auto\_close\_test\_results\_linked\_to\_retired\_CIs** in the Name column.

2.  Select the property.

3.  To automatically close test results associated with the retired CIs, set the value of the property to true.


**Parent Topic:**[Automatic closing of test results](../concept/cc-auto-close-common.md)

