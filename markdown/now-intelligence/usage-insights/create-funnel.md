---
title: Create a funnel report
description: View conversion rates and trends in aggregate user behavior to uncover the reasons behind success or failure of a specific in-application user goal. Investigating a conversion funnel can help you measure and optimize the conversion rates of relevant processes within your application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/now-intelligence/usage-insights/create-funnel.html
release: xanadu
product: Usage Insights
classification: usage-insights
topic_type: task
last_updated: "2024-12-18"
reading_time_minutes: 2
breadcrumb: [Funnel reports in User Experience Analytics, Using User Experience Analytics, User Experience Analytics, Platform Analytics]
---

# Create a funnel report

View conversion rates and trends in aggregate user behavior to uncover the reasons behind success or failure of a specific in-application user goal. Investigating a conversion funnel can help you measure and optimize the conversion rates of relevant processes within your application.

## Before you begin

Role required: Users with the analytics\_viewer, portal\_analytics\_viewer, mobile\_analytics\_viewer, core\_ui\_analytics\_viewer, now\_experience\_analytics\_viewer roles can create, edit and delete funnels for the applications they have access to.

## Procedure

1.  Navigate to **All** &gt; **User Experience Analytics** &gt; **Dashboard** and select an application.

2.  From the Dashboard, select the funnels icon \(\[Omitted image "icon-uxa-funnel.png"\]\) and select **Create Your First Funnel** or **New Funnel**.

3.  Enter a name for the relevant process you want to measure.

4.  Choose the time frame for sessions you want to include and select **Next**.

<table id="choicetable_rqr_3zv_xjb"><tbody><tr><td id="d72345e96">

**Now**

</td><td>

The report begins collecting data from the second the report is saved.

</td></tr><tr><td id="d72345e108">

**1 Week Ago**

</td><td>

Reports on data seven days prior to the current date. Includes data generated at 12AM GMT of the date.

</td></tr><tr><td id="d72345e120">

**1 Month Ago**

</td><td>

Reports on data 30 days prior to the current date. Includes data generated at 12AM GMT of the date.

</td></tr><tr><td id="d72345e132">

**3 Months Ago**

</td><td>

Reports on data 90 days prior to the current date. Includes data generated at 12AM GMT of the date.

</td></tr><tr><td id="d72345e144">

**Original Date**

</td><td>

This option is available when editing an existing report. Reports on data from the original date of the report.

</td></tr></tbody>
</table>5.  From the **Step Type** options, select steps you want to measure, and screens, events, or actions as applicable.

<table id="choicetable_fsr_qbg_wjb"><tbody><tr><td id="d72345e168">

**Event Trigger**

</td><td>

Select [User Analytics Events KPIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/now-intelligence/usage-insights/view-events.md) to measure. To match a selected event by a certain property, click **Match by properties**, select a property from the drop down, and enter a value for the property.

</td></tr><tr><td id="d72345e190">

**Screen Action**

</td><td>

Select a screen and applicable action type.

</td></tr><tr><td id="d72345e199">

**Page View**

</td><td>

Select a page.

</td></tr><tr><td id="d72345e208">

**Screen View**

</td><td>

Select a screen. \(Mobile only.\)

</td></tr><tr><td id="d72345e217">

**Session Start \(1st\)**

</td><td>

Select to measure users' first sessions.

</td></tr><tr><td id="d72345e227">

**Session Start \(any\)**

</td><td>

Select to measure any user sessions.

</td></tr></tbody>
</table>6.  Choose an **Event Name** and select **Add**.

7.  If applicable, add an alternative step type that users might choose at that point in the path.

8.  Select any additional steps to add to the funnel.

    \[Omitted image "funnel-wizard-w.png"\] Alt text: Create funnel wizard

9.  Select **Finish**.


**Parent Topic:**[Funnel reports in User Experience Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/now-intelligence/usage-insights/funnel-reports-uxa.md)

