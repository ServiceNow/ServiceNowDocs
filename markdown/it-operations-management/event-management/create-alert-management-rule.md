---
title: Create an alert management rule
description: Create an alert management rule to track alerts and resolve them by determining the required response, for example, to open an incident or launch remediation action.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Alert management rules for resolving alerts, Manage and monitor alerts, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Create an alert management rule

Create an alert management rule to track alerts and resolve them by determining the required response, for example, to open an incident or launch remediation action.

## Before you begin

To enable remediation with a subflow, you can use a subflow that is available with the base system, or you can create your own subflow. For details, see [Create a custom subflow for alerts](create-custom-create-incident-subflow.md).

Role required: evt\_mgmt\_admin, flow\_designer

## About this task

Use alert management rules to track and resolve alerts.

While working in the alert management rule designer, you can work in multiple sections without losing information in any section.

**Note:**

-   Alert management rules that are not configured to perform any action are skipped and the rule is automatically set to inactive.
-   If an alert is bound to a CI by a user action \(such as an alert management rule\) and the CI is in the Maintenance state, you must manually bind the CI to the alert and mark it with the **In Maintenance** status.

Create alert management rules that:

-   Locate other alert management rules that have relevance to the selected alert.
-   Determine when the execution of the rule takes place.

Alert management rules do not necessarily complete in the order in which they are invoked.

You can configure alert management rules to:

-   Automatically generate and link incidents, tasks, or knowledge articles to alerts.
-   Automatically apply a remediation workflow or enable users to manually run remediation.
-   Automatically construct a URL according to the value of specified fields in the alert.

To assist you, several alert management rules are provided with the base system. You can use them as presented or you can use them as examples to build custom alert management rules.

<table id="table_bmf_1ht_zcb"><thead><tr><th>

Rule

</th><th>

Description

</th><th>

Active

</th></tr></thead><tbody><tr><td>

Open sensor dashboard in PRTG

</td><td>

The sensor dashboard in the Paessler PRTG Network Monitor \(PRTG\) application opens.

</td><td>

Yes

</td></tr><tr><td>

Oracle EM Launch Target Status and View Events

</td><td>

Launch Oracle Enterprise Manager to view: -   Target Status
-   Event for alerts from source Oracle EM

</td><td>

Yes

</td></tr><tr><td>

Drilldown to OMI

</td><td>

Drill down to the HP Operations Manager i \(OMi\) application.

</td><td>

Yes

</td></tr><tr><td>

Create Incident on Primary Critical Alert

</td><td>

Create an incident for primary critical alerts. The incident can be created automatically or manually.

</td><td>

No

</td></tr><tr><td>

Search Google for "description"

</td><td>

Open Google Search in a browser to search for data according to the description that appears in the alert.

</td><td>

Yes

</td></tr><tr><td>

Create Incident

</td><td>

Create an incident for all alerts that are not in maintenance state. The rule runs automatically on selective update.

</td><td>

No

</td></tr><tr><td>

Create Incident Manually

</td><td>

Manually create an incident for alerts that are not in maintenance state.

</td><td>

Yes

</td></tr><tr><td>

Create Major Incident Candidate

</td><td>

Create a major incident candidate for all alerts that are not in maintenance state and are not secondary alerts. A major incident candidate can be promoted to become a major incident.

</td><td>

No

</td></tr><tr><td>

Create Major Incident

</td><td>

Create a major incident for all alerts that are not in maintenance state and are not secondary alerts.

</td><td>

No

</td></tr></tbody>
</table>If your instance was upgraded from Kingston, the alert action rules that were provided with the Kingston base system are available to you. However, if you modified any of the rules, the changes made are not carried over.

Alert management rules run 5 seconds after an alert is updated, resetting the timer if updates occur within that window. This delay ensures remediation actions, such as incident creation, are triggered only when the issue is clear and stable, reducing duplicates and unnecessary noise. To change the default 5-second delay, create the **evt\_mgmt.alert\_rule\_delay** property on the **All** &gt; **System Properties** &gt; **All Properties** and change the value. To know how to create a property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=australia&pubname=australia-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

## Procedure

1.  Navigate to **Event Management** &gt; **Rules** &gt; **Alert Management Rules**.

2.  Click **New** and then fill in the fields.

<table id="table_jgd_nn5_xy"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the rule.

</td></tr><tr><td>

Active

</td><td>

Check box for enabling the rule. If this check box is selected, you must specify:

-   in the **Alert Filter** section, an alert filter
-   in the **Actions** section, at least one of any of these actions:
    -   active subflow
    -   workflow
    -   quick response


</td></tr><tr><td>

Order

</td><td>

Order in which rules are evaluated when multiple rules are defined for the same alert. Alert management rules are evaluated in ascending order. The default value is `100`.

</td></tr><tr><td>

Multiple alert rules

</td><td>

Instruction about whether to search for additional rules:-   **Search for additional rules**: Execute the current rule then continue and execute other matching rules in the order of rule priority, where the lower number has the higher priority.
-   **Stop search for additional rules**: Execute only the current rule for the alert that matches the filter.

When selecting this option, a rule configured second in a rule hierarchy may run before the results of the first rule take effect.

</td></tr><tr><td>

Description

</td><td>

Descriptive text for the rule.

</td></tr><tr><td>

Assignment group

</td><td>

Assignment group that works on the alert.If no assignment group is defined in the alert rule, then this alert rule is considered as a global rule.

When the rules are running – first the global rules run and then the rules that belong to the assignment group of the alert.

</td></tr></tbody>
</table>3.  Click **Alert Filter** and specify conditions for alerts that this rule is applied to.

<table id="table_j12_ff5"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Rule is activated when

</td><td>

Rule execution takes place when:-   **Alert changes to filter**–content changes to the alert cause the alert to match the filter. If the filter is matched on following update of the alert, the rule is not applied. If the alert was closed and then reopens, at the next update of the alert and the filter is matched, the rule is applied. Thereafter, when there is an update of the alert, the rule is no longer applied.
-   **Alert matches filter**–the content of the alert matches the filter. On following update of the alert and if the filter is matched, the rule runs and is applied to the alert. The rule remains applied for every matching update.


</td></tr><tr><td class="sub-head" colspan="2">

Alert filter

</td></tr><tr><td>

Preview

</td><td>

Function to preview alerts that match the specified condition. A hyperlink shows how many alerts match the filter. ![Alert Preview filter](../image/alert-preview-filter.png) If you click the hyperlink, the browser opens another tab that lists alerts in the Alerts \[em\_alert\_list\] table. The list shows which alerts match the rule, including closed alerts. Alerts that have already been run by the rule are not marked in any way. You can click any alert to view further details.

</td></tr><tr><td>

Conditions

</td><td>

Conditions that, if fulfilled, cause the filter to be applied. For more information about building conditions, see [Using the condition builder](https://www.servicenow.com/docs/access?context=create-cond-state-using-cond-build&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).To add another condition, click **New Criteria**.

**Note:** The **Created on** condition is not invoked when running the **Event Management - Evaluate Alert Management Rules** job. Instead, use the **Updated on** condition, as the job detects alerts based on the time they were updated and not on the time they were created.

</td></tr><tr><td>

Related List Conditions

</td><td>

Conditions to include a relationship with another table in the filter.1.  Click **Table** and select the required table.
2.  Specify the conditions for this filter.
For more information about creating related lists, see [Add related list conditions](https://www.servicenow.com/docs/access?context=create-related-list-query&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

</td></tr></tbody>
</table>4.  Click **Actions**.

    In this section, you can configure the following action types as a response to alerts or to remediate alerts:

    -   Remediation Subflows: Execute a subflow provided with the base system.
    -   Launch Applications: Open applications and browsers that you configure.
    **Note:** The Remediation Workflows option is deprecated. To enable flows to be triggered by alerts, use the Flow Designer.

5.  In the Remediation Subflows section, follow these instructions to add subflows:

    1.  Under **Subflow**, double-click the cell.

    2.  Click the search icon ![Look-up icon](../image/LookupUsingList.png).

        The list of subflows provided with the base system appears. For more information, see [Event Management subflows in the base system](../reference/subflows-provided.md).

    3.  From the subflow list, select a subflow.

    4.  Repeat, adding as many subflows as required.

        ![Remediation workflow example](../image/alert-remediation-subflows-example.png)

    5.  To specify when the subflow must be executed, double-click the cell under **Execution**.

        |Name|Description|
        |----|-----------|
        |Automatic|The subflow is executed automatically when the rule is matched.|
        |Manual|Execute the subflow if required when the rule is matched.|
        |Both|When the rule is matched, the subflow is executed automatically and you can optionally execute the subflow again manually.|

    6.  Under **Automatic executions limit**, double-click the cell and enter the integer number of times to execute the subflow.

        After the subflow has been executed the indicated number of times, it does not run anymore.

    7.  To enable the subflow to be executed, double-click the cell under **Active** and select `true`.

        A link in the cell under **Link to Flow Designer** appears only after a subflow has been selected and the rule has been saved.

        ![Link to subflow](../image/link-to-flow-designer.png)

6.  To add instructions to launch applications or to open browser windows, in the Launch Applications area:

    1.  Under **Display Name**, double-click the cell.

        Specify a name for the link.

    2.  In the **URL** field, compose the URL using data from the alert in the format:`http://${source}.com:${port}/${cmdb_ci.name}`

        The **Active** field is automatically updated.

        Any URL-based action can utilize the alert parameters and the URLs can refer to wikis, messaging services, REST APIs, and so on.

7.  Click **Submit**.


## Result

The alert management rule is added to the list of available rules that can be used to resolve alerts.

**Parent Topic:**[Alert management rules for resolving alerts](../concept/alert-management-rule.md)

**Related topics**  


[Apply a quick response in an alert](apply-quick-response-in-alert.md)

