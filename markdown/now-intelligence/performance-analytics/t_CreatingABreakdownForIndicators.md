---
title: Create an automated breakdown
description: To create an automated breakdown, select a breakdown source for it to use and apply access restrictions. Then map which field on the indicator source references the breakdown source. Finally, assign indicators to the breakdown.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/performance-analytics/t\_CreatingABreakdownForIndicators.html
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Automated breakdowns, Indicator breakdowns, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Create an automated breakdown

To create an automated breakdown, select a breakdown source for it to use and apply access restrictions. Then map which field on the indicator source references the breakdown source. Finally, assign indicators to the breakdown.

## Before you begin

Familiarize yourself with the definitions and uses of [breakdowns in general](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/c_CreatingBreakdowns.md) and [automated breakdowns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/automated-breakdowns.md) in particular.

Role required: pa\_data\_collector, pa\_power\_user, pa\_admin, or admin

## About this task

An automated breakdown uses a breakdown source to determine selectable elements. You can use an existing breakdown source or you can define a new one.

**Note:** This process allows you to create a fully customized breakdown. To create a simple automated breakdown, see [Create a breakdown from a wizard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/t_CreateBreakdownFromWizard.md).

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics Administration** &gt; **Breakdowns** &gt; **Automated Breakdowns** and select **New**.

2.  Specify a meaningful **Name**.

    The name of a breakdown is frequently based on the label of the field that is used in the breakdown mappings.

3.  In the **Automated** tab, select the **Breakdown source**.

4.  Select a **Default elements filter**.

    Use element filters to restrict the elements that are visible to a user. For more information, see [Element filters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/c_BreakdownElementFilters.md).

5.  In the **Access control** tab, set who can see the breakdown.

    These restrictions apply in all cases: seeing the breakdown in the list of breakdowns, seeing the breakdown in an Analytics Hub or dashboard, or using the breakdown when creating a widget.

    |Value of Visible to|Further settings|
    |-------------------|----------------|
    |**Everyone \(default\)**|You can restrict visibility by roles. Unselect **Visible by all roles** and select the **Roles** that are required to access the breakdown.|
    |**Groups and Users**|Select the **Groups** and individual **Users** who can access this breakdown. You can select groups or users from a list, and you can select users by email address.|


## What to do next

Create breakdown mappings and associate indicators with the breakdown. You can do this from the indicator, using a graphical tool \(see [Assign and map breakdowns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/create-breakdown-mapping.md).

**Parent Topic:**[Automated breakdowns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/automated-breakdowns.md)

**Previous topic:**[Automated breakdowns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/automated-breakdowns.md)

**Next topic:**[Create a breakdown mapping on a breakdown record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/t_CrtBkdnBreakdownMpngs.md)

