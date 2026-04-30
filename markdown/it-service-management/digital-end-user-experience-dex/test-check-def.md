---
title: Test a check definition
description: Test a check definition on an endpoint device to verify that the Agent Client Collector \(ACC\) plugin is linked and the custom remedial action defined in the Powershell script runs successfully.
locale: en-US
release: yokohama
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-03-11"
reading_time_minutes: 1
breadcrumb: [Creating and executing a PowerShell script-based remedial action, DEX remedial actions, Configure, Digital End-User Experience, IT Service Management]
---

# Test a check definition

Test a check definition on an endpoint device to verify that the Agent Client Collector \(ACC\) plugin is linked and the custom remedial action defined in the Powershell script runs successfully.

## Before you begin

Create a check definition and link it to the ACC plugin package. For more information, see [Create a check definition for a custom remedial action](create-check-def-remedial-actions.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Configurations** &gt; **Check Definitions**.

2.  Search for the check definition by the name you provided and select it.

3.  In the Related Links section, select **Test check**.

4.  In the Test Check dialog box, select the Lookup using list icon ![](../image/icon-magnifying-glass-blue.png) in the **Agent** field.

5.  In the Agent Client Collectors page, select the agent from the Name list.

    The agent name is updated in the **Agent** field.

6.  Select **OK**.

    The Test Check dialog box shows the progress of the check and the status after the test is completed.

7.  On the endpoint device, verify that the plugin folder is downloaded.

8.  Review the Test Check status to confirm that the remedial action defined in the Powershell script is successfully executed.


