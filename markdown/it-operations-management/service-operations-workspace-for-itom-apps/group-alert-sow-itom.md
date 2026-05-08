---
title: Create Group automation
description: Grouping automation helps you manage alerts more effectively by collecting similar alerts together. This makes it easier to see patterns, quickly identify issues, and respond efficiently. By organizing alerts in this way, you can reduce alert noise, identify root causes, and assign them to the appropriate teams.
locale: en-US
release: australia
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 11
breadcrumb: [Alert automation in SOW for ITOM, Using SOW for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# Create Group automation

Grouping automation helps you manage alerts more effectively by collecting similar alerts together. This makes it easier to see patterns, quickly identify issues, and respond efficiently. By organizing alerts in this way, you can reduce alert noise, identify root causes, and assign them to the appropriate teams.

## Before you begin

Role required: evt\_mgmt\_admin, evt\_team\_operator, or srm\_responder

## About this task

Grouping of this method is most useful when alerts share common data or tags, such as a node or location. You can use fields or tags populated via an enrich automation. Use of alert tags is the best way to group alerts when your CMDB or service maps are immature. This complements our other grouping algorithms, including alert correlation rules, ML, and text-based grouping. Even if a new alert is matched with multiple groups, it is grouped only with the first match, and you can control the priority order of these algorithms via system property. For information on correlation logic order, see [Configure alert correlation logic order](../../event-management/task/configure-alert-correlation-logic-order.md).

Alert automation also provides a simulation feature allowing you to test how many alert groups would be formed, how many are left ungrouped, and the compression rate. A higher compression rate means your team is more productive and may be able to identify root causes faster. However, consider whether the groups are accurate, operationally correct, and assigned to the right teams. You may adjust the group criteria until you are satisfied with the resulting groups.

For users familiar with the classic Event Management experience, this feature offers an easier interface with improved team support for creating tag-based alert clustering definitions.

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the bottom of the navigation pane, select the AIOps configuration center icon ![ITOM AIOps configuration center icon](../../health-log-analytics-admin/image/icon-itom-aiops-config.png).

    The ITOM AIOps configuration center page appears. The configuration center is a centralized workspace. Use it to configure and manage AIOps features from a single place.

3.  On the ITOM AIOps configuration center page, under the Optimize section, select **Group alerts**

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

7.  In the **Then, group alerts by the following criteria** section, perform the following steps.

    ![Alert grouping criteria](../image/group-automation-criteria.png)

    1.  In the **Grouping timeframe** field, specify the duration \(in minutes\) when alerts must be collected and grouped together.
    2.  In the **Criteria type** menu, select how you want to group the alerts.

        Available options are:

        -   **Similar fields &amp; tags**: Groups alerts that share common fields or tags.
            -   In the **Source field** menu, select the source from which you want the alerts to be grouped.

                **Note:** You can manually add a field name and select the type of the field. The available options include additional info field, alert tag, and CI tag. This flexibility allows you to customize the information being captured according to your specific needs.

            -   In the **Match method for grouping** field, select one of the following options: group alerts based on an exact match, fuzzy match, or pattern match.

                When you select a value for the fuzzy match method in the grouping field, the **Similarity threshold \(percentage\)** field becomes visible. Alerts are grouped when their similarity is greater than or equal to the specified percentage based on edit distance.

                For example, if you have alerts from USA, CA, and USA, NY, and you want to group the alerts by country, you would set the **Source** field to the location. If the **Match Method for Grouping** is a fuzzy match and the **Similarity threshold \(percentage\)** is 50%, then alerts will be grouped if they are at least 50% similar, meaning they share the country "USA" as a common attribute.

            -   When you select a value for the pattern match method in the grouping field, the **Pattern matching** field becomes visible. Alerts are grouped when the specified pattern matches. For more information, see Pattern matching.

                Use asterisks \(\*\) in the search string to match any number of characters or a question mark \(?\) to match any single character. Everything else in the search string matches itself. For example, use "HTTP Error 5??" to match all HTTP 500 errors.

        -   **Related CIs**: Group alerts according to CI \(Configuration Item\) relationships—such as parent/child \(**VM** &gt; **host**\), sibling relationships \(for example, multiple VMs on the same host\), containment \(**process** &gt; **application** &gt; **server**\), and applicative flows that describe how components interact within an application. In simple terms, these alerts are connected because the underlying infrastructure components are connected.
        -   **Related log properties**: Health Log Analytics \(HLA\) alerts are grouped together because their underlying logs look related based on patterns detected by the HLA algorithms.

            You can create an alert group based on related log properties on HLA alerts combined with alert tags or CMDB logic. When you choose to use related log properties, only log analytics alerts will be considered for grouping. Run the related log properties rule later in the rule order so that other rules—such as CMDB- or service-based grouping—can evaluate and group log analytics alerts first.

        -   **Impacted service instances**: Alerts are grouped because they affect the same service instance, regardless of topological distance \(hops\) between the alert CIs.

            You can control which service instance must be considered by specifying relevant impacted service instance. When you select **Impacted service instances**, two options are available: **Any service instance** and **Specific service instance**. If you choose **Specific service instance**, you can select one or more service instances from the list, or select the search icon \(![search icon](../../health-log-analytics-operator/image/icon-search-sow.png)\) to open the **Select impacted service instances** pop-up and choose the required service instances.

            By default, the Impacted service instances grouping criterion is based on the impacted service. It can also be configured to use service associations from the \[svc\_ci\_assoc\] table. You can control whether to use impacted services or service associations using the **sa\_analytics.use\_impacted\_services\_for\_mixed\_grouping** system property. If the property value is `true`, alerts are grouped by impacted services and if the property value is `false`, the alerts are grouped by service associations.

    3.  To include additional fields for grouping, select **+ Add criteria**.
8.  In the **Advanced options** section, you can do the following:

    -   Enable the toggle switch to set the minimum number of alerts required to form a group. When you enable it, the **Minimum number of alerts in the group** field appears, allowing you to enter the number. The default value is 2, which means grouping occurs only when there are two or more alerts.
    -   Enable the toggle switch to form group only if at least one alert meets specific conditions you define.

        **Note:** The threshold and required alert act as prerequisites for forming an alert group. The threshold defines the minimum number of alerts required to create a group. The required alert condition ensures that at least one specific, meaningful alert is present before grouping starts. If that alert is not present, the group is not created — even if there are multiple other alerts. In other words, a group is created only when both conditions are satisfied.

        Example: Imagine a network switch with multiple ports, where alerts can occur either on individual ports or on the switch itself. You want a group to be created only when the switch is affected, not when there is just a port-level issue. In this setup, if alerts occur only on one or more ports, no group is created. A group is created only when an alert occurs on the switch along with one or more alerts on its ports. This ensures that grouping happens only for larger, meaningful issues involving the switch, and not for minor or isolated port problems. This is useful because it prevents unnecessary alert groups from being created, helps you focus on more important and meaningful issues, and reduces noise caused by minor or isolated alerts.

9.  In the **Automation details** section, provide an order and automation description.

    ![Alert grouping automation details](../image/group-automation-details.png)

    1.  In the **Order** field, enter the automation order.

        **Note:** Alerts are grouped based on the first match, executed in order from the lowest to the highest number. The **Automation is managed by** field displays the team or assignment group who owns, edits, and can delete this automation. The assignment group is the same as the one defined in the **If these conditions are met** section.

    2.  In the **Automation description** field, enter a brief description of the automation.
10. To test if the alert grouping is working correctly, navigate to **Test this automation on past alerts**, select the timeframe for the simulation from the drop-down list, select whether you want to consider other grouping types, and then select **Test automation**.

    **Note:** From the **Consider other group types** menu, you can select either **This automation only** or **Consider other group types**. Selecting **This automation only** ignores other alert group types while choosing **Consider other group types** includes all alert grouping automations, such as mixed, automated, and text-based alert grouping.

    During the simulation, it shows both the grouped alerts and the ungrouped alerts for the specified timeframe. If any alerts are grouped, you are shown the number of alerts that are grouped. You can select this number to view the grouped alerts. Additionally, selecting an individual alert displays the details of that specific alert. You can also modify any alert grouping conditions or field values and initiate the process again by selecting **Re-run test**.

    ![Test automation section](../image/group-automation-test.png)

    The header of the Test Automation section also displays the following: matching alerts, alert groups, ungrouped alerts, and compression.

    -   **Matching alerts**: The total number of matching alerts before grouping that match the conditions defined for this automation.
    -   **Alert groups**: The number of groups containing more than one alerts matching the automation conditions. The smaller number in parentheses represents the number of groups created by this automation.
    -   **Ungrouped**: The number of alerts matching the automation conditions that remain ungrouped.
    -   **Compression**: The percentage reduction in the number of total alerts achieved by grouping, calculated as 1 - \(Alert groups + Ungrouped\) / Total alerts. You can improve the compression rate by grouping your alerts into related problems. The smaller number in parentheses indicates the percentage of matching alerts compressed by this automation.
    -   When the criteria type is **Related CIs**:
        -   The **Open CIs dependency map** link appears in the Test Automation section.
        -   The **Configuration Item** field is displayed.
    The Test Automation section displays three key columns: **Description**, **Type**, and **Time**. The **Description** column outlines the alert group details. Preceding the **Description** column, a number indicates the total alerts contained within that group. **Type** specifies the category of grouping, such as This grouping automation, Other grouping automation, CMDB group, or Single alert, among others. Selecting **Other grouping automation** directs you to the corresponding automation page that generated the group. Additionally, the **Time** column shows when the test was conducted.

    **Important:** You can run the simulation of alerts on your test as well as production instance. The test automation simulates the automation using up to 200 recent alerts that match the specified conditions. It only considers groups where all alerts meet the conditions for this automation, although additional grouping algorithms may be applied during actual runtime.

11. Select **Save automation**.

    A notification appears when the automation is successfully saved. Otherwise, an error message is displayed. The group automation that you created appears on the Group alerts page where you can view, edit, or delete the existing automation.


## What to do next

You can escalate alerts needing quicker responses from teams or individuals by implementing [Create Respond automation](respond-alert-sow-itom.md).

