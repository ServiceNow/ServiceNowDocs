---
title: Resolving a service request case by using playbooks in Public Sector Digital Services
description: You can use playbooks to create cases and to complete the tasks and activities that are needed to resolve specific types of cases.Complete the intake stage as your first step in resolving a case using the Service Request Playbook.Complete the review stage as your second step in resolving a case using the Service Request Playbook.Complete the process stage as your third step in resolving a case using the Service Request Playbook.Complete the decision stage as your last step in resolving a case using the Service Request Playbook.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 8
breadcrumb: [Using Service Request Playbooks, Using Playbooks, Using Public Sector Digital Services, Public Sector Digital Services \(PSDS\)]
---

# Resolving a service request case by using playbooks in Public Sector Digital Services

You can use playbooks to create cases and to complete the tasks and activities that are needed to resolve specific types of cases.

**Note:** Verify that the Service Request Playbook application, which is separate from the Public Sector Digital Services Core application, has been installed and configured. For instructions, see [Install and configure the Service Request Playbook application](configuring-service-request-playbook.md).

By default, the following stages are available to you as a government service agent in the Service Request Playbook in the CSM Configurable Workspace.

-   Intake
-   Review
-   Processing
-   Decision

## Stages in a Service Request Playbook

The Service Request Playbook experience starts with the Intake stage. This stage is the default playbook stage for a new service request case. Use this playbook stage to gather information about the requester and the complaint for the service request case. You can also request additional information from the requester.

The playbook continues with the Review stage. In this stage, you can do the initial troubleshooting on the case, check for similar or duplicate case requests, and determine what services need to be rendered and if a field service agent needs to be dispatched. For more information on the Public Sector Digital Services integration with Field Service Management, see [Integration with Field Service Management](psds-integration-fsm.md).

The playbook continues with the Process stage. In this stage, you can assess resources, request resource approval, create case tasks, and add or request new information before case resolution begins. If a field service agent needs to be dispatched to the service request location, you can create a work order during the process stage. The case status changes to Work in Progress after the field service agent begins work on the service request case. After work has been completed, the case is moved to the Decision stage.

The final stage of the Service Request Playbook is the Decision stage. At the Decision stage, the state of the case is updated from Work in Progress to Ready for Decision after an agent sends in a decision. A notification is sent to the requester that lets them know that a decision has been reached. The requester can then either accept or reject the solution. If the requester accepts the solution, the case is automatically closed. If the requester rejects the solution, the case is reopened, and the agent must propose another solution.

## Complete the Intake Stage in Service Request Playbook

Complete the intake stage as your first step in resolving a case using the Service Request Playbook.

### Before you begin

Role required: admin, sn\_gsm.constituent\_agent, sn\_gsm.business\_agent, sn\_gsm.agency\_agent, sn\_gsm.relationship\_agent, and sn\_gsm.service\_manager

### Procedure

1.  In the CSM Configurable Workspace, navigate to **Lists** &gt; **Service Request case list** &gt; **All**.

2.  Select **New**.

    The Service Request playbook opens and initiates the first activity for collecting the request details

3.  On the Enter Request Details activity card, fill in the information.

4.  Select **Save**.

    A case is created with the service request information. The case number is added to the tab and the first activity in the Intake stage is marked as complete. The second activity in this stage is highlighted as the current activity. If you have enabled the Similar Records UI activity, this will display as the second activity. For more information, see [Configure the Similar Records Activity UI in Service Request Playbook](../task/psds-srp-configure-similar-records.md).

5.  Review the similar records that are displayed in the Similar Records Activity UI, and determine whether any of them are a duplicate of the current case.

    -   If the current case is a duplicate of any of the cases displayed in the Similar Records UI, select **Mark as Primary Case**, then select **Move to Decision**.
    -   If the current case is not a duplicate of any of the cases displayed in the Similar Records UI, select **Existing Case Check Done** to move to the next activity.
6.  Review the details of the case and make updates if needed.

7.  Select **Submit**.

8.  Select **Move to review**.

    The Intake stage is now complete and the case is moved to the Review stage.


## Complete the Review Stage in Service Request Playbook

Complete the review stage as your second step in resolving a case using the Service Request Playbook.

### Before you begin

Role required: admin, sn\_gsm.constituent\_agent, sn\_gsm.business\_agent, sn\_gsm.agency\_agent, sn\_gsm.relationship\_agent, and sn\_gsm.service\_manager

### Procedure

1.  In the contextual side panel, check for duplicate cases using the Related records feature in the contextual side panel.

2.  Do one of the following actions depending on whether or not you have duplicate cases.

<table id="choicetable_lk3_nsm_gwb"><thead><tr><th align="left" id="d24761e363">

Options

</th><th align="left" id="d24761e366">

Steps

</th></tr></thead><tbody><tr><td id="d24761e372">

**If there are no duplicate cases**

</td><td>

Select **Request inspection**, then check the box to confirm that there are no similar service requests.

</td></tr><tr><td id="d24761e384">

**If there are duplicate cases**

</td><td>

1.  In the Parent field, select the search icon \( ![Search icon.](../image/activity-stream-search-icon-psds.png)\) and then select the duplicate case.
2.  Select **Mark as duplicate** and then select **Move to decision** to skip the Process stage to move the case directly to the Decision stage. Select again to confirm.

In the Decision stage, the Resolution code is `Void/Cancelled, Duplicate Issue` by default.

3.  Resolve the case and notify constituents by selecting **Propose solution**.
4.  If the solution doesn't work, select **Repropose solution** to delete the existing solution and then resubmit the case. You’re redirected to the Decision stage, where you can edit any field. Submit the updated solution and notify constituents by selecting **Propose solution**. After a solution has been proposed, the state of the case changes to Resolved.


</td></tr></tbody>
</table>3.  Fill in the Inspect and report case form.

    For more information on how Public Sector Digital Services integrates with Field Service Management, see [Integration with Field Service Management](psds-integration-fsm.md).

4.  Do one of the following actions depending on whether a field service agent must be dispatched to the service request location.

<table id="choicetable_srl_gtm_gwb"><thead><tr><th align="left" id="d24761e479">

Option

</th><th align="left" id="d24761e482">

 

</th></tr></thead><tbody><tr><td id="d24761e487">

**If a field service agent must be dispatched**

</td><td>

1.  Select **Create work order** if a field service agent must be dispatched to the service request location to resolve the issue.
2.  Fill in the details of the work order request.

**Note:** Agents can't proceed with the rest of the playbook until the work order is complete.

3.  Once the work order has been fulfilled, select **Move to process** to move to the next activity.


</td></tr><tr><td id="d24761e516">

**If no field service agent must be dispatched**

</td><td>

If a field service agent doesn't need to be dispatched to the service request location, or if Field Service Management hasn't yet been integrated with Public Sector Digital Services, select **Record findings** to go to the next activity.

</td></tr></tbody>
</table>5.  Fill in the Record findings case form.

6.  Verify if any open case tasks need to be closed, and then select **Move to process**.

    The Review stage is now complete and the case is moved to the Process stage.


## Complete the Process Stage in Service Request Playbook

Complete the process stage as your third step in resolving a case using the Service Request Playbook.

### Before you begin

Role required: admin, sn\_gsm.constituent\_agent, sn\_gsm.business\_agent, sn\_gsm.agency\_agent, sn\_gsm.relationship\_agent, and sn\_gsm.service\_manager

### Procedure

1.  Fill in the Assess resources case form.

2.  Do one of the following actions depending on whether a resource approval is required to proceed.

<table id="choicetable_tpm_25m_gwb"><thead><tr><th align="left" id="d24761e624">

Options

</th><th align="left" id="d24761e627">

Steps

</th></tr></thead><tbody><tr><td id="d24761e633">

**If a resource approval is required**

</td><td>

1.  Select **Request approval**. The case moves to the **Approve resources** activity, where an approval record case task is created, and each approver can approve or reject the proposed conditions.
2.  After all approvals have been received, select **Start work** to move to the **Perform work** activity.


</td></tr><tr><td id="d24761e663">

**If a resource approval is not required**

</td><td>

If no approvals are needed, select **Start work** to bypass the **Approve resources** activity. The case is moved to the **Perform work** activity.

</td></tr></tbody>
</table>3.  Fill in the Perform work case form.

4.  Do one of the following actions depending on whether a field service agent must be dispatched to the service request location.

<table id="choicetable_tgk_p5m_gwb"><thead><tr><th align="left" id="d24761e696">

Options

</th><th align="left" id="d24761e699">

Steps

</th></tr></thead><tbody><tr><td id="d24761e705">

**If a field service agent must be dispatched to the request location**

</td><td>

1.  Select **Create work order**.
2.  Fill in the required information and select **Submit**.


</td></tr><tr><td id="d24761e729">

**If no field service agent must be dispatched**

</td><td>

If no field service agent must be dispatched to the service request location, or if Field Service Management hasn't yet been integrated with Public Sector Digital Services, select **Mark complete.**

</td></tr></tbody>
</table>5.  Verify that everything is correct and that you’ve added all your comments.

6.  Select **Move to decision**, and confirm again when prompted.

    The Process Stage is complete and the case is moved to the Decision stage.


## Complete the Decision Stage in Service Request Playbook

Complete the decision stage as your last step in resolving a case using the Service Request Playbook.

### Before you begin

Role required: admin, sn\_gsm.constituent\_agent, sn\_gsm.business\_agent, sn\_gsm.agency\_agent, sn\_gsm.relationship\_agent, and sn\_gsm.service\_manager

### Procedure

1.  Fill in the Resolve case form.

2.  Select **Propose solution**.

    All case tasks must be closed before an agent can propose a solution to the case.

    A notification is sent to the constituent that lets them know that a decision has been reached. The constituent can either accept or reject the solution. If the constituent accepts the solution, the case is automatically closed. If the constituent rejects the solution, the case is reopened, and the agent must propose another solution.


