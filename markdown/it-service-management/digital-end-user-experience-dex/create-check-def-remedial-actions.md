---
title: Create a check definition for a custom remedial action
description: Create a check definition and link it to the Agent Client Collector \(ACC\) plugin to enable the ACC agent to run a custom remedial action.
locale: en-US
release: zurich
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-03-11"
reading_time_minutes: 1
breadcrumb: [Creating and executing a PowerShell script-based remedial action, DEX remedial actions, Configure, Digital End-User Experience, IT Service Management]
---

# Create a check definition for a custom remedial action

Create a check definition and link it to the Agent Client Collector \(ACC\) plugin to enable the ACC agent to run a custom remedial action.

## Before you begin

-   [Create an ACC plugin package](create-acc-plugin-structure.md)
-   [Sign and verify the ACC plugin](sign-verify-plugin.md)
-   Upload the signed ACC plugin `tar.gz` file to the ServiceNow instance. For more information, see [Create and edit Agent Client Collector plugins](https://www.servicenow.com/docs/access?context=create-edit-assets&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Configurations** &gt; **Check Definitions**.

2.  Select **New**.

3.  On the form, enter a name for the check definition in the **Name** field.

    For example, custom-script-check.

4.  Select the check type to define how the output is processed after running the check definition.

    1.  In the **Check type** field, select the Lookup using list icon ![](../image/icon-magnifying-glass-blue.png) to navigate to the Check Types page.

    2.  Select the check type from the list.

5.  In the **Command** field, enter the name of the `.rb` script included in the ACC plugin package.

    For example, `custom-script.rb`.

    **Note:** For information about creating a check definition with input parameters, see [Create a check definition](https://www.servicenow.com/docs/access?context=acc-api-check-def&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US).

6.  From the **When to send the check results** drop-down list, select when to send check results.

7.  In the Plugins field, integrate the plugins in the ACC plugin package with the check definition.

    1.  Select the Unlock plugins icon ![](../image/icon-visible-fields.png).

    2.  In the Select target record field, select the Lookup using list icon ![](../image/icon-magnifying-glass-blue.png) and select the plugin or type the plugin names.

        For example, acc-f-commons and acc-dex-custom.

    3.  Select the Lock Plugins icon ![](../image/icon-lock-visible-fields.png).

8.  On the form, fill in the remaining fields.

    For a description of the field values, see [Agent Client Collector check definition page](https://www.servicenow.com/docs/access?context=check-definition-form&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US).

9.  Select **Submit**.


**Parent Topic:**[Creating and executing a PowerShell script-based remedial action](../concept/remedial-actions-ps.md)

