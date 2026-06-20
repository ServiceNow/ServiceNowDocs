---
title: Get insights from the Integration Hub Usage Dashboard
description: Use the Integration Hub Usage Dashboard to get insights on the Integration Hub transactions. For example, you can view which protocol was the most used in the transactions in the last year. You can also use filters and customize the layout and arrangement of the columns in the reports.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/integration-hub/use-integrationhub-usage-dashboard.html
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-19"
reading_time_minutes: 3
breadcrumb: [Integration Hub Usage Dashboard, Configure, Integration Hub, Workflow Data Fabric]
---

# Get insights from the Integration Hub Usage Dashboard

Use the Integration Hub Usage Dashboard to get insights on the Integration Hub transactions. For example, you can view which protocol was the most used in the transactions in the last year. You can also use filters and customize the layout and arrangement of the columns in the reports.

## Before you begin

Role required: admin, flow designer, action\_designer, usage\_admin, or flow\_operator

## Procedure

1.  To access the dashboard, navigate to **All** &gt; **IntegrationHub** &gt; **IntegrationHub Usage**.

    **Tip:** Get quicker access by entering **Integrationhub usage** in the filter search field \[Omitted image "filter-search.png"\] Alt text: Filter search field..

2.  To view the reports, select **Spokes** or **Protocols &amp; Features** in the **View by** list.

    \[Omitted image "ihub-dashboard-view-reports.png"\] Alt text: View reports.

    **Note:** There’s no order in which you must view the reports, set the filters, or customize the columns in the report tables. So, you can complete one or more of the following steps in any order. The Transactions tab is selected by default.

3.  To drill down and view more details in a report, select the graph or chart.

4.  To group transactions under a common parameter, do the following actions:

    1.  Drill down the report.

    2.  In the desired column, move the mouse device to the row that contains the parameter and click the group transactions by parameter icon \(\[Omitted image "group-by-icon.png"\] Alt text: Group transactions by parameter icon.\) for the parameter under which you want to group the transactions.

    3.  Click **Show Matching**.

        Alternatively, you can view the following animation by opening this topic on a browser.

        \[Omitted image "group-by.gif"\] Alt text: Group transactions by parameter.

5.  To hide or reveal the slices in a pie chart, do the following actions:

    Each slice in a pie chart represents a transaction usage insight. However, it might be difficult to view certain slices because they’re obscured by fairly bigger slices.

    1.  To hide a slice, click its colored legend.

    2.  To reveal the slice back, click the colored legend again.

    Alternatively, you can view the following animation by opening this topic on a browser.

    \[Omitted image "hide-reveal-pie-slices.gif"\] Alt text: Hide or reveal pie chart slices.

6.  To customize the columns in the report table, do the following actions:

    1.  Drill down the report.

    2.  Click the column settings icon \(\[Omitted image "column-settings-icon.png"\] Alt text: Column settings icon.\).

    3.  Click **Edit columns**.

    4.  In the Available columns section, click the column name.

    5.  To include a column, click the include column icon \(\[Omitted image "include-column.png"\] Alt text: Include column icon.\).

    6.  To exclude a column from the table, in the Selected columns section, click the remove column icon \(\[Omitted image "remove-column.png"\] Alt text: Remove column icon.\).

    7.  To change the positions of the columns in the report table, in the Selected columns section, click and drag the drag column icon \( \[Omitted image "drag-column.png"\] Alt text: Drag column icon.\).

    8.  To apply the changes, click **OK**.

7.  Filter the data in the reports by caller scopes, spokes, and date by doing the following steps:

    1.  To filter by caller scope or spoke, click **Caller Scope** or **Spoke** and then select one or more values.

        **Tip:** Select multiple caller scopes or spoke values by doing the following steps.

        1.  Select the **Caller Scope** or **Spoke** filter.
        2.  Click to select the first value in the Available list.

            \[Omitted image "ihub-dashboard-sel-scope.png"\] Alt text: Select single scope.

        3.  Click to select more values.

            \[Omitted image "ihub-dashboard-sel-multiple-values.png"\] Alt text: Select multiple values.

    2.  Click the Move selected items to the To be Applied list icon \[Omitted image "ihub-dashboard-move-sel-items-icon.png"\] Alt text: Move selected items to the To be Applied list icon.

    3.  Click **Apply**.

        The filter is applied.

    4.  To filter the report data by time period, select the Time Period filter.

    5.  Select the time period by which you want to filter the data.

    6.  Click **Apply**.


**Parent Topic:**[Integration Hub Usage Dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/integration-hub/integrationhub-usage-dashboard.md)

