---
title: Create an indicator group
description: For convenience, you can organize related indicators into an indicator group. When you configure some visualizations that show multiple indicators, you can specify an indicator group instead of individual indicators.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/performance-analytics/t\_CreatingIndicatorGroups.html
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Indicators, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Create an indicator group

For convenience, you can organize related indicators into an indicator group. When you configure some visualizations that show multiple indicators, you can specify an indicator group instead of individual indicators.

## Before you begin

Role required: pa\_admin, pa\_power\_user, or admin

## About this task

By creating indicator groups, you can organize indicators along whatever themes are most useful to you. The indicators do not have to be of the same type or share an indicator source or data collector job. Indicator groups save you the trouble of specifying multiple individual indicators when you configure the following objects:

-   List widgets
-   Time series widgets with the relative compare visualization
-   Email notifications about indicators
-   Security Incident Analytics treemaps

After you create an indicator group, you can add indicators to the group or remove them from the group. This change propagates to all objects that use the indicator group, so you do not need to edit the configurations of the objects.

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics Administration** &gt; **Indicators** &gt; **Indicator Groups**.

2.  Select **New**.

3.  Enter a **Label** for the indicator group.

4.  Open the Additional actions menu \(\[Omitted image "additional-actions.png"\] Alt text: Additional actions menu icon\) and click **Save**.

    The Indicators related list appears.

5.  Select **Edit** on the Indicators related list and add indicators to the group.

6.  Select **Save** to finish adding indicators, then **Update** to exit the Indicator Group record.


## Creating and using the 'Open and Resolved Incidents' indicator group

In this example, create an indicator group with all the indicators that refer to either open or resolved incidents. The incidents are all included with the demo data for Performance Analytics. After creating the indicator group, create a list widget that uses the indicator group and add the widget to a dashboard.

1.  First, go to **Performance Analytics** &gt; **Indicator Groups** and click **New**. An empty Indicator Group form opens.
2.  Give the indicator group the label `Open and Resolved Incidents`, and save the form from the Additional actions menu.

    \[Omitted image "indicator-group-save.png"\] Alt text: Naming and saving a new indicator group

    The Indicators related list appears at the bottom of the record.\[Omitted image "indicator-group-new-saved.png"\] Alt text: Newly created indicator group with no indicators

3.  Click **Edit**, which opens the Edit Members dialog. To group all the indicators that involve resolved or open incidents, add all the indicators with 'resolved' or 'open' in their name. Also add the Incident backlog growth indicator.

    \[Omitted image "indicator-group-edit-members.png"\] Alt text: Indicator group Edit Members dialog showing indicators being added

4.  The indicator group is complete. Click **Save** in the Edit Members dialog and then **Update** on the indicator group record.
5.  Now create a Performance Analytics List widget and specify the Open and Resolved Incidents indicator group.

    \[Omitted image "indicator-group-widget.png"\] Alt text: New widget form for a list widget with the Open and Resolved Incidents indicator group

6.  To share the widget with other users, add it to the Incident Management dashboard.\[Omitted image "incident-group-dashboard.png"\] Alt text: Incident Management dashboard showing the list widget with the Open and Resolved Incidents indicator group

**Related topics**  


[List widgets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/list-widgets.md)

[Create a relative compare visualization for a time series widget](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/create-relative-compare-ts.md)

[Create an email notification for indicators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/t_CreateEmailSummaries.md)

[bundle-security.t_DfnSvcImpctTmapDmn]

