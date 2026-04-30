---
title: Create an SLA definition
description: You can create one or more Service Level Agreement \(SLA\) definitions and use them to create an SLA record. This SLA record enables you to use an SLA system for your organization's task.
locale: en-US
release: xanadu
product: Service Level Management
classification: service-level-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Service Level Agreement \(SLA\) definition, Configure Service Level Agreement \(SLA\), Configuring Service Level Management, Service Level Management, IT Service Management]
---

# Create an SLA definition

You can create one or more Service Level Agreement \(SLA\) definitions and use them to create an SLA record. This SLA record enables you to use an SLA system for your organization's task.

## Before you begin

When you create an SLA definition, avoid using dot-walked fields that change frequently in any of the SLA conditions \(start, stop, pause, and reset\). The SLA engine features, such as SLA Timeline and SLA Repair replays the audit history of the Task record that the task\_sla is attached to. The SLA engine does not replay the audit history of any dot-walked fields from that Task, rather only considers the final state of the dot-walk fields.

For example, a pause condition is set to an incident dot-walk field `incident.company.cost_center`. The value of the Cost Center is first set to Finance and later changed to Engineering. When the SLA repair runs, only the final value of the Cost Center is considered. So, if the SLA pause condition is: `incident.company.cost_center is Engineering`, SLA Repair pauses immediately, because the SLA Repair does not consider the previous Cost Center value: Finance. This condition also applies to SLA Timeline \(as well as when executing the SLA Engine asynchronously\).

Now, if the requirement is to pause when incident.company.cost\_center is Engineering and not Finance, then the audit history must be on the Task record using a custom field. Create a custom field \(in this example on the incident table\) such as: u\_company\_cost\_center and a business rule to populate the field when either the company changes or the Cost Center of the company changes. In this approach, instead of setting the SLA pause condition to the dot-walked field, it is set against the custom field. The given approach ensures that the task\_sla, SLA repair, and SLA Timeline always shows the same results.

**Note:** The deeper the dot walk, the more business rules are required.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Service Level Management** &gt; **SLA** &gt; **SLA Definitions**.

2.  Click **New**.

    The **SLA Definition** form is displayed.

3.  On the form, fill in the fields.

<table id="table_fzg_nxf_qs"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name that identifies the SLA definition.

</td></tr><tr><td>

Type

</td><td>

Select the type of agreement being defined: **SLA**, **OLA**, or **Underpinning contract**. **Note:** Type is used for reporting purposes only.

</td></tr><tr><td>

Target

</td><td>

Select the target of the agreement being defined: **None**, **Response**, or **Resolution**. Target is used for filtering, searching, and reporting purposes only.**Note:** This feature is available only in new instances starting with Jakarta or a later release.

</td></tr><tr><td>

Table

</td><td>

Table that determines the records tracked by the SLA. SLAs can be defined for any table that extends the task table, including incident, change request, and service catalog tasks. **Note:** Starting with the Helsinki release, you can and [create an SLA definition for configuration items and business services](https://www.servicenow.com/docs/access?context=c_EMSLAsForBSAndCIs&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US) for Event Management.

</td></tr><tr><td>

Flow

</td><td>

Select the flow to run when the SLA definition attaches to a Task record. Selecting a flow disables the **Workflow** field.

</td></tr><tr><td>

Workflow

</td><td>

Select the workflow to run when the SLA definition attaches to a Task record. Selecting a workflow disables the **Flow** field.

</td></tr><tr><td>

Vendor

</td><td>

Select the vendor associated with the SLA definition.

</td></tr><tr><td>

Service Commitment

</td><td>

A flag that helps to differentiate between a normal SLA definition and a service offering SLA definition.

</td></tr><tr><td>

Enable logging

</td><td>

Check box to activate debug logging just for the specific SLA definition. The debug logging information includes details of the conditions that have matched or not matched. The information also provides the before and the after values for the task SLA and task records.

</td></tr><tr><td>

Duration type

</td><td>

Specify the method for calculating the duration of the SLA. The duration can either be a **User specified duration**, or a **Relative Duration**, such as **Breach on Due Date** or **End of next business day**.

</td></tr><tr><td>

Duration

</td><td>

Specify the length of time the SLA runs before it is marked **Breached**. This field appears when the duration is **User specified duration**.**Note:** The number of days specified in this field is converted to 24-hour blocks. If the **Schedule** field identifies a schedule with eight-hour days, a duration of **1 Day** sets the SLA to breach three business days later.

</td></tr><tr><td>

Relative duration works on

</td><td>

Specify the record that the relative duration should be calculated for. Select either **Task record** or **SLA record**. This field appears only when the relative duration is specified.

</td></tr><tr><td>

Schedule source

</td><td>

Specify the schedule to be used when creating task SLAs. You can specify one of the following options:-   **No schedule**: If the **No Schedule** option is selected, the SLA calculates the schedule duration based on a 24 x 7 schedule.
-   **SLA definition**: If the **SLA definition** option is selected, the **Schedule** choice list appears.

**Schedule**: Specify the hours during which the SLA timer runs.

-   **Task field**: This option title is determined from the option selected in the Table field, for example, if the Incident option is selected in the Table field, this option becomes the Incident field. If the **Task table field** option is selected, the **Schedule source field** list appears.

Schedule source field: Select the appropriate field from the task such as an incident or problem that provides the schedule. For example, **Configuration item** &gt; **Schedule**.

</td></tr><tr><td>

Timezone Source

</td><td>

Specify the time zone source to be used when creating task SLAs. You can specify one of the following time zones:-   **The caller's timezone**.
-   **The SLA definition's timezone**: If the **The SLA definition's timezone** option is selected, the **Timezone** choice list appears.

**Timezone**: Specify a time zone for the SLA. The time zone can be the system time zone or active standard geographical time zones.

-   **The CI location's timezone**.
-   **The task's location's timezone**.
-   **The caller's location's timezone**.


</td></tr><tr><td class="sub-head" colspan="2">

Tabs

</td></tr><tr><td>

Start condition

</td><td>

Define the conditions under which the SLA is attached. From the **When to cancel** list, you can choose the conditions under which the SLA is canceled.

-   **Start conditions are not met** option: If one or more of the specified start conditions change, the SLA is canceled. This option is selected by default.
-   **Cancel conditions are met** option: The start condition must be met only once, thereafter the SLA is canceled only when the cancel condition is met.
-   **Never** option: The SLA is never canceled.
 **Retroactive start**: **** to choose a date and time field from the task that provides the start time of the task SLA. If you select the **Retroactive start** check box, the **Set start to** field and the **Retroactive pause time** check box appear.

-   **Set start to** field: Offers the date and time fields available on the task type that this SLA definition applies to. For example, if you select **Retroactive start** on a Priority 1 SLA definition and choose **Created** in the **Set start to** field, then the SLA is attached with the start time that is the date and time from the **Created** field on the incident.
-   **Retroactive pause time** check box: Enables the calculation of retroactive pause time on the specific SLA definition. For example, if you select **Retroactive start** on a Priority 1 SLA definition and then select the **Retroactive pause time** check box, the SLAs that have enabled retroactive start can recover prior to the pause time.

**Note:** The **Retroactive pause time** check box is available only when the duration is a user-specified duration.

</td></tr><tr><td>

Pause condition

</td><td>

Define the conditions under which the SLA suspends increasing elapsed time. From the **When to resume** list, you can choose the conditions under which the SLA resumes increasing elapsed time.

-   **Pause conditions are not met** option: If one or more of the specified pause conditions no longer match, the elapsed time continues to increase. The **Pause conditions are not met** option is selected by default.
-   **Resume conditions are met** option: If one or more of the specified resume conditions match, the elapsed time continues to increase.


</td></tr><tr><td>

Stop condition

</td><td>

Define the conditions under which the SLA completes. If all these conditions match, then the task SLA completes regardless of whether it is breached.

</td></tr><tr><td>

Reset condition

</td><td>

Determines whether the existing task is canceled or completed on task SLA reset. Defines the conditions under which the running SLA is canceled or completed and a new SLA is attached. For a new SLA to be attached, the start condition must match. Reset condition also helps to configure SLAs when the value of any specific field on the task record changes, changes to, or changes from a specific value. For example, the value of the **Location** field in the task record is 101 Broadway East, Seattle,WA. If you set the SLA reset condition as **Location** **changes from** 101 Broadway East, Seattle,WA, any change in the value of the **Location** field resets the SLA of the task record.

</td></tr><tr><td class="sub-head" colspan="2">

Fields that can be added by configuring the form

</td></tr><tr><td>

Condition type

</td><td>

Select the condition type to determine when an SLA attaches, pauses, completes, or resets.

</td></tr></tbody>
</table>
**Parent Topic:**[Service Level Agreement \(SLA\) definition](../concept/c_SLADefinitions.md)

