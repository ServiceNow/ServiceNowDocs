---
title: Create Group automation
description: Grouping automation helps you manage alerts more effectively by collecting similar alerts together. This makes it easier to see patterns, quickly identify issues, and respond efficiently. By organizing alerts in this way, you can reduce alert noise, identify root causes, and assign them to the appropriate teams.
locale: en-US
release: zurich
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 9
breadcrumb: [Alert automation in SOW for ITOM, Using SOW for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# Create Group automation

Grouping automation helps you manage alerts more effectively by collecting similar alerts together. This makes it easier to see patterns, quickly identify issues, and respond efficiently. By organizing alerts in this way, you can reduce alert noise, identify root causes, and assign them to the appropriate teams.

## Before you begin

Role required: evt\_mgmt\_admin, evt\_team\_operator, or srm\_responder

## About this task

Grouping of this method is most useful when alerts share common data or tags, such as a node or location. You can use fields or tags populated via an enrich automation. It’s the best way to group alerts when your CMDB or service maps are immature. This complements our other grouping algorithms, including alert correlation rules, CMDB, ML, and text-based grouping. Alerts are grouped with their first match, and you can control the priority order of these algorithms via system property. For information on correlation logic order, see [Configure alert correlation logic order](../../event-management/task/configure-alert-correlation-logic-order.md).

Alert automation also provides a simulation feature allowing you to test how many alert groups would be formed, how many are left ungrouped, and the compression rate. A higher compression rate means your team will be more productive and may be able to identify root causes faster. However, consider whether the groups are accurate, operationally correct, and assigned to the right teams. You may adjust the group criteria until you are satisfied with the resulting groups.

For users familiar with the classic Event Management experience, this feature offers an easier interface with improved team support for creating tag-based alert clustering definitions.

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the bottom of the navigation pane, select the AIOps configuration center icon ![ITOM AIOps configuration center icon](../../health-log-analytics-admin/image/icon-itom-aiops-config.png).

    The ITOM AIOps configuration center page appears. The configuration center is a centralized workspace. Use it to configure and manage AIOps features from a single place.

3.  On the ITOM AIOps configuration center page, under the Optimize section, select **Group alerts**

    The Group alerts page is displayed.

    ![Group alerts page opens.](../image/group-automation-page.png)

4.  Select **Create automation**.

    ![Group alerts page opens.](../image/group-automtion-name.png)

5.  In the **Automation name** field, enter the name of the automation for grouping alerts.

    By default, the **Active** check box is selected.

6.  In the **If these conditions are met** section, set up filter criteria to identify the alerts that you want to group.

    ![Group alerts conditions.](../image/group-automation-operator.png)

    1.  From the **Assignment group** field menu, select the assignment group to determine which team’s alerts will trigger the automation.

        The **Assignment group** represents a specific team responsible for handling certain alerts. By selecting an assignment group, you ensure that only the alerts assigned to that particular team will trigger the automation. This way, the automation is targeted and only activates for relevant alerts associated with the selected team.

        **Note:**

        -   If you’re logged in to the instance with an administrator role \(evt\_mgmt\_admin\), all of the assignment groups are available. Additionally, you can select **All groups** to enable generating alerts for any of the available groups.
        -   If you’re an operator, only the group you’re a part of is available.
        -   Only members of the selected group or administrators can update or delete the automation.
    2.  Set up the conditions by selecting the field, operator, and field value. Then, add more conditions using OR or AND operators. You must add at least one more filter besides the assignment group.

        **Tip:** Select a more specific filter to enhance performance.

        To add another set of conditions, select **+ New condition set**. You can also manually add an additional info field if you don’t see it in the drop-down list.

        **Note:** Select **Load past events** to view previous events when creating the automation.

7.  In the **Then, group alerts by the following criteria** section, perform the following steps.

    ![Alert grouping criteria](../image/group-automation-criteria.png)

    1.  In the **Grouping timeframe** field, specify the duration \(in minutes\) when alerts must be collected and grouped together.
    2.  In the **Criteria type** menu, select how you want to group the alerts.

        Currently, there are two options:

        -   **Similar fields &amp; tags**: Group alerts based on similar fields and tags.
        -   **Related CIs**: Group alerts based on CI \(Configuration Item\) relationships—child, parent, or sibling—along with containment and applicative flows.
        -   **Impacted service instances**: Groups alerts affecting the same service instances. You can choose either **All Service Instances** or a **Specific Service Instance**. For **Specific Service Instance**, use the **Service Instance** field to select the services you want.
        -   **Related logs properties**: Groups alerts generated from logs using the Health Log Analytics grouping algorithm. The **Related logs properties** option appears only when you install the Health Log Analytics plugin.
    3.  In the **Source field** menu, select the source from which you want the alerts to be grouped.

        **Note:** You can manually add a field name and select the type of the field. The available options include additional info field, alert tag, and CI tag. This flexibility allows you to customize the information being captured according to your specific needs.

    4.  In the **Match method for grouping** field, select one of the following options: group alerts based on an exact match, fuzzy match, or pattern match.

        When you select a value for the fuzzy match method in the grouping field, the **Similarity threshold \(percentage\)** field becomes visible. Alerts are grouped when their similarity is greater than or equal to the specified percentage based on edit distance.

        For example, if you have alerts from USA, CA, and USA, NY, and you want to group the alerts by country, you would set the **Source** field to USA. If the **Match Method for Grouping** is a fuzzy match and the **Similarity threshold \(percentage\)** is 50%, then alerts will be grouped if they are at least 50% similar, meaning they share the country "USA" as a common attribute.

    5.  When you select a value for the pattern match method in the grouping field, the **Pattern matching** field becomes visible. Alerts are grouped when the specified pattern matches. For more information, see [Pattern matching](https://www.servicenow.com/docs/access?context=c_PatternMatching&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

        Use asterisks \(\*\) in the search string to match any number of characters or a question mark \(?\) to match any single character. Everything else in the search string matches itself. For example, use "HTTP Error 5??" to match all HTTP 500 errors.

        To include additional fields for grouping, select **+ Add criteria**.

8.  In the **Advanced options** section, you have two toggle options.

    -   **Set the minimum number of alerts to form a group**: Defines the least number of alerts required to create a group.

        Example: During a flash sale, you may want to group alerts only if at least 5 similar errors occur to avoid noise from single occurrences.

    -   **Form group only if at least one alert meets specific conditions you define**: When enabled, the system groups alerts only if at least one alert satisfies your defined criteria that you have mentioned in the **Then, group alerts by the following criteria** section.

        Example: Useful for critical services where you want to group alerts only if a high-severity alert is present, ignoring low-priority alerts.

        When this option is enabled, additional fields appear:

        -   **Select field**: The alert property to check, e.g., Severity, Host Name, Service Name, Metric Value, Region, or Status.
        -   **Select operator**: The comparison logic for the selected field, e.g., is, is not, contains, starts with, greater than, less than.
        -   **Enter value**: The specific data the alert's field must match or be compared against, e.g., Critical, prod-web-01, US-East-1, or 100.
        -   Operators:
            -   **or**: Combines multiple conditions; the result is true if at least one condition is true.
            -   **and**: Combines multiple conditions; all conditions must be true for the result to be true.
        -   **Add condition set**: Adds a new, independent set of conditions.
9.  In the **Automation details** section, provide an order and automation description.

    ![Alert grouping automation details](../image/group-automation-details.png)

    1.  In the **Order** field, enter the automation order.

        **Note:** Alerts are grouped based on the first match, executed in order from the lowest to the highest number. The **Automation is managed by** field displays the team or assignment group who owns, edits, and can delete this automation. The assignment group is the same as the one defined in the **If these conditions are met** section.

    2.  In the **Automation description** field, enter a brief description of the automation.
10. To test if the alert grouping is working correctly, navigate to **Test this automation on past alerts**, select the timeframe for the simulation from the drop-down list and then select **Test automation**.

    You can also modify any alert grouping conditions or field values and initiate the process again by selecting **Re-run test**.

    ![Test automation section](../image/group-automation-test.png)

    The header of the Test Automation section also displays the following: matching alerts, alert groups, ungrouped alerts, and compression.

    -   **Matching alerts**: The total number of matching alerts before grouping that match the conditions defined for this automation.
    -   **Alert groups**: The number of groups containing more than one alerts matching the automation conditions. The smaller number in parentheses represents the number of groups created by this automation.
    -   **Ungrouped**: The number of alerts matching the automation conditions that remain ungrouped.
    -   **Compression**: The percentage reduction in the number of total alerts achieved by grouping, calculated as 1 - \(Alert groups + Ungrouped\) / Total alerts. You can improve the compression rate by grouping your alerts into related problems. The smaller number in parentheses indicates the percentage of matching alerts compressed by this automation.
    -   When the criteria type is **Related CIs**:
        -   The **Open CIs dependency map** link appears in the Test Automation section.
        -   The **Configuration Item** field is displayed.
    The Test Automation section displays key columns: **Alerts**, **Description**, **Grouped by**, **Node**, and **Time**. The **Description** column outlines the alert group details. Preceding the **Description** column, a number indicates the total alerts contained within that group. **Grouped by** specifies the category of grouping, such as **Group alerts with the same Node** and **CMDB**. You can sort the **Grouped by** column which is by default in the descending order. The value for other automation group displays the name of the corresponding automation group and includes a link to it. For a single alert, the value is displayed as **–**. The **Time** column shows when the test was conducted.

    **Important:** You can run the simulation of alerts on your test as well as production instance. The test automation simulates the automation using up to 200 recent alerts that match the specified conditions. It only considers groups where all alerts meet the conditions for this automation, although additional grouping algorithms may be applied during actual runtime.

11. Select **Save automation**.

    A notification appears when the automation is successfully saved. Otherwise, an error message is displayed. The group automation that you created appears on the Group alerts page where you can view, edit, or delete the existing automation.

    **Note:** After you save the automation, when you select an automation result and hover over the green dot next to an alert, a tooltip appears explaining its meaning.

    ![A tooltip explaining its meaning of the alert.](../image/group-automation-test-details1.png)

    If you select the description, it opens a detailed view with additional information.![A detailed view with additional information.](../image/group-automation-test-details2.png)


## What to do next

You can escalate alerts needing quicker responses from teams or individuals by implementing [respond automation](esc-notify-alert-sow-itom.md).

