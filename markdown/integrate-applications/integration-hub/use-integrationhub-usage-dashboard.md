---
title: Get insights from the Integration Hub Usage Dashboard
description: Use the Integration Hub Usage Dashboard to get insights on the Integration Hub transactions. For example, you can view which protocol was the most used in the transactions in the last year. You can also use filters and customize the layout and arrangement of the columns in the reports.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2023-08-03"
reading_time_minutes: 3
breadcrumb: [Integration Hub Usage Dashboard, Configuring Integration Hub, Integration Hub, Creating integrations with applications]
---

# Get insights from the Integration Hub Usage Dashboard

Use the Integration Hub Usage Dashboard to get insights on the Integration Hub transactions. For example, you can view which protocol was the most used in the transactions in the last year. You can also use filters and customize the layout and arrangement of the columns in the reports.

## Before you begin

Role required: admin, flow designer, action\_designer, usage\_admin, or flow\_operator

## Procedure

1.  To access the dashboard, navigate to **All** &gt; **IntegrationHub** &gt; **IntegrationHub Usage**.

    **Tip:** Get quicker access by entering **Integrationhub usage** in the filter search field ![Filter search field.](../images/filter-search.png).

2.  To view the reports, select **Spokes** or **Protocols &amp; Features** in the **View by** list.

    ![View reports.](../images/ihub-dashboard-view-reports.png)

    **Note:** There’s no order in which you must view the reports, set the filters, or customize the columns in the report tables. So, you can complete one or more of the following steps in any order. The Transactions tab is selected by default.

3.  To drill down and view more details in a report, select the graph or chart.

4.  To group transactions under a common parameter, do the following actions:

    1.  Drill down the report.

    2.  In the desired column, move the mouse device to the row that contains the parameter and click the group transactions by parameter icon \(![Group transactions by parameter icon.](../images/group-by-icon.png)\) for the parameter under which you want to group the transactions.

    3.  Click **Show Matching**.

        Alternatively, you can view the following animation by opening this topic on a browser.

        ![Group transactions by parameter.](../images/group-by.gif "Group transactions by parameter")

5.  To hide or reveal the slices in a pie chart, do the following actions:

    Each slice in a pie chart represents a transaction usage insight. However, it might be difficult to view certain slices because they’re obscured by fairly bigger slices.

    1.  To hide a slice, click its colored legend.

    2.  To reveal the slice back, click the colored legend again.

    Alternatively, you can view the following animation by opening this topic on a browser.

    ![Hide or reveal pie chart slices.](../images/hide-reveal-pie-slices.gif "Hide or reveal pie chart slices")

6.  To customize the columns in the report table, do the following actions:

    1.  Drill down the report.

    2.  Click the column settings icon \(![Column settings icon.](../images/column-settings-icon.png)\).

    3.  Click **Edit columns**.

    4.  In the Available columns section, click the column name.

    5.  To include a column, click the include column icon \(![Include column icon.](../images/include-column.png)\).

    6.  To exclude a column from the table, in the Selected columns section, click the remove column icon \(![Remove column icon.](../images/remove-column.png)\).

    7.  To change the positions of the columns in the report table, in the Selected columns section, click and drag the drag column icon \( ![Drag column icon.](../images/drag-column.png)\).

    8.  To apply the changes, click **OK**.

7.  Filter the data in the reports by caller scopes, spokes, and date by doing the following steps:

    1.  To filter by caller scope or spoke, click **Caller Scope** or **Spoke** and then select one or more values.

        **Tip:** Select multiple caller scopes or spoke values by doing the following steps.

        1.  Select the **Caller Scope** or **Spoke** filter.
        2.  Click to select the first value in the Available list.

            ![Select single scope.](../images/ihub-dashboard-sel-scope.png)

        3.  Click to select more values.

            ![Select multiple values.](../images/ihub-dashboard-sel-multiple-values.png)

    2.  Click the Move selected items to the To be Applied list icon ![Move selected items to the To be Applied list icon.](../images/ihub-dashboard-move-sel-items-icon.png)

    3.  Click **Apply**.

        The filter is applied.

    4.  To filter the report data by time period, select the Time Period filter.

    5.  Select the time period by which you want to filter the data.

    6.  Click **Apply**.


**Parent Topic:**[Integration Hub Usage Dashboard](../concept/integrationhub-usage-dashboard.md)

