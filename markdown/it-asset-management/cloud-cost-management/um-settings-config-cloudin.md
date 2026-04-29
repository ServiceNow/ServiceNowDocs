---
title: Configure Unused resources operations
description: The Unused resources feature recommends termination or power-off for resources that are wasting money because they aren’t being used. Configure Unused resources processes and specify the potential savings that trigger notifications.
locale: en-US
release: australia
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Manage unused resources, Using Cloud Cost Management, Cloud Cost Management, IT Asset Management]
---

# Configure Unused resources operations

The Unused resources feature recommends termination or power-off for resources that are wasting money because they aren’t being used. Configure Unused resources processes and specify the potential savings that trigger notifications.

## Before you begin

Run Discovery on each service account.

Ensure that the Billing Download job has completed for each provider.

Ensure that the Price Sheet Download job has completed for each provider.

Role required: insights\_admin \[sn\_clin\_core.insights\_admin\] or insights\_owner \[sn\_clin\_core.insights\_owner\].

## About this task

**Note:** Microsoft Azure only: The Azure Advisor service generates the recommendations that appear in Rightsizing and Unused resources reports. Cloud Cost Management doesn't generate the recommendations.

## Procedure

1.  Navigate to **Cloud Cost Management Workspace** &gt; **Operations** &gt; **Recommendations** &gt; **Unused resources**.

2.  Select **Settings**.

3.  On the form, fill in the fields.

<table id="table_qnq_v3t_tgb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Enable Unused Machines

</td><td>

Option for enabling Unused resources activities.

 This field is automatically enabled.

</td></tr><tr><td>

Advanced

</td><td>

Option to specify non-default change templates.

</td></tr><tr><td>

Auto pause interval

</td><td>

Indicates the minimum idle time for the Azure SQL database in minutes.

 Default: 60 minutes

</td></tr><tr><td>

Maximum age for snapshots in AWS/Azure/Google \(days\)

</td><td>

Age of the snapshot. The snapshot data is displayed in the **Rationale** column in the **Recommendations** tab.Default: 90 days

</td></tr><tr><td>

Notify when potential unused savings exceed \(%\) of total spend

</td><td>

Percentage of overall cloud spend on unused resources that triggers an email notification to the users or groups that you specify.The value is calculated using the amount that could be saved if all Unused resources recommendations are applied.

Default: 15%

The default value of 15 means that notifications are sent only when the cost of operation for unused resources is greater than 15% of total costs.

</td></tr><tr><td>

Notify users / Notify groups

</td><td>

Users or groups to notify by email when the spend for unused resources exceeds the specified percentage of overall cloud spend.

 For information on configuring the email, see [Create an email template](https://www.servicenow.com/docs/access?context=t_CreateAnEmailTemplate&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td></tr><tr class="sub-head"><td>

Auto-approval \(Standard Change\)

</td><td>

 

</td></tr><tr><td>

Script include

</td><td>

This field appears only when the **Advanced** check box is selected.

`CLINRSStandardChangeRequestUtil`Script include to use for change requests when a resource matches a policy of the specified type. The Change group is derived from the Standard Change template and can’t be overridden.

</td></tr><tr class="sub-head"><td>

Manual approval \(Normal Change\)

</td><td>

 

</td></tr><tr><td>

Script include

</td><td>

This field appears only when the **Advanced** check box is selected.

`CLINRSNormalChangeRequestUtil`

</td></tr></tbody>
</table>4.  Select **Save**.


**Parent Topic:**[Manage unused resources](../concept/manage-unused-mac.md)

**Related topics**  


[Change Management](https://www.servicenow.com/docs/access?context=c_ITILChangeManagement&version=australia&pubname=australia-it-service-management&ft:locale=en-US)

