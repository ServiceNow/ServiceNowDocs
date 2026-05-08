---
title: Create an agent policy
description: Create an agent policy by configuring a filter that determines the Configuration Items \(CI\) to run the checks and the metrics that are collected.
locale: en-US
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Managing DEX Agent policy, Configure, Digital End-User Experience, IT Service Management]
---

# Create an agent policy

Create an agent policy by configuring a filter that determines the Configuration Items \(CI\) to run the checks and the metrics that are collected.

## Before you begin

Confirm that the DEX plugin \(sn\_dex\) is installed.

Role required: admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  In the primary navigation pane, select the DEX Administration icon \(![](../image/icon-administration.png)\).

3.  In the Device and application configuration section, select **Manage policies** on the Agent policies card.

4.  Select **New**.

5.  Provide a descriptive name and description for the policy.

    **Note:** In the **Publish status**, the value is set to *Draft*. After you create and save the policy, the **Publish status** value changes to *Ready to publish*. In the **Hierarchy** field, the value is set to *None*. If you create a child for the current policy, the value changes to *Parent*.

6.  On the **Monitored CIs** tab, select one of the following options.

<table id="choicetable_en5_d41_52c"><thead><tr><th align="left" id="d238035e145">

Option

</th><th align="left" id="d238035e148">

Description

</th></tr></thead><tbody><tr><td id="d238035e154">

**Manual calculation**

</td><td>

Select to exclude the policy from scheduled policy calculation, ignoring any changes to the policy impacted CIs.Select this option when the policy monitors a single CI. The option enables you to avoid a long completion time for the Refresh and Publish Monitoring Policies scheduled job.

</td></tr><tr><td id="d238035e165">

**Monitored CI type by filter**

</td><td>

1.  In the **Monitored CI type** field, select the CI type, which you want the policy checks to monitor.
2.  In the **Filter** field, configure a filter so that the policy checks monitor only CI types, which meet the specified criteria. CI **tags** are included in the available criteria.


</td></tr><tr><td id="d238035e192">

**Monitored CI type by script**

</td><td>

Specify the monitored CIs using a script. Using a script enables you to create a CI filter for several tables related to each other. For example, you can set a filter in both a Linux servers table and an Oracle table when searching for a CI.

</td></tr><tr><td id="d238035e203">

**Monitored CI type by CMDB Group**

</td><td>

Specify the monitored CIs by using CMDB group queries. When selected, the **Monitored CMDB group** drop-down list of CMDB groups appears.

</td></tr></tbody>
</table>7.  On the **Checks** tab, select checks in the **Available** cell and use the arrow to move them to the **Selected** cell.

    Checks can be selected multiple times when you’re monitoring more than one process. You can also select a group of checks in the **Filter checks by groups** field, which presents checks of the selected group in the **Available** cell.

8.  On the **Proxy Settings** tab, configure a proxy server.

    Configure a proxy server only when using the agent as a proxy to report data on remote machines.

9.  On the **Scheduling** tab, select one of the following options.

<table id="choicetable_elq_mdb_52c"><thead><tr><th align="left" id="d238035e268">

Option

</th><th align="left" id="d238035e271">

Steps

</th></tr></thead><tbody><tr><td id="d238035e277">

**Interval-based scheduling**

</td><td>

Configure the time interval \(in seconds\) to indicate the frequency with which the policy's checks run.

</td></tr><tr><td id="d238035e286">

**Cron-based scheduling**

</td><td>

Enables configuring the policy to be active only during a specific time or time frames.1.  Select the Unlock icon \(![Unlock icon](../image/icon-acc-lock.png)\) to enable selecting cron expressions.
2.  Select the search icon \(![Search icon](../../configurable-workforce-optimization-itsm/image/search-icon.png)\), then select **New** to create a cron expression.

You can also select one of the following cron expressions that come with the base system:

    -   Every hour nightly 5:00pm-7:00am
    -   Every minute daily 8:00am-4:59pm
    -   Every minute Mon-Fri 8:00am-4:59pm
The specified cron expression operates in the time zone of the machine hosting the agent.

</td></tr></tbody>
</table>    **Note:** If an **Interval** or **Cron** value was specified for the check definition, that value overrides the value configured in either of these fields.

10. On the **Credentials** tab, select one of the following.

    |Options|Steps|
    |-------|-----|
    |**Credential name**|Select credentials to be assigned to the policy. The available credentials are displayed on the associated check definition's **Check Secure Parameter Definitions** tab.|
    |**Credential alias**|Select the Search icon ![Search icon](../../configurable-workforce-optimization-itsm/image/search-icon.png) to select a credential alias to be used by the policy's checks to connect to the monitored CI. The available options are created on the **Connection &amp; Credential Aliases** page.|

11. Select **Save**.

    The following buttons appear:

    -   **Publish**: Publishes the Draft policy, moving its **Publish status** to **Queued**. A queued policy is processed by the policy publishing job. The job calculates which agents run the policy and then sends the policy to the relevant MID Servers. The job then moves the policy's **Publish status** to **Published**. A published policy is active on the agent.
    -   **Delete**: Deletes the policy.

