---
title: Create a change request in Configuration Compliance
description: You can create a change request from a remediation task in the Configuration Compliance application.
locale: en-US
release: australia
product: Configuration Compliance
classification: configuration-compliance
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Use, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Create a change request in Configuration Compliance

You can create a change request from a remediation task in the Configuration Compliance application.

## Before you begin

Role required: user with the itil role

## About this task

As an IT or remediation specialist, create a change request \(CHG\) directly from a remediation task for all the test results in it. Create a change request with pre-populated information to expedite your investigation for vulnerabilities that require manual intervention.

You can create, approve, implement, review, and close change requests directly from remediation tasks that are assigned to you. You can create three types of change requests with pre-populated information from a remediation task:

-   **Standard**

    A pre-authorized change that is low risk, relatively common, and follows a specified procedure or work instruction.

-   **Normal**

    Normal change requests follow a prescriptive process which requires two levels of approval before being implemented, reviewed, and closed.

-   **Emergency**

    A change to resolve a major incident.


The following image illustrates the basic flow for creating a change request from a remediation task. The detailed steps for this flow follow the image.

![States for remediation tasks for creating a change request](../image/cc-CR-CHG.png)

Starting with version 19.0 of Vulnerability Response, you can create change requests for Remediation Tasks from the IT Remediation Workspace. For more information, see [Create a change request in the IT Remediation Workspace](../../vulnerability-response/task/vr-ws-CRs.md).

**Note:** Starting with v14.9 of Configuration Compliance, the following terms have been renamed:

|Terminology prior to v14.9|Terminology v14.9 onwards|
|--------------------------|-------------------------|
|Test Result Group|Remediation Task|
|Group Rules|Remediation Task Rules|
|Policy|Test group|

## Procedure

1.  Navigate to **All** &gt; **Configuration Compliance** &gt; **Remediation Tasks** &gt; **My Open Tasks**.

    The list of remediation tasks assigned to your groups is displayed.

2.  In the Number column, click the remediation task you want to create a change request for.

    You can create change requests from remediation tasks in any states other than **Closed** or **In review**.

    The remediation task record is displayed.

3.  In the upper right of the record, click **Create Change**.

    The change request form is displayed.

4.  Fill in the fields.

    1.  From the list of the **Applies to** field, choose one to continue.

<table id="choicetable_llc_1nk_b4b"><thead><tr><th align="left" id="d419248e247">

Option

</th><th align="left" id="d419248e250">

Description

</th></tr></thead><tbody><tr><td id="d419248e256">

**All active test results in this group**

</td><td>

If selected, all active test results from this remediation task with a state other than **Closed** are added automatically to the change request after you click **Create Change**.

</td></tr><tr><td id="d419248e271">

**All active test results in this group matching a set of conditions**

</td><td>

If selected, the condition builder is displayed. Enter filter criteria to identify the test results that you want for the new change request.An example of a filter you might create would locate only test results from the remediation task that match a specific state and risk score:

State is **Open** and Risk Score is greater than **50**.

</td></tr></tbody>
</table>5.  For the **Add CIs to CR** check box, choose one to continue.

    |Option|Description|
    |------|-----------|
    |**Check box selected**|Default is selected. If the check box is selected, any configuration items \(CIs\) that belong to active test results from this remediation task are added to this change request. The test result transitions to **Awaiting Implementation**.|
    |**Check box cleared**|Clear the check box if you do not want the CIs from the active test results from this remediation task added to the new change request. The remediation task remains in its current state.|

6.  From the list for the **Change type** field, choose one to continue.

<table id="choicetable_vkc_zvk_b4b"><thead><tr><th align="left" id="d419248e344">

Option

</th><th align="left" id="d419248e347">

Description

</th></tr></thead><tbody><tr><td id="d419248e353">

**Emergency**

</td><td>

A change to resolve a major incident.

</td></tr><tr><td id="d419248e362">

**Normal**

</td><td>

A change type that is used to implement any change to a service that is not a standard or emergency change.

</td></tr><tr><td id="d419248e371">

**Standard**

</td><td>

A pre-authorized, low-risk change request that is frequently implemented. Approved standard change requests can be predefined in a catalog of templates to make accessing and requesting a standard change more efficient. If selected, two fields are displayed. Select one from each list to fill in these fields:-   **Change category**: Select a category for the change from your existing catalog, for example, `Hardware`, `Server Standard Changes`, `Software`.
-   **Change template**: Select one available template for change requests with pre-defined supporting tasks from your catalog.
 For more information on ITSM change request categories, templates, and change types, see [Change types](https://www.servicenow.com/docs/access?context=change-types&version=australia&pubname=australia-it-service-management&ft:locale=en-US).

</td></tr></tbody>
</table>    The feature automatically reads the types of change requests that you set up in your catalog in ITSM Change Management. For example, if you change the name for your Standard change requests in ITSM from `Standard` to `Pre-approved`, your new name is automatically displayed in the Change type list on the Create change request form.

7.  The fields in the Change Request Preview section of the form are pre-populated with information from the remediation task.

    If required, edit these fields.

8.  Click **Create Change**.

    The change request is displayed. On the Affected CIs related list, the CIs from the test results that matched your criteria are displayed. If the change request requires approval, the **Request Approval** button is displayed.

    After the change request is created, the test result group moves to the **Awaiting Implementation** state. After the change request for this remediation task is resolved, if there are no other open change requests associated with this remediation task, the remediation task is also moved to the **Resolved** state.

    See [State synchronization between change requests and remediation tasks](cc-cr-state-synch.md) for more information.

    **Note:** You can still manually move change requests and remediation tasks through the states of their life cycles on their respective records with state synchronization enabled, but when the system registers that a change request has changed its state, or you add a change request or remove it from a remediation task, state synchronization potentially can override your manual intervention. However, change requests states do not automatically move the remediation task from the `Closed` or `Deferred` states.


