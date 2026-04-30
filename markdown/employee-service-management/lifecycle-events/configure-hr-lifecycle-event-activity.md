---
title: Configure a lifecycle event activity
description: Create or modify a lifecycle event activity. Lifecycle Events activities can be approvals, employee tasks, fulfiller activities, notifications, flows, content, or activity containers.Configure a lifecycle event activity that is an approval. Approvals create a to-do for the specified approvers to approve or reject.Configure a lifecycle event activity that is a task for an employee. Employee tasks are assigned to the subject person of the lifecycle event case.Configure a lifecycle event activity that is for a fulfiller. Fulfiller activities are assigned to an agent or fulfiller in a department such as HR, IT, or Facilities.Configure a lifecycle event activity that is a notification. Notifications automate the sending of an email to the specified recipients.Use flow activity parameters on a lifecycle event activity to automatically populate values from a subflow within an activity.Configure a lifecycle event activity that uses a subflow.Use activity field mappings to map information from a field on a table, custom text, or a custom script to a flow input from a subflow.Configure a lifecycle event activity to schedule content. This activity type enables you to deliver relevant and tailored content to employees as part of the lifecycle event. For example, you can push company-related information or a first day at work banner to new hires as part of their onboarding.Configure a lifecycle event activity that is a container for a group of activities. This activity type enables you to manage the dependencies of activities within an activity set. You can use activity containers to order activities, in parallel or sequence, as well as configure multiple activity containers within an activity set.Configure a lifecycle event activity that is a pulse survey. Pulse surveys capture employee feedback.There are multiple ways you can move an activity within an activity set.You can reorder an activity within an activity set for a lifecycle event using different methods.For a lifecycle event case, you can trigger or create an activity from an activity that is in another activity set.
locale: en-US
release: xanadu
product: Lifecycle Events
classification: lifecycle-events
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 33
breadcrumb: [Configure a lifecycle event, Building a lifecycle event, Lifecycle Events, HR Service Delivery, Employee Service Management]
---

# Configure a lifecycle event activity

Create or modify a lifecycle event activity. Lifecycle Events activities can be approvals, employee tasks, fulfiller activities, notifications, flows, content, or activity containers.

## Before you begin

Role required: sn\_hr\_le.activity\_writer and membership in the owning group that owns the activity.

Each activity must be associated with an owning group. If the activity has a targeted audience, you can use audience records to define the conditions or criteria that the subject person of a lifecycle event case must meet for the activity to trigger on their behalf. Each activity is associated with a single activity set.

## Procedure

1.  Navigate to **All** &gt; **Lifecycle Events** &gt; **Administration** &gt; **Manage Lifecycle Events**, and open a record.

2.  Click the **Activity Sets** tab to access the lifecycle event builder.

3.  Create a new or modify an existing activity.

    -   To create a new activity, click **Add Activity**.
    -   To modify an existing activity, hover over the activity and click **Edit Activity**.
    ![Use the lifecycle event builder to create new or modify existing activities.](../image/le-builder-configure-activities.png)

4.  On the Activity form, set the **Activity type** field to one of the following:

    -   Approval
    -   Employee task
    -   Fulfiller activity
    -   Notification
    -   Flow
    -   Content
    -   Activity container
    -   Pulse survey
    For each activity type, follow the applicable task.

    **Warning:** An LE activity \(fulfiller activity\) for an HR service that has the same LE type as the LE case can cause a loop that could cause a memory issue.


**Parent Topic:**[Configure a lifecycle event](configure-hr-lifecycle-event-type.md)

## For an approval

Configure a lifecycle event activity that is an approval. Approvals create a to-do for the specified approvers to approve or reject.

### Before you begin

Role required: sn\_hr\_le.activity\_writer and membership in the owning group that owns the activity.

### Procedure

1.  On the Activity form, set the **Activity type** field to `Approval`.

2.  Fill in the fields on the form, as appropriate.

<table id="table_ldl_tqc_2hb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title

</td><td>

Name of the lifecycle event activity.

</td></tr><tr><td>

Description

</td><td>

Description of the lifecycle event activity.

</td></tr><tr><td>

Activity type

</td><td>

Set the value to `Approval`.

</td></tr><tr><td>

Active

</td><td>

Option to activate the activity for use.

</td></tr><tr><td>

Owning group

</td><td>

Owning group that the activity is associated with. **Note:**

-   Owning groups control who owns a lifecycle event activity. To learn more, see [Configure an owning group for a lifecycle event](configure-lifecycle-event-owning-group.md).
-   To create, update, or delete an activity, you must be both a member of the associated owning group and have the sn\_hr\_le.activity\_writer role.


</td></tr><tr><td>

Activity set

</td><td>

Activity set that the activity is associated with.

</td></tr><tr><td>

Audience

</td><td>

Defines whether the activity should trigger for the lifecycle event case. You can apply one or more audience records. The subject person of the lifecycle event case must meet the conditions or criteria of one audience record for the activity to trigger in the case. If no audience record is selected, then the activity for the activity to trigger in the case. The audience criteria for an activity set applies first. When the audience criteria is met, the activity set executes. The audience at the activity level is then checked and executed.

 You cannot set an audience for activity sets that have a trigger type of Rescind.

 **Note:** Audience records define the conditions or criteria that a user must meet.

</td></tr></tbody>
</table>3.  In the **Approvers** related list, define the approvers for the lifecycle event activity.

    |Field|Description|
    |-----|-----------|
    |Approver groups|Groups to approve the activity.|
    |Approver users|Users to approve the activity.|
    |Approvers from case|User from the lifecycle event case to approve the activity.|

4.  In the **Approval Options** related list, set how the activity is approved.

    |Field|Description|
    |-----|-----------|
    |Wait for|Select one of the following actions for when an approval is completed:|
    |Anyone to approve|Only one person is required to approve the HR activity.|
    |Everyone to approve|Everyone assigned to the HR activity is required to approve it. If one person rejects, the Assigned to person receives a message with a link to select a substitute approver.|
    |First response from anyone|The first person to respond \(approve or reject\) to the activity determines the state.|
    |On rejection|Select one of the following actions for when an approval is rejected:|
    |Allow resubmit of approvals:|An HR agent can resubmit for approval. The Assigned to person receives a message on the case with a link to resubmit approval requests. All approvers are resubmitted the approval request.|
    |Close incomplete|When the HR service is rejected, change the **State** of the case or task to **Closed and Incomplete**.|
    |Missing any approver|Select one of the following actions for when any approver is missing:|
    |Select replacements|When an approver is missing, the Assigned to person can select a replacement. If the activity is configured to have the Opened for Manager to approve, but the Opened for person has no manager assigned, the activity has a missing approver. If **Select replacements** is selected in the **Missing any approver** field, the Assigned to person receives a message with a link to select a substitute approver.|
    |Skip missing|Bypass any missing approver and continue.|
    |Close incomplete|Change the state of the case or task to **Closed Incomplete** when there is a missing approver.|
    |Missing all approvers|Select one of the following actions for when all approvers are missing:|
    |Select replacements|When all approvers are missing, the Assigned to person can select replacements. If the activity is configured to have the Opened for Manager to approve, but the Opened for person has no manager assigned, the activity has a missing approver. If **Select replacements** is selected in the **Missing any approver** field, the Assigned to person receives a message with a link to select a substitute approver.|
    |Close incomplete|Change the state of the case or task to **Closed and Incomplete** when all approvers are missing.|

5.  Click **Submit** or **Update**.


## For an employee task

Configure a lifecycle event activity that is a task for an employee. Employee tasks are assigned to the subject person of the lifecycle event case.

### Before you begin

Role required: sn\_hr\_le.activity\_writer and membership in the owning group that owns the activity.

### Procedure

1.  On the Activity form, set the **Activity type** field to `Employee`.

2.  Fill in the fields on the form, as appropriate.

<table id="table_wbz_ksq_42b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title

</td><td>

Name of the lifecycle event activity.

</td></tr><tr><td>

Description

</td><td>

Description of the lifecycle event activity.

</td></tr><tr><td>

Activity type

</td><td>

Set the value to `Employee`.

</td></tr><tr><td>

HR task template

</td><td>

HR task template to use with the activity.**Note:** An HR task template automatically populates fields on the HR task form when the task is generated. See [Configure an HR task template](configure-hr-task-template.md) for more information.

</td></tr><tr><td>

Wait for generated task to complete

</td><td>

Option to wait for the generated task to complete before the activity closes. This field appears when you select one of the following task types in the HR task template form. If selected:-   **HR Service**: Completion of the HR task results in the creation of an HR case. The HR case must complete in order for the activity to close.
-   **Submit Catalog Item**: Completion of the HR task results in the creation of a request. The request must complete in order for the activity to close.
-   **Submit Order Guide**: Completion of the HR task results in the creation of an IT request. The IT request must complete in order for the activity to close.
 **Note:**

-   The condition for closure depends on the activity type, and can be modified.
-   If selected, the change applies only to new lifecycle event cases. Activities in existing cases will not wait for the generated task to complete before the activity closes.


</td></tr><tr><td>

Active

</td><td>

Option to activate the activity for use.

</td></tr><tr><td>

Owning group

</td><td>

Owning group that the activity is associated with. **Note:**

-   Owning groups control who owns a lifecycle event activity. To learn more, see [Configure an owning group for a lifecycle event](configure-lifecycle-event-owning-group.md).
-   To create, update, or delete an activity, you must be both a member of the associated owning group and have the sn\_hr\_le.activity\_writer role.


</td></tr><tr><td>

Activity set

</td><td>

Activity set that the activity is associated with.

</td></tr><tr><td>

Use badge from HR service configuration

</td><td>

\(If for the associated HR task template, the **HR task type** value is **HR service**\) Option to use the badge that is associated with the parent HR service.

</td></tr><tr><td>

Badge

</td><td>

Badge that the fulfiller activity type is associated with. **Note:** Badges display on the portal to indicate to the employee which department is fulfilling that activity. See [Configure an HR badge](CreateModHRBadges.md) for more information.

</td></tr><tr><td>

Audience

</td><td>

Defines whether the activity should trigger for the lifecycle event case. You can apply one or more audience records. The subject person of the lifecycle event case must meet the conditions or criteria of one audience record for the activity to trigger in the case. If no audience record is selected, then the activity for the activity to trigger in the case. The audience criteria for an activity set applies first. When the audience criteria is met, the activity set executes. The audience at the activity level is then checked and executed.

 You cannot set an audience for activity sets that have a trigger type of Rescind.

 **Note:** Audience records define the conditions or criteria that a user must meet.

</td></tr></tbody>
</table>3.  Click **Save**.

4.  In the associated HR task template, when the **HR task type** value is **HR service**, **Submit catalog item**, or **Submit order guide**, in the **Activity Field Mappings** section, you can map fields from the parent lifecycle event case to the appropriate variables on the child activity that is generated when the employee activity is triggered.

    1.  Click **New** or open a record.

    2.  Fill in the fields on the form.

<table id="table_g2p_5jw_bhb"><thead><tr><th>

Field

</th><th colspan="2">

Description

</th></tr></thead><tbody><tr><td>

Activity

</td><td colspan="2">

This field is automatically set to the name of the associated lifecycle event activity.

</td></tr><tr><td>

Map from table

</td><td colspan="2">

Source table that the activity field is mapped from. This field is automatically set to the name of the HR case table that the parent lifecycle event case is associated with.

</td></tr><tr><td rowspan="3">

Map from

</td><td colspan="2">

Map from type. Select one of the following:

</td></tr><tr><td>

Field

</td><td>

Map from a field. In the **Map from field** field, select the field in the source table that the activity field is mapped from.**Note:** Make sure that the data type of the field being mapped from is the same as the data type of the field being mapped to.

</td></tr><tr><td>

Custom text

</td><td>

Map from custom text. In the **Custom Text** field, provide a string value. Custom text can be static or include variables that are pulled from the source table. For example, you can provide a short description for an IT request, such as, "Provide laptop for new hire: $\{subject\_person\}."

</td></tr><tr><td>

Map to variable

</td><td colspan="2">

Variable that the activity field is mapped to.**Note:** Make sure that the data type of the field being mapped from is the same as the data type of the field being mapped to.

</td></tr></tbody>
</table>    3.  Click **Submit** or **Update**.

    4.  Repeat the process as needed.

5.  Click **Update**.


## For a fulfiller activity

Configure a lifecycle event activity that is for a fulfiller. Fulfiller activities are assigned to an agent or fulfiller in a department such as HR, IT, or Facilities.

### Before you begin

Role required: sn\_hr\_le.activity\_writer and membership in the owning group that owns the activity.

### Procedure

1.  On the Activity form, set the **Activity type** field to `Fulfiller`.

2.  Fill in the fields on the form, as appropriate.

<table id="table_wbz_ksq_42b"><thead><tr><th>

Field

</th><th colspan="2">

Description

</th></tr></thead><tbody><tr><td>

Title

</td><td colspan="2">

Name of the lifecycle event activity.

</td></tr><tr><td>

Description

</td><td colspan="2">

Description of the lifecycle event activity.

</td></tr><tr><td>

Activity type

</td><td colspan="2">

Set the value to `Fulfiller`.

</td></tr><tr><td rowspan="7">

Fulfiller activity

</td><td colspan="2">

Select one of the following fulfiller activity types:**Note:** You can control the different fulfiller activity types that appear here. See [Configure an activity configuration for a lifecycle event](configure-lifecycle-event-fulfiller-activity-configuration.md) for more information.

</td></tr><tr><td>

Automated Order Guide

</td><td>

\(Lifecycle Events for Enterprise only\) An order guide fulfills the activity. In the **Order guide** field, select the order guide to use.**Note:** An order guide submits a single service catalog request that generates several items. See [Order guides](https://www.servicenow.com/docs/access?context=c_ServiceCatalogOrderGuides&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) for more information.

</td></tr><tr><td>

Catalog Item

</td><td>

\(Lifecycle Events for Enterprise only\) A catalog item fulfills the activity. In the **Catalog item** field, select the catalog item to use.**Note:** A catalog item is a good or service. See [Service catalog items](https://www.servicenow.com/docs/access?context=c_IntroductionToCatalogItems&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) for more information.

</td></tr><tr><td>

Flow

</td><td>

A flow fulfills the activity. In the **Flow** field, select the flow to use.**Note:** A flow automates a process with a sequence of reusable actions. See [Flow designer](https://www.servicenow.com/docs/access?context=flow-designer&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US) for more information.

</td></tr><tr><td>

HR Service

</td><td>

An HR service fulfills the activity. In the **HR service** field, select the HR service to use.**Note:** HR services are the requests and assistance an HR organization provides its employees. See [HR services](../concept/hr-service-administration.md) for more information.

</td></tr><tr><td>

HR Task

</td><td>

An HR task fulfills the activity. In the **HR task template** field, select the HR task template to use.**Note:** An HR task template automatically populates fields on the HR task form when the task is generated. See [Configure an HR task template](configure-hr-task-template.md) for more information.

</td></tr><tr><td>

Incident

</td><td>

\(Lifecycle Events for Enterprise only\) An incident fulfills the activity. In the **Template** field, select the incident template to use.**Note:** An incident template automatically populates fields on the Incident form. See [Incident Management](https://www.servicenow.com/docs/access?context=c_IncidentManagement&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Active

</td><td colspan="2">

Option to activate the activity for use.

</td></tr><tr><td>

Use badge from HR service configuration

</td><td colspan="2">

\(If for the associated HR task template, the **HR task type** value is **HR service**\) Option to use the badge that is associated with the parent HR service.

</td></tr><tr><td>

Badge

</td><td colspan="2">

Badge that the fulfiller activity type is associated with. **Note:** Badges display on the portal to indicate to the employee which department is fulfilling that activity. See [Configure an HR badge](CreateModHRBadges.md) for more information.

</td></tr><tr><td>

Owning group

</td><td colspan="2">

Owning group that the activity is associated with. **Note:**

-   Owning groups control who owns a lifecycle event activity. To learn more, see [Configure an owning group for a lifecycle event](configure-lifecycle-event-owning-group.md).
-   To create, update, or delete an activity, you must be both a member of the associated owning group and have the sn\_hr\_le.activity\_writer role.


</td></tr><tr><td>

Activity set

</td><td colspan="2">

Activity set that the activity is associated with.

</td></tr><tr><td>

Audience

</td><td colspan="2">

Defines whether the activity should trigger for the lifecycle event case. You can apply one or more audience records. The subject person of the lifecycle event case must meet the conditions or criteria of one audience record for the activity to trigger in the case. If no audience record is selected, then the activity for the activity to trigger in the case. The audience criteria for an activity set applies first. When the audience criteria is met, the activity set executes. The audience at the activity level is then checked and executed.

 You cannot set an audience for activity sets that have a trigger type of Rescind.

 **Note:** Audience records define the conditions or criteria that a user must meet.

</td></tr></tbody>
</table>3.  Click **Save**.

4.  In the **Activity Field Mappings** section, you can map fields from the parent lifecycle event case to the appropriate fields on the child activity that is generated when the fulfiller activity is triggered.

    **Note:** This section inherits any mappings from the associated fulfiller activity type. You can use the default fulfiller activity type mappings as-is or further modify them.

    1.  Click **New** or open a record.

    2.  Fill in the fields on the form.

<table id="table_g2p_5jw_bhb"><thead><tr><th>

Field

</th><th colspan="2">

Description

</th></tr></thead><tbody><tr><td>

Activity

</td><td colspan="2">

This field is automatically set to the name of the associated lifecycle event activity.

</td></tr><tr><td>

Map from table

</td><td colspan="2">

Source table that the activity field is mapped from. This field is automatically set to the name of the HR case table that the parent lifecycle event case is associated with.

</td></tr><tr><td rowspan="3">

Map from

</td><td colspan="2">

Map from type. Select one of the following:

</td></tr><tr><td>

Field

</td><td>

Map from a field. In the **Map from field** field, select the field in the source table that the activity field is mapped from.**Note:** Make sure that the data type of the field being mapped from is the same as the data type of the field being mapped to.

</td></tr><tr><td>

Custom text

</td><td>

Map from custom text. In the **Custom Text** field, provide a string value. Custom text can be static or include variables that are pulled from the source table. For example, you can provide a short description for an IT request, such as, "Provide laptop for new hire: $\{subject\_person\}."

</td></tr><tr><td>

Map to table

</td><td colspan="2">

Target table that the activity field is mapped to. This field is automatically set to the name of the table that the child activity is associated with.

</td></tr><tr><td>

Map to field

</td><td colspan="2">

Field in the target table that the activity field is mapped to.**Note:** Make sure that the data type of the field being mapped from is the same as the data type of the field being mapped to.

</td></tr></tbody>
</table>    3.  Click **Submit** or **Update**.

    4.  Repeat the process as needed.

5.  Click **Update**.


## For a notification

Configure a lifecycle event activity that is a notification. Notifications automate the sending of an email to the specified recipients.

### Before you begin

Role required: sn\_hr\_le.activity\_writer and membership in the owning group that owns the activity.

### Procedure

1.  On the Activity form, set the **Activity type** field to `Notification`.

2.  Fill in the fields on the form, as appropriate.

<table id="table_wbz_ksq_42b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title

</td><td>

Name of the lifecycle event activity.

</td></tr><tr><td>

Description

</td><td>

Description of the lifecycle event activity.

</td></tr><tr><td>

Activity type

</td><td>

Set the value to `Notification`.

</td></tr><tr><td>

Email template

</td><td>

Select an existing or create a new email template.

</td></tr><tr><td>

From

</td><td>

Provide the name of the sender.

</td></tr><tr><td>

Active

</td><td>

Option to activate the activity for use.

</td></tr><tr><td>

Owning group

</td><td>

Owning group that the activity is associated with. **Note:**

-   Owning groups control who owns a lifecycle event activity. To learn more, see [Configure an owning group for a lifecycle event](configure-lifecycle-event-owning-group.md).
-   To create, update, or delete an activity, you must be both a member of the associated owning group and have the sn\_hr\_le.activity\_writer role.


</td></tr><tr><td>

Activity set

</td><td>

Activity set that the activity is associated with.

</td></tr><tr><td>

Audience

</td><td>

Defines whether the activity should trigger for the lifecycle event case. You can apply one or more audience records. The subject person of the lifecycle event case must meet the conditions or criteria of one audience record for the activity to trigger in the case. If no audience record is selected, then the activity for the activity to trigger in the case. The audience criteria for an activity set applies first. When the audience criteria is met, the activity set executes. The audience at the activity level is then checked and executed.

 You cannot set an audience for activity sets that have a trigger type of Rescind.

 **Note:** Audience records define the conditions or criteria that a user must meet.

</td></tr></tbody>
</table>3.  In the **Recipients** related list, define the notification recipients for the lifecycle event activity.

    |Field|Description|
    |-----|-----------|
    |Recipient users|Users to receive the email notification.|
    |Recipient groups|Groups to receive the email notification.|
    |Users/Groups on case|User fields from the lifecycle event case to receive the email notification.|

4.  Click **Submit** or **Update**.


## Flow activity parameters

Use flow activity parameters on a lifecycle event activity to automatically populate values from a subflow within an activity.

You can configure subflows for a lifecycle event and pass the values for the input parameters of the subflow within the activity.

Having the ability to call any subflow from a lifecycle event activity provides you with a low code or no code configuration.

Calling subflows from a lifecycle event activity provides an enterprise-wide workflow you can use to interact with third-party applications at a specific point in a lifecycle event.

For more information, see [Flows](https://www.servicenow.com/docs/access?context=flows&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).

### Use cases

You can use flow activity parameters for:

<table id="table_pjp_hdf_ymb"><thead><tr><th>

Subflow

</th><th>

Parameters

</th></tr></thead><tbody><tr><td>

Terminate employee in Workday.

</td><td>

-   Employee: Subject person
-   End Date: Subject person HR Profile.Employment End Date

</td></tr></tbody>
</table><table id="table_pr1_4df_ymb"><thead><tr><th>

Subflow

</th><th>

Parameters

</th></tr></thead><tbody><tr><td>

Mark employee as a no show in Workday. \(Employee accepted an offer of employment, but at some point decided to back out of agreement.\)

</td><td>

-   Employee: Subject person
-   Reason: Reason for no show

</td></tr></tbody>
</table><table id="table_vzp_k2f_ymb"><thead><tr><th>

Subflow

</th><th>

Parameters

</th></tr></thead><tbody><tr><td>

Switch primary job

</td><td>

-   Employee: Subject person
-   Job: Subject person job

</td></tr></tbody>
</table>For more information, see [Subflows](https://www.servicenow.com/docs/access?context=subflows&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).

### Map activity fields and input parameters

You can use fields from a table to map your activity field to an input parameter.

Or, you can map activity fields to an input parameter using a custom script.

### For a flow

Configure a lifecycle event activity that uses a subflow.

#### Before you begin

Role required: sn\_hr\_le.activity\_writer and membership in the owning group that owns the activity.

#### Procedure

1.  On the Activity form, set the **Activity type** field to `Flow`.

2.  Fill in the fields on the form, as appropriate.

<table id="table_wbz_ksq_42b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title

</td><td>

Name of the lifecycle event activity.

</td></tr><tr><td>

Description

</td><td>

Description of the lifecycle event activity.

</td></tr><tr><td>

Activity type

</td><td>

Set the value to `Flow`.

</td></tr><tr><td>

Flow

</td><td>

Subflow to use with the activity.**Important:**

-   Only the **Switch primary job** subflow that is used to [support multiple jobs in a lifecycle event](adopt-jobs-table.md) is available to use out-of-box.
-   To use a different subflow with the activity, additional configuration is required. See the [Implementing multiple subflows in an LE activity \[KB0817520](https://support.servicenow.com/kb_view.do?sysparm_article=KB0817520) article in the HI Knowledge Base for more information.


</td></tr><tr><td>

Active

</td><td>

Option to activate the activity for use.

</td></tr><tr><td>

Badge

</td><td>

Badge that the fulfiller activity type is associated with. **Note:** Badges display on the portal to indicate to the employee which department is fulfilling that activity. See [Configure an HR badge](CreateModHRBadges.md) for more information.

</td></tr><tr><td>

Owning group

</td><td>

Owning group that the activity is associated with. **Note:**

-   Owning groups control who owns a lifecycle event activity. To learn more, see [Configure an owning group for a lifecycle event](configure-lifecycle-event-owning-group.md).
-   To create, update, or delete an activity, you must be both a member of the associated owning group and have the sn\_hr\_le.activity\_writer role.


</td></tr><tr><td>

Activity set

</td><td>

Activity set that the activity is associated with.

</td></tr><tr><td>

Audience

</td><td>

Defines whether the activity should trigger for the lifecycle event case. You can apply one or more audience records. The subject person of the lifecycle event case must meet the conditions or criteria of one audience record for the activity to trigger in the case. If no audience record is selected, then the activity for the activity to trigger in the case. The audience criteria for an activity set applies first. When the audience criteria is met, the activity set executes. The audience at the activity level is then checked and executed.

 You cannot set an audience for activity sets that have a trigger type of Rescind.

 **Note:** Audience records define the conditions or criteria that a user must meet.

</td></tr></tbody>
</table>3.  Click **Save**.

    The **Activity Field Mappings** and **Rescind activities** tabs appear. These fields pass from the subflow.


### Configure activity field mapping

Use activity field mappings to map information from a field on a table, custom text, or a custom script to a flow input from a subflow.

#### Before you begin

Role required: sn\_hr\_le.activity\_writer

#### About this task

The activity field mappings pass fields from the subflow you selected when configuring the lifecycle event activity.

#### Procedure

1.  Navigate to **All** &gt; **Lifecycle Events** &gt; **Manage Activities**.

2.  Select an activity that has **Flow** as the **Activity type**.

    For more information, see [For a flow](configure-hr-lifecycle-event-activity.md#).

3.  Click the **Activity Field Mappings** tab.

4.  Click an activity field mapping.

5.  Fill in the fields on the form, as appropriate.

<table id="table_ek5_t1x_zmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Activity

</td><td>

The activity you are creating field mappings for.

</td></tr><tr><td>

Map from table

</td><td>

The table you want to map values from.

</td></tr><tr><td>

Map from

</td><td>

How you want to map values from the table you selected. Valid values are:-   Field
-   Custom Text
-   Custom Script


</td></tr><tr><td>

Map from field

</td><td>

The field from the table you selected that you want to map your activity field.For example, you can select the Activity \[sn\_hr\_le\_case\] table and the subject-person field from that table to map to the User flow input.

 Appears when you select **Field** from the **Map from field**.

</td></tr><tr><td>

Custom text

</td><td>

The text you want to map to your activity field.Appears when you select **Custom Text** from the **Map from field**.

</td></tr><tr><td>

Script

</td><td>

The script you want to map to your activity field.Appears when you select **Custom Script** from the **Map from field**.

</td></tr><tr><td>

Map to flow input

</td><td>

The input parameter from your subflow that you are mapping from a field from a table, custom text, or custom script.For more information, see [For a flow](configure-hr-lifecycle-event-activity.md#).

</td></tr><tr><td>

Input mandatory

</td><td>

Indicates if the input is required and reflects the settings from the subflow you selected.For more information, see [Subflows](https://www.servicenow.com/docs/access?context=subflows&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).

</td></tr></tbody>
</table>6.  Click **Submit** or **Update**.


## For content

Configure a lifecycle event activity to schedule content. This activity type enables you to deliver relevant and tailored content to employees as part of the lifecycle event. For example, you can push company-related information or a first day at work banner to new hires as part of their onboarding.

### Before you begin

Role required: sn\_cd.content\_manager, sn\_hr\_le.activity\_writer, and membership in the owning group that owns the activity.

### Procedure

1.  On the Activity form, set the **Activity type** field to `Content`.

2.  Fill in the fields on the form, as appropriate.

<table id="table_wbz_ksq_42b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title

</td><td>

Name of the lifecycle event activity.

</td></tr><tr><td>

Description

</td><td>

Description of the lifecycle event activity.

</td></tr><tr><td>

Activity type

</td><td>

Set the value to `Content`.

</td></tr><tr><td>

Template

</td><td>

Schedule content template to use with the activity.**Note:** A schedule content template schedules and delivers content to users as part of a lifecycle event. See [Configure a schedule content template for a lifecycle event activity](configure-schedule-content-template-for-lifecycle-event.md) for more information.

</td></tr><tr><td>

Active

</td><td>

Option to activate the activity for use.

</td></tr><tr><td>

Owning group

</td><td>

Owning group that the activity is associated with. **Note:**

-   Owning groups control who owns a lifecycle event activity. To learn more, see [Configure an owning group for a lifecycle event](configure-lifecycle-event-owning-group.md).
-   To create, update, or delete an activity, you must be both a member of the associated owning group and have the sn\_hr\_le.activity\_writer role.


</td></tr><tr><td>

Audience

</td><td>

Defines whether the activity should trigger for the lifecycle event case. You can apply one or more audience records to target the content to the subject person, opened for person, or a person working on the lifecycle event case.

 The audience criteria for an activity set applies first. When the audience criteria is met, the activity set executes. The audience at the activity level is then checked and executed.

 You cannot set an audience for activity sets that have a trigger type of Rescind.

 **Note:** Audience records define the conditions or criteria that a user must meet.

</td></tr></tbody>
</table>3.  In the **Activity Field Mappings** section, you can map fields from the parent lifecycle event case to the appropriate fields on the content activity.

    You can use the activity field mappings to define who the content is delivered to, when the content is delivered, how long the content is available for, and more.

    1.  Click **New** or open a record.

    2.  Fill in the fields on the form.

<table id="table_g2p_5jw_bhb"><thead><tr><th>

Field

</th><th colspan="2">

Description

</th></tr></thead><tbody><tr><td>

Activity

</td><td colspan="2">

This field is automatically set to the name of the associated lifecycle event activity.

</td></tr><tr><td>

Map from table

</td><td colspan="2">

Source table that the activity field is mapped from. This field is automatically set to the name of the HR case table that the parent lifecycle event case is associated with.

</td></tr><tr><td rowspan="3">

Map from

</td><td colspan="2">

Map from type. Select one of the following:

</td></tr><tr><td>

Field

</td><td>

Map from a field. In the **Map from field** field, select the field in the source table that the activity field is mapped from.**Note:** Make sure that the data type of the field being mapped from is the same as the data type of the field being mapped to.

</td></tr><tr><td>

Custom text

</td><td>

Map from custom text. In the **Custom Text** field, provide a string value. Custom text can be static or include variables that are pulled from the source table. For example, you can provide a short description for an IT request, such as, "Provide laptop for new hire: $\{subject\_person\}."

</td></tr><tr><td>

Map to table

</td><td colspan="2">

Target table that the activity field is mapped to. This field is automatically set to the name of the table that the child activity is associated with.

</td></tr><tr><td>

Map to field

</td><td colspan="2">

Field in the target table that the activity field is mapped to.**Note:** Make sure that the data type of the field being mapped from is the same as the data type of the field being mapped to.

</td></tr></tbody>
</table>    3.  Click **Submit** or **Update**.

    4.  Repeat the process as needed.

4.  Click **Submit** or **Update**.


## For an activity container

Configure a lifecycle event activity that is a container for a group of activities. This activity type enables you to manage the dependencies of activities within an activity set. You can use activity containers to order activities, in parallel or sequence, as well as configure multiple activity containers within an activity set.

### Before you begin

Role required: sn\_hr\_le.activity\_writer and membership in the owning group that owns the activity.

### Procedure

1.  On the Activity form, set the **Activity type** field to `Activity container`.

2.  Fill in the fields on the form, as appropriate.

<table id="table_wbz_ksq_42b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title

</td><td>

Name of the lifecycle event activity.

</td></tr><tr><td>

Description

</td><td>

Description of the lifecycle event activity.

</td></tr><tr><td>

Activity type

</td><td>

Set the value to `Activity container`.

</td></tr><tr><td>

Active

</td><td>

Option to activate the activity for use.

</td></tr><tr><td>

Owning group

</td><td>

Owning group that the activity is associated with. **Note:**

-   Owning groups control who owns a lifecycle event activity. To learn more, see [Configure an owning group for a lifecycle event](configure-lifecycle-event-owning-group.md).
-   To create, update, or delete an activity, you must be both a member of the associated owning group and have the sn\_hr\_le.activity\_writer role.


</td></tr><tr><td>

Audience

</td><td>

Defines whether the activity should trigger for the lifecycle event case. You can apply one or more audience records. The subject person of the lifecycle event case must meet the conditions or criteria of one audience record for the activity to trigger in the case. If no audience record is selected, then the activity for the activity to trigger in the case. The audience criteria for an activity set applies first. When the audience criteria is met, the activity set executes. The audience at the activity level is then checked and executed.

 You cannot set an audience for activity sets that have a trigger type of Rescind.

 **Note:** Audience records define the conditions or criteria that a user must meet.

</td></tr></tbody>
</table>3.  Right-click the former header and click **Save**.

    The **Member activities** related list appears.

4.  In the **Member activities** related list, create one or more member activities of the following types:

    **Note:**

    -   Member activities inherit the audience of the activity container.
    -   Member activities trigger based on the order number assigned. Activities with the same order number trigger at the same time.
    -   New member activities must be created for each activity container. You cannot move existing activities into an activity container, nor can you move member activities out of the container to use as standalone activities.
    -   Member activities cannot be activity containers. You cannot place an activity container inside another activity container.
    -   Approval
    -   Employee
    -   Fulfiller
    -   Notification
    -   Flow
    -   Content
    For example, this is an activity container to request a credit card. The activity container has three member activities. The first is to approve the credit card request, the second is to submit the request, and the third is to notify relevant groups about the request.

    ![An activity container to request a credit card, with three member activities to approve the request, submit the request, and notify relevant groups.](../image/le-activity-container-example.png)

5.  Click **Update**.


## For a pulse survey

Configure a lifecycle event activity that is a pulse survey. Pulse surveys capture employee feedback.

### Before you begin

Role required:

### Procedure

1.  On the Activity form, set the **Activity type** field to `Pulse Survey`.

2.  Fill in the fields on the form, as appropriate.

<table id="table_ldl_tqc_2hb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title

</td><td>

Name of the lifecycle event activity.

</td></tr><tr><td>

Description

</td><td>

Description of the lifecycle event activity.

</td></tr><tr><td>

Pulse survey

</td><td>

The survey to send.

</td></tr><tr><td>

Pulse user field

</td><td>

The users to whom you want to send the survey. Use the tree picker to select a field.

</td></tr><tr><td>

Active

</td><td>

Option to activate the activity for use.

</td></tr><tr><td>

Owning group

</td><td>

Owning group that the activity is associated with. **Note:**

-   Owning groups control who owns a lifecycle event activity. To learn more, see [Configure an owning group for a lifecycle event](configure-lifecycle-event-owning-group.md).
-   To create, update, or delete an activity, you must be both a member of the associated owning group and have the sn\_hr\_le.activity\_writer role.


</td></tr><tr><td>

Audience

</td><td>

Defines whether the activity should trigger for the lifecycle event case. You can apply one or more audience records. The subject person of the lifecycle event case must meet the conditions or criteria of one audience record for the activity to trigger in the case. If no audience record is selected, then the activity for the activity to trigger in the case. The audience criteria for an activity set applies first. When the audience criteria is met, the activity set executes. The audience at the activity level is then checked and executed.

 You cannot set an audience for activity sets that have a trigger type of Rescind.

 **Note:** Audience records define the conditions or criteria that a user must meet.

</td></tr></tbody>
</table>3.  Click **Submit** or **Update**.


## Moving an activity within an activity set

There are multiple ways you can move an activity within an activity set.

The different methods are:

-   The drag-and-drop feature enables you to move an activity within an activity set or to another activity set.
-   Use the reorder pop-up on an activity and select where you want the activity to reside.
-   Edit the activity and select and save a new activity set or enter a new display order number to reorder an activity within an activity set.
-   You cannot reorder a request activity.

    **Note:** Requests have a grey background around the request card for easier identification.

-   You cannot move an activity above a request activity.
-   If you use the ![Lifecycle event reorder icon](../image/le-reorder-icon.png) to move an activity to another activity set, by default it moves it to the top position of the activity set below any request activities.

### Reorder a life cycle event activity

You can reorder an activity within an activity set for a lifecycle event using different methods.

#### Before you begin

Role required: admin

#### Procedure

1.  Navigate to **All** &gt; **Lifecycle Events** &gt; **Administration** &gt; **Manage Lifecycle Events**.

2.  Select a lifecycle event.

3.  Select the **Activity Sets** tab.

4.  Use the drag-and-drop method to select an activity with your mouse and hold it and drag it to a different location within the same activity set or into another activity set.

    **Note:** The ordering numbers change automatically.

5.  To move an activity, select the Reorder icon \(![Lifecycle event reorder icon](../image/le-reorder-icon.png) from an activity.

    **Note:** If you use the Reorder icon to move an activity to another activity set, by default it moves it to the top position of the activity set below any request activities.

6.  A reorder pop-up appears.

    ![Lifecycle event activity - Reorder](../image/le-reorder-activity.png)

7.  Select a choice with your mouse and release.

    **Note:** The ordering numbers change automatically.

8.  Another way to edit an activity is to select the Edit Activity icon \(![Lifecycle event - Edit Activity icon](../image/le-edit-activity-icon.png)\) on an activity.

    The activity appears in a separate window.![Lifecycle event - Edit activity](../image/le-edit-activity.png)

9.  Edit the **Activity set** and **Display order** fields to change the activity set the activity belongs to and the order it appears.

    **Note:** Requests cannot be reordered.

10. Select **Update**.


## Triggering an activity from upstream activities

For a lifecycle event case, you can trigger or create an activity from an activity that is in another activity set.

Activities in later activity sets can be created based on survey responses in earlier activity sets and for users other than the person the case was created for \(subject person\).

You can create an activity that has a task type of Collect Employee Input and based on the results, another activity is created. In this example, the activity that has a task type of Collect Employee Input is the upstream activity. The activity that is created from this is the downstream activity.

Previously, only the Subject person could answer questions from an activity with a task type of Collect Employee Input \(survey\). For an New Hire Onboarding lifecycle event, the Subject person might not have access to the survey yet. Now, the Opened for, Subject person, or Assigned to can take the survey. This keeps the lifecycle event moving.

-   **Upstream survey creates downstream survey**

    For example, a lifecycle event activity can task a manager with taking a survey.

    -   The survey asks a hiring manager if their new employees require special equipment.
    -   The hiring manager can answer the survey indicating if the new hires require special equipment.
    -   If the answer is yes, a new survey can be created in a downstream activity set that asks what specific safety equipment are required.
    -   Anyone that has access to the original lifecycle event case can answer the second survey requesting specific safety equipment for the new hires.
    -   To configure this activity, associate an HR template that has an HR task type of **Collect Employee Input**. For more information, see [Configure an HR task template](configure-hr-task-template.md) and [Adding an HR task to an HR case](t_ViewAnHRTask.md).
    -   -   **System property**

    The sn\_hr\_core.create\_new\_survey\_instances system property determines if new survey instances are created with each survey task even when an existing survey instance for the same user exists.

    The default value is **True** and indicates multiple survey instances can be created.

    If the value is **False**, when an existing survey instance for the same survey and same user exists, the survey is attached to the survey task.


