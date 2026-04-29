---
title: Create a custom subflow for alerts
description: You can create a subflow according to your requirements. For example, you can resolve alerts, notify teams, or run remediation actions.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Alert management rules for resolving alerts, Manage and monitor alerts, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Create a custom subflow for alerts

You can create a subflow according to your requirements. For example, you can resolve alerts, notify teams, or run remediation actions.

## Before you begin

Role required: evt\_mgmt\_admin, flow\_designer

## About this task

Copy an existing subflow, and then customize it. Publish the custom subflow so that it is available to be used to resolve any alert. For more information, see [Create a subflow](https://www.servicenow.com/docs/access?context=create-subflow&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

**Note:** If your ServiceNow instance uses domain separation, you must ensure that the new custom subflow that you created operates only on the data of the designated domain.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  In the Flow Designer window, click **Subflows**.

3.  Click **Create Incident**.

    The Create Incident subflow opens in Flow Designer in read-only format. The inputs in the Create Incident subflow are described in the following table.

    |Value|Description|
    |-----|-----------|
    |alertRuleName|The name of the alert management rule that specifies this subflow, for example `IDD`.|
    |alertRuleId|The sys\_id of the alert management rule, for example, `1ae122e84f5f1300b28392918110c71e`.|
    |alertGR|The alert record that matches the filter that is defined in the alert management rule, for example, `Alert0027931`|
    |executionId|The ID of the execution to be retrieved, for example, `000182ebdb66630091187f1daf9619d4`|
    |userName|The current user's name, for example, `admin`.|
    |userDisplayName|The name that the current user specified to be displayed, for example, `System Administrator`.|

    For example, in an alert management rule that has processed alerts, in the Alert Executions area, click the **Link to execution** of the required alert.

    ![Link to execution](../image/link-to-execution.png)

    The Flow Designer opens. Click **Subflow Inputs and Outputs**. The input variable names of the subflow are displayed with their respective values.

    ![Subflow variable values](../image/subflow-parameter-values.png)

4.  In the subflow header, click more actions ![More actions](../image/more-actions-icon.png) and select **Copy subflow**.

5.  In the **New Subflow Name** field, enter the name of the new subflow.

6.  To limit the application scope of the subflow, in the **Application** field, select the required application, otherwise select `Global`.

7.  Click **Copy**.

    The new subflow is created and is opened as a tab in the subflow designer editor. The inputs provided by the template appear.

    Inputs are fixed and cannot be added to.

    In the editor, you can delete subflow inputs or outputs, as required.

8.  To delete an input, click ![Delete input icon](../image/delete-input-icon.png).

    Inputs are fixed and cannot be added to.

9.  Create subflow outputs by defining the names and data types.

    1.  Click ![Add new input icon](../image/add-input-icon.png) to add output.

    2.  Define the name and the data type.

10. To save the subflow in draft status, click **Save**.

11. To save and publish the subflow so that it can be used in the alert management rule designer, click **Publish**.


## Result

Include the modified subflow in an alert management rule to resolve alerts according to your customized requirements.

**Parent Topic:**[Alert management rules for resolving alerts](../concept/alert-management-rule.md)

**Related topics**  


[Subflows](https://www.servicenow.com/docs/access?context=subflows&version=australia&pubname=australia-build-workflows&ft:locale=en-US)

