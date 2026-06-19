---
title: Create a check definition for a custom remedial action
description: Create a check definition and link it to the Agent Client Collector \(ACC\) plugin to enable the ACC agent to run a custom remedial action.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/digital-end-user-experience-dex/create-check-def-remedial-actions.html
release: australia
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

-   [Create an ACC plugin package](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/create-acc-plugin-structure.md)
-   [Sign and verify the ACC plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/sign-verify-plugin.md)
-   Upload the signed ACC plugin `tar.gz` file to the ServiceNow instance. For more information, see .

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Configurations** &gt; **Check Definitions**.

2.  Select **New**.

3.  On the form, enter a name for the check definition in the **Name** field.

    For example, custom-script-check.

4.  Select the check type to define how the output is processed after running the check definition.

    1.  In the **Check type** field, select the Lookup using list icon \[Omitted image "icon-magnifying-glass-blue.png"\] Alt text: to navigate to the Check Types page.

    2.  Select the check type from the list.

5.  In the **Command** field, enter the name of the `.rb` script included in the ACC plugin package.

    For example, `custom-script.rb`.

    **Note:** For information about creating a check definition with input parameters, see .

6.  From the **When to send the check results** drop-down list, select when to send check results.

7.  In the Plugins field, integrate the plugins in the ACC plugin package with the check definition.

    1.  Select the Unlock plugins icon \[Omitted image "icon-visible-fields.png"\] Alt text:.

    2.  In the Select target record field, select the Lookup using list icon \[Omitted image "icon-magnifying-glass-blue.png"\] Alt text: and select the plugin or type the plugin names.

        For example, acc-f-commons and acc-dex-custom.

    3.  Select the Lock Plugins icon \[Omitted image "icon-lock-visible-fields.png"\] Alt text:.

8.  On the form, fill in the remaining fields.

    For a description of the field values, see .

9.  Select **Submit**.


**Parent Topic:**[Creating and executing a PowerShell script-based remedial action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/remedial-actions-ps.md)

