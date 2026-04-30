---
title: Process Mining use cases for security incidents
description: The following Process Mining use cases provide various analysis methods that you can use to identify inefficiencies during the resolution of your security incidents.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-03-27"
reading_time_minutes: 4
breadcrumb: [Process Mining Workspace for Security Incident Response, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Process Mining use cases for security incidents

The following Process Mining use cases provide various analysis methods that you can use to identify inefficiencies during the resolution of your security incidents.

## Multi-hop analysis

Security incidents that are reassigned multiple times to different teams might result in a resolution delay. By analyzing the reasons of reassignments for such security incidents, and where the incidents are held up for longer durations, you can improve the overall efficiency.

The following are example steps to get the list of security incidents that took the longer routes:

1.  Navigate to **Workspaces** &gt; **Process Mining Workspace**.
2.  Select **Assignment group**.
3.  Open a project, and navigate to **Analyst Workbench**.

    When you open a mined process optimization project, by default the Analyst Workbench opens.

4.  Select **Variation Analysis**.
5.  Select the filter \(![Filter icon](../../security-incident-response/image/filter-icon.png)\) icon, and set the filter similar to the following:

    -   Steps greater than the average number of steps.
    -   Records greater than the minimum number of records that have taken a longer route.

        **Note:** You can configure the values as per your requirement.

    ![Example filter settings for multi-hop analysis](../image/multi-hop-filter-proc-min-sir.png)

6.  Select **Apply**.

    All the records that match the filter criteria appear. Select a record to view the closure route of the record.

7.  Select a record, and then select **Show Route**.

    The route traversed by the record appears. You can use this route to identify the step where the incidents were held up for a longer duration than expected.


## SLA breach analysis

You can use process mining to analyze security incidents that have breached a certain SLA \(Service Level Agreement.\)

The following are example steps to get the list of security incidents that breached the SLA:

1.  Navigate to **Workspaces** &gt; **Process Mining Workspace**.
2.  Open a project, and navigate to **Analyst Workbench**.

    When you open a mined process optimization project, by default the Analyst Workbench opens.

3.  From the Advanced filters, select **Conditions**.
4.  Select the arrow corresponding to **Related List Condition**.
5.  Set the conditions similar to the following:

    -   Use the **Select** list to select the `Task SLA` table.
    -   Set the value of the **Greater than or equal to** field to `1`.
    -   Set the value of **Has breached** to **True**.
    -   To identify security incidents which breached a specific SLA, set a **SLA definition** filter.
    ![Condition settings for SLA breach](../image/sla-breach-filters-proc-min.png)

6.  Select **Apply**.

    All the records that match the conditions appear. Select a record to view the route of the record for analysis.


## Priority analysis

You can use the process mining to review and improve the existing priority assignment process to your security incidents.

The following are example steps to get the list of security incidents for which are priority was modified:

1.  Navigate to **Workspaces** &gt; **Process Mining Workspace**.
2.  Open a project, and navigate to **Analyst Workbench**.

    When you open a mined process optimization project, by default the Analyst Workbench opens.

3.  Select **Priority**.
4.  From the Advanced filters, select **Transitions**.
5.  In **Advanced filter on transitions**, configure the following:

    1.  Set Priority is 1 - Critical.
    2.  Select **Eventually followed By**
    3.  Priority is not 1 - Critical.
    ![Priority analysis conditions](../image/priority-analysis-proc-min.png)

6.  Select **Apply all chains**.

    The map shows all the security incidents that were assigned a priority 1 and their priority was later lowered.


## Bottleneck analysis

You can use the process mining to review the state transitions of your security incidents. This analysis identifies the transitions that are not usual and the time delay caused because of such.

The following are example steps to perform the bottleneck analysis:

1.  Navigate to **Workspaces** &gt; **Process Mining Workspace**.
2.  Open a project, and navigate to **Analyst Workbench**.

    When you open a mined process optimization project, by default the Analyst Workbench opens.

3.  Select **Bottleneck Analysis** from the **Model Options**.

    The screen displays the state transitions for the security incidents.

    ![Bottle neck analysis](../../security-incident-response/image/bottleneck-analysis.png)

4.  Select the **Filter by** to identify bottleneck transitions. Alternatively, use the search bar to search for bottleneck transitions. For example, to identify incidents which were moved to other states from the Closed state, use "Closed " or "Closed -".

## Long time to start than resolve

You can use the process mining to review the incidents that take a long time to get to the Draft state, but then were closed in a relatively shorter time.

The following are example steps to identify security incidents that were in the Draft state for more than two days and were closed within 30 minutes after moving to the Analysis state:

1.  Navigate to **Workspaces** &gt; **Process Mining Workspace**.
2.  Open a project, and navigate to **Analyst Workbench**.

    When you open a mined process optimization project, by default the Analyst Workbench opens.

3.  From the Advanced filters, select **Transitions**.
4.  In **Advanced filter on transitions**, configure the following:
    1.  Set `State (Incident)` is `Draft`.
    2.  Select **Eventually followed By**
    3.  Select **Add constraints** and set **From** as `2` days.
    4.  Select **Add next activity**.
    5.  Set `State (Incident)` is In `Analysis`.
    6.  Select **Eventually followed By**
    7.  Select **Add constraints** and set **Up to** as `30` minutes.
    8.  Select **Add next activity**.
    9.  Select **Eventually followed By**
    10. Select **Add constraints** and set **Up to** as 30 minutes.
    11. Set `State (Incident)` is `Closed`.

        ![Long analysis time example](../../security-incident-response/image/long-analysis-example-proc-min.png)

5.  Select **Apply all chains**.
6.  Select **Breakdown Filters** and sort by **Longest Avg Duration**.

