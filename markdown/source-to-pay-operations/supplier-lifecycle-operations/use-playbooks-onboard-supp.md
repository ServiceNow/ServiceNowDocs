---
title: Use the supplier onboarding playbook to onboard suppliers
description: Supplier owners and supplier managers can use the supplier onboarding playbook to complete the tasks and activities that are needed to onboard new suppliers.The following table lists the activities in the Registration stage of the Supplier onboarding playbook.The following table lists the activities in the Qualification stage of the Supplier onboarding playbook.The following table lists the activities in the Activation stage of the Supplier onboarding playbook.The following table lists the activities in the Rejection stage of the Supplier onboarding playbook.
locale: en-US
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Create a supplier, Using Source-to-Pay Workspace, Use, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Use the supplier onboarding playbook to onboard suppliers

Supplier owners and supplier managers can use the supplier onboarding playbook to complete the tasks and activities that are needed to onboard new suppliers.

## Playbooks overview

Playbooks provide step-by-step guidance for onboarding suppliers. A playbook visualizes a workflow in a simple, task-oriented view. The workflow for a playbook is typically created using [Process Automation Designer](https://www.servicenow.com/docs/access?context=process-automation-designer&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

A playbook takes a workflow and breaks it into multiple stages. Each stage in a playbook includes one or more activities or steps for a supplier owner or supplier manager to complete. Stages can also include automated activities, such as sending an email to a supplier contact when a stage or activity is complete. For more information, see [Interact with Playbook](https://www.servicenow.com/docs/access?context=playbook-ui&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

When using a playbook, a supplier owner or supplier manager can:

-   View the playbook stages and activities.
-   View status indicators that display the current state of each activity or step.
-   View check boxes that indicate the stage you are currently at in the workflow.
-   Select an activity and perform the work necessary to complete that activity.
-   Mark an activity as complete and move to the next activity or stage.
-   Complete the stages and activities necessary to complete the case.

## Supplier onboarding playbook

You can use the Supplier onboarding playbook to onboard a new supplier. The Supplier onboarding playbook provides the activities and tasks that a supplier owner or supplier manager can perform during the onboarding process.

You can use the Supplier onboarding playbook with cases that are created using the Onboard a Supplier case type.

The Supplier onboarding playbook appears in the **Playbook** tab on the Case Details page in the Source-to-Pay Workspace.

After you submit a supplier onboarding request, the application creates a new case of type Onboard a Supplier and opens the Case Details page. You can select the **Playbook** tab and start the supplier onboarding process using playbook. For more information on creating a supplier, see [Add a supplier](../../sourcing-procurement-operations/task/create-supplier.md).

**Important:** Supplier Lifecycle Operations creates an approval record if the "Ask For Approval" action is a part of any SLO flow. This approval record can be approved by the user who belongs to the Supplier Administrators group \(sys\_user\_group table\). For more information, see [Add a user to a group](https://www.servicenow.com/docs/access?context=t_AddAUserToAGroup&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

![Playbook tab on the Case Details page.](../image/playbook-tab.png "Playbook tab on the Case Details page")

The Supplier onboarding playbook includes the following stages:

-   Registration: Includes activities to register the supplier.
-   Qualification: Includes activities to verify the eligibility of the supplier.
-   Activation: Includes activities to activate the supplier.
-   Rejection: Includes activities to reject the supplier.

**Parent Topic:**[Create a supplier from the Source-to-Pay Workspace](../task/new-supplier.md)

**Related topics**  


[Add a subsidiary for a supplier from the Source-to-Pay Workspace](../task/add-subsidiary.md)

[Perform risk assessment playbook](perform-risk-playbook.md)

## Registration stage

The following table lists the activities in the Registration stage of the Supplier onboarding playbook.

<table id="table_n5m_klm_sbc"><thead><tr><th>

Activity

</th><th>

Activity Details

</th></tr></thead><tbody><tr><td>

Collecting onboarding details

</td><td>

Processes the supplier details collected in the onboarding request form.This activity completes automatically.

</td></tr><tr><td>

Process onboarding variables

</td><td>

Uses the information provided to start the onboarding activities.This activity completes automatically.

</td></tr><tr><td>

Update the supplier case record

</td><td>

Sets the supplier case record to Work in progress.This activity completes automatically.

</td></tr><tr><td>

Show possible duplicate suppliers

</td><td>

Displays duplicate supplier records to ensure you are not onboarding an existing supplier.If there are no duplicate supplier records, this activity auto-completes.

If duplicate supplier records exist, then select **Open List** to see the duplicate record and resolve the issue.

</td></tr><tr><td>

Show possible duplicate onboarding requests

</td><td>

Displays duplicate supplier onboarding request cases to ensure you are not duplicating an existing case.If there are no duplicate supplier onboarding request cases, this activity auto-completes.

If duplicate supplier cases exist, then select **Open List** to see the duplicate cases and resolve the issue.

</td></tr><tr><td>

Check for supplier intelligence source

</td><td>

Checks if a supplier intelligence platform is installed to import supplier data.

</td></tr><tr><td>

Import supplier details from intelligent/external source

</td><td>

Imports supplier details from the supplier intelligence platform.Available actions:

-   **Import data**
-   **Skip**

</td></tr><tr><td>

Create new company record

</td><td>

Creates a new record for the supplier in the Company \[core\_company\] table.This activity completes automatically.

</td></tr><tr><td>

Create new supplier record

</td><td>

Creates a new supplier record in the Supplier \[sn\_fin\_supplier\] table.This activity completes automatically.

</td></tr><tr><td>

Associate the onboarding case with the newly created supplier.

</td><td>

Associates the onboarding case with the supplier. The **Supplier** field shows the newly created supplier on the **Details** tab of the case.This activity completes automatically.

</td></tr><tr><td>

Sync supplier profile with the third party source

</td><td>

Synchronizes the supplier and company records with data from a third-party supplier intelligence.This activity completes automatically.

</td></tr><tr><td>

Invite supplier contact

</td><td>

Sends an email to the primary contact to register to the Supplier Collaboration Portal.

</td></tr><tr><td>

Verify that the supplier information is correct

</td><td>

Ensure that the supplier information is accurate and up to date.Available actions:

-   **Mark complete**
-   **Skip**
-   **Update**

</td></tr><tr><td>

Waiting for supplier contact invitation to be sent out

</td><td>

Waits for the primary contact to be given access to the Supplier Collaboration Portal.

</td></tr><tr><td>

Set the case status to On Hold.

</td><td>

Sets the case status to On Hold.After this activity is completed, the playbook moves to the Qualification stage.

</td></tr></tbody>
</table>**Related topics**  


[Qualification stage](use-playbooks-onboard-supp.md#)

[Activation stage](use-playbooks-onboard-supp.md#)

[Rejection stage](use-playbooks-onboard-supp.md#)

## Qualification stage

The following table lists the activities in the Qualification stage of the Supplier onboarding playbook.

<table id="table_t2h_mlm_sbc"><thead><tr><th>

Activity

</th><th>

Activity Details

</th></tr></thead><tbody><tr><td>

Check if Risk assessment for supplier plugin is installed

</td><td>

Checks whether the risk assessment for supplier plugin is installed.

</td></tr><tr><td>

Risk assessment decision

</td><td>

Lets you choose whether you need to perform risk assessment for the supplier being onboarded.Available actions:

-   **Continue without assessment**
-   **Perform risk assessment**

</td></tr><tr><td>

Perform risk assessment

</td><td>

The playbook starts the risk assessment process.

</td></tr><tr><td>

Waiting for risk assessment to be completed

</td><td>

The playbook waits for the risk assessment to be completed. A new due diligence case is created. You can see this case on the **Related Cases** tab of the Onboard a supplier case. Select the link for the due diligence case, which opens the Perform risk assessment playbook.One of the following occurs:

-   If you have installed only the Risk Assessments Integration for Supplier Lifecycle Operations \[com.snc.sn\_supplier\_tprm\] plugin, the Perform risk assessment playbook triggers the flow that includes activities to verify the eligibility of the supplier by creating risk assessments. For more information, see [Playbook stages and activities when only Vendor Risk Management is installed](risk-flow-vrm-stages.md).
-   If you have installed both the Risk Assessments Integration for Supplier Lifecycle Operations \[com.snc.sn\_supplier\_tprm\] and GRC: Third-party Risk Due Diligence \[com.sn\_tprm\_onboarding\] plugins, the Perform risk assessment playbook triggers the flow that includes activities to create a due diligence request, complete Inherent Risk Questionnaire \(IRQ\) assessments, and conduct risk assessments for a third-party and an engagement. For more information, see [Playbook stages and activities when Third-party Risk Due Diligence is installed](risk-flow-tprmdd-stages.md).

</td></tr><tr><td>

Update the supplier case record

</td><td>

Updates the state of the case to Work in progress.

</td></tr><tr><td>

Confirm supplier is not restricted

</td><td>

Verify that this supplier is not on any corporate or governmental restricted list. If they are, you must reject this case.Available actions:

-   **Confirm not restricted**
-   **Reject**

If you select **Reject**, the playbook opens the [Rejection stage](use-playbooks-onboard-supp.md#).


</td></tr><tr><td>

Confirm qualification status

</td><td>

Confirm if you would like to continue onboarding or reject the supplier.Available actions:

-   **Continue Onboarding**
-   **Reject**

If you select **Reject**, the playbook opens the [Rejection stage](use-playbooks-onboard-supp.md#).


After this activity is completed, the playbook moves to the Activation stage.

</td></tr></tbody>
</table>**Related topics**  


[Registration stage](use-playbooks-onboard-supp.md#)

[Activation stage](use-playbooks-onboard-supp.md#)

[Rejection stage](use-playbooks-onboard-supp.md#)

## Activation stage

The following table lists the activities in the Activation stage of the Supplier onboarding playbook.

<table id="table_mkw_mlm_sbc"><thead><tr><th>

Activity

</th><th>

Activity Details

</th></tr></thead><tbody><tr><td>

Create a task to collect banking details

</td><td>

Creates and assigns a task to the primary supplier contact to update the supplier banking details.

</td></tr><tr><td>

Create a task to review the supplier profile details

</td><td>

Creates and assigns a task to the primary supplier contact to review the supplier profile details.

</td></tr><tr><td>

Waiting for supplier to complete banking details

</td><td>

This activity is completed after the primary supplier contact completes the Update banking details task from the Supplier Collaboration Portal.

</td></tr><tr><td>

Waiting for supplier to validate their profile details

</td><td>

This activity is completed after the primary supplier contact validates the Update supplier profile task from the Supplier Collaboration Portal.

</td></tr><tr><td>

Confirm supplier activation

</td><td>

Confirm if you would like to continue onboarding or reject the supplier.Available actions:

-   **Continue Onboarding**
-   **Reject**

If you select **Reject**, the playbook opens the [Rejection stage](use-playbooks-onboard-supp.md#).


</td></tr><tr><td>

Activate supplier record

</td><td>

Sets the supplier record to onboarded=true.

</td></tr><tr><td>

Update supplier company status

</td><td>

Sets the status for the company record to **active**.

</td></tr><tr><td>

Send welcome email to supplier

</td><td>

Sends an email to the supplier with a welcome message.

</td></tr><tr><td>

Notify requestor of onboard completion

</td><td>

Sends an email to the requestor, informing them about the supplier onboarding completion status.

</td></tr><tr><td>

Set onboarding case to complete.

</td><td>

Updates the onboarding case to Closed completed.

</td></tr></tbody>
</table>**Related topics**  


[Registration stage](use-playbooks-onboard-supp.md#)

[Qualification stage](use-playbooks-onboard-supp.md#)

[Rejection stage](use-playbooks-onboard-supp.md#)

## Rejection stage

The following table lists the activities in the Rejection stage of the Supplier onboarding playbook.

<table id="table_ebs_nlm_sbc"><thead><tr><th>

Activity

</th><th>

Activity Details

</th></tr></thead><tbody><tr><td>

Provide reason for rejection

</td><td>

Provide a reason for rejecting the supplier onboarding request.In the **Close notes** field, enter the reason for rejection and select **Reject Supplier**.

Available actions:

-   **Reject Supplier**
-   **Skip**

</td></tr><tr><td>

Send rejection email to supplier

</td><td>

Sends an email to the supplier informing them that their onboarding request has been rejected.

</td></tr><tr><td>

Notify requestor of onboard rejection

</td><td>

Sends an email to the requestor, informing them about the supplier onboarding rejection.

</td></tr><tr><td>

Set onboarding case to rejected

</td><td>

Updates the onboarding case to Closed rejected.

</td></tr></tbody>
</table>**Related topics**  


[Registration stage](use-playbooks-onboard-supp.md#)

[Qualification stage](use-playbooks-onboard-supp.md#)

[Activation stage](use-playbooks-onboard-supp.md#)

