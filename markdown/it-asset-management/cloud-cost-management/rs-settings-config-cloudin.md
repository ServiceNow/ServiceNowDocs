---
title: Configure Rightsizing operations
description: Configure Rightsizing processes and specify the amount of potential rightsizing savings that triggers notifications.
locale: en-US
release: australia
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Resize resources with Rightsizing, Using Cloud Cost Management, Cloud Cost Management, IT Asset Management]
---

# Configure Rightsizing operations

Configure Rightsizing processes and specify the amount of potential rightsizing savings that triggers notifications.

## Before you begin

Run Discovery on each service account.

Ensure that the Billing Download job has completed for each provider.

Ensure that the Price Sheet Download job has completed for each provider.

Role required: insights\_admin or insights\_owner

## Procedure

1.  Navigate to **Cloud Cost Management Workspace** &gt; **Operations** &gt; **Recommendations** &gt; **Rightsizing**.

2.  Select **Settings**.

3.  On the form, fill in the fields.

<table id="table_qnq_v3t_tgb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Enable Rightsizing

</td><td>

Option for enabling Rightsizing activities. Clearing the check box disables Rightsizing.Default: Enabled

 This field is automatically enabled.

</td></tr><tr><td>

After resize, exclude resource for \(days\)

</td><td>

Number of days to place a resized resource in the Excluded Resources list. During this monitoring period, you can’t remove the resource from the Excluded Resources list.

 Cloud Cost Management monitors resized resources for the specified period to verify that the new size is appropriate. When the period expires, the resource is removed from the list and rightsizing analysis resumes.

 **Note:** Microsoft Azure only: The Azure Advisor service begins to analyze usage and may again recommend resizing after seven days regardless of this setting. If you specify a value greater than seven days, the Cloud Cost Management doesn’t report the Azure Advisor recommendation for the time period that you specify.

 Minimum value: 7

</td></tr><tr><td>

Do not recommend if savings are below threshold

</td><td>

Minimum cost over a 30-day period to use when deciding whether to rightsize. For example, a setting of ¥100 means that Cloud Cost Management ignores any rightsizing recommendation that would result in less than ¥100 in savings over 30 days.

</td></tr><tr><td>

Notify when potential rightsizing savings exceed \(%\) of total spend

</td><td>

Percentage of overall cloud spend for resources that are sized incorrectly that should trigger an email notification to the users or groups that you specify.The value is calculated using the amount that could be saved if all rightsizing recommendations are followed.

Default: 15%

The default value of **15** means that notifications are sent only when the cost of non-rightsized resources is greater than 15% of total costs.

</td></tr><tr><td>

Notify users / Notify groups

</td><td>

Users or groups to notify by email when the spend for incorrectly sized resources exceeds the specified percentage of overall cloud spend. For information on configuring the email, see [Create an email template](https://www.servicenow.com/docs/access?context=t_CreateAnEmailTemplate&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

Advanced

</td><td>

Option for specifying non-default change templates for generating change requests.

</td></tr><tr class="sub-head"><td>

Auto-approval \(Standard Change\)

</td><td>

 

</td></tr><tr><td>

Script include

</td><td>

This field appears only when the **Advanced** check box is selected.

`CLINRSStandardChangeRequestUtil`: The Change group is derived from the Standard Change template and can’t be overridden.

</td></tr><tr class="sub-head"><td>

Manual Approval \(Normal Change\)

</td><td>

 

</td></tr><tr><td>

Script include

</td><td>

This field appears only when the **Advanced** check box is selected.

`CLINRSNormalChangeRequestUtil`: Manual approval or Normal Change policies.

</td></tr></tbody>
</table>4.  Select **Save**.


-   **[Specify rate discounts to enable accurate pricing for Rightsizing recommendations](discounts-specify-cloudin.md)**  
To generate an accurate Rightsizing recommendation, the system analyzes usage data for the last 14 days, obtains prices from the price sheet data tables, and then applies appropriate discounts. To enable the calculations, specify the provider's discount rate for each service account.
-   **[Define a metric threshold](define-metric-threshold.md)**  
To enable accurate memory usage data for use in generating Rightsizing recommendations, you first define memory metrics in your account. You then define a custom memory metric in Cloud Cost Management.

**Parent Topic:**[Resize resources with Rightsizing](../concept/resize-res-ci.md)

