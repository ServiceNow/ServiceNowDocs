---
title: Configure update set scanning properties
description: The Scan Engine provides several options to further configure update set scanning and enhance the governance over update set management. Update set scanning occurs during scheduled instance scans and when developers attempt to mark update sets complete.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/update-set-scanning-properties2.html
release: australia
topic_type: task
last_updated: "2026-07-10"
reading_time_minutes: 2
breadcrumb: [Configure Scan Engine parameters, Activate Scan Engine and review settings, Run Impact Guided Setup, Configuring Impact, Impact]
---

# Configure update set scanning properties

The Scan Engine provides several options to further configure update set scanning and enhance the governance over update set management. Update set scanning occurs during scheduled instance scans and when developers attempt to mark update sets complete.

## Before you begin

Update sets are scanned in two scenarios:

-   During scheduled instance scans
-   When a user attempts to mark an update set as Complete

Role required: scan\_engine\_admin

## Procedure

1.  Navigate to **ALL** &gt; **Impact** &gt; **Configuration** &gt; **Scan Engine Properties**.

2.  Select the **Update Sets** tab.

3.  Configure the update set scanning condition using the condition builder.

    These conditions determine which update sets to scan. By default, conditions filter out non-active and default update sets.

4.  Select the **Enforce update set validation** check box to require update sets to meet completion conditions.

    When enabled, update sets must meet the conditions specified in the **Conditions for completing an update set** field.

    When enforcement is enabled, a completion enforcement message appears in the scan modal warning users of requirements to complete the update set. Message content changes based on the scan type and enforcement condition. For example, if a specific suite is required, the message directs the user to select that suite.

    **Warning:** Update sets can't be marked complete until conditions are met.

5.  Configure conditions for completing an update set using the condition builder.

    These conditions determine whether an update set can be marked complete.

6.  Configure additional update set scanning options.

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enable update set summary scan synchronization

</td><td>

Allows update set summary scans to be synced between instances defined in the multi-instance communication API integration.

</td></tr><tr><td>

Table for update set scanning condition

</td><td>

Specifies which table the scan condition builder references. By default, this is the Update Set \[sys\_update\_set\] table and is typically not changed.

</td></tr><tr><td>

Override Environment Check for Update Set Scans

</td><td>

Enables all active definitions to run during update set scans regardless of instance-specific settings. Useful for validating update sets before promoting them to production.

</td></tr><tr><td>

Allow Suite Scan for update sets

</td><td>

-   When selected, developers can choose between Full scan and Suite scan.
    -   Suite Scan runs only selected definitions for faster validation.
    -   Full Scan runs all active definitions for comprehensive validation.
-   When cleared, only Full scans are available.
-   If completion enforcement is enabled and requires a specific suite, users must select that suite from the dropdown to meet the completion condition. For example, if the condition requires the Scan Engine suite, users must select Scan Engine from the suite list.


</td></tr></tbody>
</table>7.  Select **Save**.


**Parent Topic:**[Configure Scan Engine parameters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/configure-scan-engine-properties.md)

**Related topics**  


[Customize Scan Engine definition suites](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/create-scan-engine-definition-suites.md)

[Configure application scanning properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/configure-application-scanning-properties.md)

[Initiate update set scans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/initiate-update-set-scans.md)

