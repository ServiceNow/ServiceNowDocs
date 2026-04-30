---
title: Create an Employee Relations case in Agent Workspace for HR Case Management
description: You can use HR Service Delivery Agent Workspace to create ER cases for employees that wish to report misconduct, discrimination, or a disciplinary issue.
locale: en-US
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Use, Employee Relations, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Create an Employee Relations case in Agent Workspace for HR Case Management

You can use HR Service Delivery Agent Workspace to create ER cases for employees that wish to report misconduct, discrimination, or a disciplinary issue.

## Before you begin

Role required: sn\_hr\_er.case\_writer

## Procedure

1.  Navigate to **All** &gt; **HR Case Management** &gt; **Agent Workspace for HR Case Management**.

2.  Select the **Lists** icon \(![Lists icon](../image/agent-ws-hr-list-icon.png)\).

3.  In the ER category, click **New**.

4.  Search for an employee or case number, or select the **Skip verification** link if the subject person is external or wants to remain anonymous.

5.  Fill in the form.

<table id="table_dpm_wgt_lbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

COE

</td><td>

The **Center of Excellence** associated with the HR case you are creating. Currently, Employee Relations Case is the only COE available for ER cases.

 Selecting a COE filters the choices for HR service. See [HR Centers of Excellence data model](../concept/hr-centers-of-excellence-coes.md).

 **Note:** You can also select an HR service first and the associated COE automatically populates.

</td></tr><tr><td>

HR Service

</td><td>

After selecting **Employee Relations Case** from the **COE** field, select one:-   Accommodation Request
-   Report Discrimination
-   Report Misconduct

**Note:** You can use the Skip verification feature when creating a Report Misconduct case. For more information, see [Using HR Service Delivery Employee Relations](../concept/hr-er-using.md).

-   Performance improvement plan\(PIP\)
 Limit what HR services are available to an employee by filtering:

-   COE selected.
-   HR criteria for the **Subject person** based on the HR service configuration.

Limit services filter on the **Case Creation Configuration** form. If the HR service field is empty, ensure that you did not remove the Opened for field.

 **Note:** **Bulk Parent Case** does not appear as a selection because it only appears when creating a parent case for child bulk cases. Refer to [Add or modify bulk HR cases](t_CreateBulkCases.md).

</td></tr><tr><td>

Opened for

</td><td>

The person the ER case was opened for. You can enter letters or numbers to search for possible hits.If the person wants to remain anonymous or is outside of your company, you can leave this field blank.

</td></tr><tr><td>

Subject person

</td><td>

The person the ER case is about.

</td></tr><tr><td>

Work notes

</td><td>

Details about the ER case.**Note:** Interviews are under the **more** tab.

</td></tr></tbody>
</table>6.  Select **Create case**.

    The case returns with a **Case Timeline** that provides a visual of all tasks and key milestones and dates related to the case. The **Case Timeline** helps agents visualize and navigate the key investigation activities on a case and quickly understand the history and what still needs to be done. A **Show Legend** drop-down also appears to show or hide the number of events scheduled or conducted and the associated date.

    Below the **Case Timeline** are a number of tabs that you can provide additional information about the case.

    **Note:** Closed and completed events could still appear on the timeline, but not necessarily in the related tabs.

    The **Related Items menu** shows a series of tabs you can use to add information about the ER case.

    -   **Details**

        Workplace case information entered by the requester for the ER case.

    -   **Involved Parties**

        People associated with the ER case. Involved parties can be the complainant, subject of the allegation, a witness, or other \(undefined\). For more information, see [Create an involved parties record](hr-er-involved-parties.md).

    -   **Allegations**

        Information that further defines an employee relations case. For more information, see [Create an allegation record](hr-er-create-allegation.md).

    -   **Interviews**

        Interview record for an involved party. For more information, see .

    -   **Evidence**

        Evidence to support the ER case. For more information, see [Evidence Management for Employee Relations](../concept/hr-er-evidence-mgmt.md#).

    -   **more**

        Select to view the following:

        -   Corrective Actions: Information about the resolution and any associated corrective actions after an investigation related to the ER case. For more information, see [Create a corrective action](hr-er-corrective-actions.md).
        -   Attached Knowledge: List of knowledge articles attached to the HR service type. For more information, see [HR Knowledge Management](../concept/hr-knowledge-management.md).
        -   Approvers: Lists employees that can approve changed information or the case, state of approval, comments, and associated dates. For more information, see [Resubmit an HR case for approval](t_ApproveAnHRCase.md).

            **Note:** To reject an approval, users should have the HR case writer \[sn\_hr\_core\_case.writer\] role.

        -   Child Cases: Lists child cases for the current case.
        -   ER Cases for Involved Parties: Lists other ER cases for the involved parties of the ER case.
        -   Allegation Outcomes: Shows allegations and results.

