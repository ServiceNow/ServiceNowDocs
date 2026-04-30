---
title: Create Group automation
description: Grouping automations helps you manage alerts more effectively by collecting similar alerts together. This makes it easier to see patterns, quickly identify issues, and respond efficiently. By organizing alerts in this way, you can reduce alert noise, identify root causes, and assign them to the appropriate teams.
locale: en-US
release: xanadu
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Alert automation in Service Operations Workspace for ITOM, Using Service Operations Workspace for ITOM, Service Operations Workspace for ITOM, ITOM Health, IT Operations Management]
---

# Create Group automation

Grouping automations helps you manage alerts more effectively by collecting similar alerts together. This makes it easier to see patterns, quickly identify issues, and respond efficiently. By organizing alerts in this way, you can reduce alert noise, identify root causes, and assign them to the appropriate teams.

## Before you begin

Role required: evt\_mgmt\_admin or srm\_responder

## About this task

Grouping of this method is most useful when alerts share common data or tags, such as a node or location. You can use fields or tags populated via an enrich automation. It’s the best way to group alerts when your CMDB or service maps are immature. This complements our other grouping algorithms, including alert correlation rules, CMDB, ML, and text-based grouping. Alerts are grouped with their first match, and you can control the priority order of these algorithms via system property. For information on correlation logic order, see [Configure alert correlation logic order](../../event-management/task/configure-alert-correlation-logic-order.md).

Alert automation also provides a simulation feature allowing you to test how many alert groups would be formed, how many are left ungrouped, and the compression rate. A higher compression rate means your team will be more productive and may be able to identify root causes faster. However, consider whether the groups are accurate, operationally correct, and assigned to the right teams. You may adjust the group criteria until you are satisfied with the resulting groups.

For users familiar with the classic Event Management experience, this feature offers an easier interface with improved team support for creating tag-based alert clustering definitions.

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  In the primary navigation, select the Alert Automation icon \(![Alert automations icon](../../event-management/image/alert-automations-icon.png)\).

3.  On the Alert automation page, under **Automation types**, select **Group**.

    The Group alerts page is displayed.

    ![Group alerts page opens.](../image/group-automation-page.png)

4.  Select **Create automation**.

    ![Group alerts page opens.](../image/group-automtion-name.png)

5.  In the **Automation name** field, enter the name of the automation.

6.  Activate the automation by selecting the **Active** check box.

7.  In the **If these conditions are met** section, set up filter criteria to identify the alerts that you want to group.

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

8.  In the **Then, group alerts by the following criteria** section, perform the following steps.

    ![Alert grouping criteria](../image/group-automation-criteria.png)

    1.  In the **Grouping timeframe** field, specify the duration \(in minutes\) when alerts must be collected and grouped together.
    2.  In the **Source field** menu, select the source from which you want the alerts to be grouped.

        **Note:** You can manually add a field name and select the type of the field. The available options include additional info field, alert tag, and CI tag. This flexibility allows you to customize the information being captured according to your specific needs.

    3.  In the **Match method for grouping** field, select one of the following options: group alerts based on an exact match, fuzzy match, or pattern match.

        When you select a value for the fuzzy match method in the grouping field, the **Similarity threshold \(percentage\)** field becomes visible. Alerts are grouped when their similarity is greater than or equal to the specified percentage based on edit distance.

        For example, if you have alerts from USA, CA, and USA, NY, and you want to group the alerts by country, you would set the **Source** field to USA. If the **Match Method for Grouping** is a fuzzy match and the **Similarity threshold \(percentage\)** is 50%, then alerts will be grouped if they are at least 50% similar, meaning they share the country "USA" as a common attribute.

    4.  When you select a value for the pattern match method in the grouping field, the pattern matching field becomes visible. Alerts are grouped when the specified pattern matches. For more information, see [Pattern matching](https://www.servicenow.com/docs/access?context=c_PatternMatching&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

        Use asterisks \(\*\) in the search string to match any number of characters or a question mark \(?\) to match any single character. Everything else in the search string matches itself. For example, use "HTTP Error 5??" to match all HTTP 500 errors.

        To include additional fields for grouping, select **+ Add criteria**.

9.  In the **Automation details** section, provide an order and automation description.

    ![Alert grouping automation details](../image/group-automation-details.png)

    1.  In the **Order** field, enter the automation order.

        **Note:** Alerts are grouped based on the first match, executed in order from the lowest to the highest number. The **Automation is managed by** field displays the team or assignment group who owns, edits, and can delete this automation. The assignment group is the same as the one defined in the **If these conditions are met** section.

    2.  In the **Automation description** field, enter a brief description of the automation.
10. To test if the alert grouping is working correctly, navigate to **Test this automation on past alerts**, select the timeframe for the simulation from the drop-down list, select whether you want to consider other grouping types, and then select **Test automation**.

    During the simulation, it shows both the grouped alerts and the ungrouped alerts for the specified timeframe. If any alerts are grouped, you are shown the number of alerts that are grouped. You can select this number to view the grouped alerts. Additionally, selecting an individual alert displays the details of that specific alert. You can also modify any alert grouping conditions or field values and initiate the process again by selecting **Re-run simulation**.

    The header of the Test Automation section also displays the following: total alerts, alert groups, ungrouped alerts, and compression.

    -   Total alerts: The total number of alerts before grouping.
    -   Alert groups: The number of groups containing more than one alert. The smaller number in parentheses represents the groups created by this automation.
    -   Ungrouped: The number of alerts that remain ungrouped.
    -   Compression: The percentage reduction in the number of total alerts achieved by grouping, calculated as 1 - \(Alert groups + Ungrouped\) / Total alerts. You can improve the compression rate by grouping your alerts into related problems.
    The simulation allows you to test how past alerts would be grouped if the automation was activated. It takes 200 past alerts in their ungrouped form and considers grouping them as if they were just received.

    **Note:** You can run the simulation of alerts on your test as well as production instance.

11. Select **Save automation**.

    A notification appears when the automation is successfully saved. Otherwise, an error message is displayed. The group automation that you created appears on the Group alerts page where you can view, edit, or delete the existing automation.


## What to do next

You can escalate alerts needing quicker responses from teams or individuals by implementing [respond automation](esc-notify-alert-sow-itom.md).

