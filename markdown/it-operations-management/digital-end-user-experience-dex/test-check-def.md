---
title: Test a check definition
description: Test a check definition on an endpoint device to verify that the Agent Client Collector \(ACC\) plugin is linked and the custom remedial action defined in the script runs successfully.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/digital-end-user-experience-dex/test-check-def.html
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-10-23"
reading_time_minutes: 1
keywords: [test check definition, check definition, acc plugin test, powershell remedial action, verify remedial action]
breadcrumb: [Creating a PowerShell remedial action, Creating DEX remedial actions, Configure, Digital End-User Experience, IT Operations Management]
---

# Test a check definition

Test a check definition on an endpoint device to verify that the Agent Client Collector \(ACC\) plugin is linked and the custom remedial action defined in the script runs successfully.

## Before you begin

A check definition must be created and linked to the ACC plugin package. For more information, see [Create a check definition for a custom remedial action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/create-check-def-remedial-actions.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Configurations** &gt; **Check Definitions**.

2.  Search for the check definition by the name you provided and select it.

3.  In the Related Links section, select **Test check**.

4.  In the Test Check dialog box, select the Lookup using list icon \[Omitted image "icon-magnifying-glass-blue.png"\] Alt text: in the **Agent** field.

5.  On the Agent Client Collectors page, select the agent from the Name list.

    The agent name is updated in the **Agent** field.

6.  Select **OK**.

    The Test Check dialog box shows the progress of the check and the status after the test is completed.

7.  On the endpoint device, verify that the plugin folder is downloaded.

8.  Review the Test Check status to confirm that the remedial action defined in the PowerShell script is successfully executed.


