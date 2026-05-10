---
title: Reduce resource cost with Reservation Plans
description: View the Reserved Instances \(RI\) report, implement recommendations, and configure processes to convert on-demand payment plans to reservation plans, and save the cost of your resources.Configure Reservation/Saving plans processes and specify the amount of potential savings that triggers notifications.
locale: en-US
release: australia
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Using Cloud Cost Management, Cloud Cost Management, IT Asset Management]
---

# Reduce resource cost with Reservation Plans

View the Reserved Instances \(RI\) report, implement recommendations, and configure processes to convert on-demand payment plans to reservation plans, and save the cost of your resources.

You can filter by payment option, term, and look back period to view specific results for the Reserved Instances report.

![Reservation/Saving plans in Operations view.](../image/reservation-ws.png)

|Chart|Description|
|-----|-----------|
|Upfront cost to reserve|Upfront cost if all Reservation/Saving plans recommendations were applied.|
|Overall RI utilization percentage|Percentage of resources on reservation plans that were used and that weren’t used in the last 30-day period.|
|Potential savings by service category|Monthly savings to expect when all Reservation/Saving plan recommendations are applied.|

<table id="table_jrn_f2d_qxb"><thead><tr><th>

Recommendation tab

</th><th>

Description

</th><th>

Available selections on selected recommendations

</th></tr></thead><tbody><tr><td>

New

</td><td>

Resources that would benefit most in reservation plans. Review the list and decide the conversion to reservation plans. You can perform conversion by moving a resource to one of the other tabs by selecting the appropriate action.

</td><td>

-   Accept
-   Decline

</td></tr><tr><td>

Accepted

</td><td>

Resources that are converted to reservation plans. After a resource is moved to the **Accepted Recommendations** tab, it won't reappear on the **New Recommendations** tab.

</td><td>

Decline

</td></tr><tr><td>

Declined

</td><td>

Resources that aren’t converted to reservation plans. After a resource is moved to the **Declined Recommendations** tab, it won't reappear on the **New Recommendations** tab.

</td><td>

Accept

</td></tr></tbody>
</table>**Important:** When you move a resource to the **Accepted Recommendations** or **Declined Recommendations** tab, the Cloud Cost Management application doesn't perform any action. You can change payment plans on the provider management interface.

Google Cloud recommendations are updated periodically and might not show the latest suggestions until the console is manually refreshed. In contrast, Cloud Cost Management fetches recommendations via API, ensuring it has the most current data. This difference can sometimes cause Google Cloud RI recommendations in Cloud Cost Management to diverge from what's shown in the Google Cloud console. A manual refresh is required to see the latest recommendations.

You can also [configure Reservation/Saving plans operations](reserve-plan-using.md#) by selecting **Settings**.

**Parent Topic:**[Using Cloud Cost Management](using-cloud-insights.md)

## Configure Reservation/Saving plans operations

Configure Reservation/Saving plans processes and specify the amount of potential savings that triggers notifications.

### Before you begin

Run Discovery on each service account.

Ensure that the Billing Download job has completed for each provider.

Role required: insights\_admin and insights\_owner

### Procedure

1.  Navigate to **Cloud Cost Management Workspace** &gt; **Operations** &gt; **Recommendations** &gt; **Reservation/Saving plans**.

2.  On the Reserved Instances page, select **Settings**.

3.  On the form, fill in the fields:

<table id="table_qnq_v3t_tgb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enable Reserved Instance

</td><td>

Option for enabling Reserved Instance activities. Clearing the check box disables Reservation/Saving plans operations.

 Default: Enabled

</td></tr><tr><td>

Notify when potential reserved instance savings exceed \(%\) of total spends

</td><td>

Percentage of overall cloud spends for potential savings on reserved savings that should trigger an email notification to the users or groups that you specify.

 The value is calculated using the amount that could be saved if all the Reservation/Saving plans recommendations are followed.

 The default value of **15** means that notifications are sent only when the savings for potential reserved instances are greater than 15% of total costs.

</td></tr><tr><td>

Do not recommend if savings are below threshold

</td><td>

Minimum cost, as calculated over the Lookback period, to use when deciding whether to recommend a Reservation/Saving plan for a resource.

 For example, a setting of ¥100 means that the app should ignore any Reservation/Saving plan recommendation that would result in less than ¥100 in savings.

</td></tr><tr><td>

Notify groups/Notify users

</td><td>

Users or groups to notify by email when the spend for potential reserved instance savings exceed the specified percentage of overall cloud spend. For information on configuring the email, see [Create an email template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_CreateAnEmailTemplate.md).

</td></tr><tr><td class="sub-head" colspan="2">

**Default Filter Settings**

</td></tr><tr><td>

Payment option

</td><td>

Sets the selected payment option as the default filter on the Reservation/Savings Plan page.

</td></tr><tr><td>

Term

</td><td>

Sets the selected term as the default filter on the Reservation/Savings Plan page.

</td></tr><tr><td>

Look back period

</td><td>

Sets the selected look back period as the default filter on the Reservation/Savings Plan page.

</td></tr></tbody>
</table>4.  Select **Save**.


### What to do next

To view the changes, rerun the Billing Download job.

