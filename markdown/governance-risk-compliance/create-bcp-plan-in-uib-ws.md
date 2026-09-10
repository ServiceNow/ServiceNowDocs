---
title: Create a business continuity plan
description: Create a business continuity plan in ServiceNow Business Continuity Management.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/create-bcp-plan-in-uib-ws.html
release: australia
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 8
breadcrumb: [Structured workflows for BCPs, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Create a business continuity plan

Create a business continuity plan in ServiceNow Business Continuity Management.

## Before you begin

Role required: sn\_bcm.program\_manager, sn\_bcm.planner, for plan owner group filter: sn\_bcp.plan\_contributor, sn\_bcp.plan\_manager

**Important:** The BCP Plan Manager \(`sn_bcp.plan_manager`\) now includes the Doc writer \(`sn_doc.writer`\) role that provides read and write permissions to the document templates. \(Added June 25, 2026\)

## About this task

You can assign ownership of a business continuity plan to an individual owner, to an owner group, or to both. When you create a plan, you're added as the Plan owner by default.

**Important:** You must provide either a **Plan owner** or **Plan owner group** to save the record.

When you select an owner group, the **Plan owner** field is limited to members of that group. To assign the plan to a group only, clear the **Plan owner** field. All members of the owner group have the same edit rights on the plan as the owner.

## Procedure

1.  Navigate to **Workspaces** &gt; **Business Continuity Workspace** &gt; **Planning** in the list view and select **New**.

    The Create Plan form is displayed.

2.  Fill in the required fields in the **Details** tab of the Create Plan form.

    |Field|Description|
    |-----|-----------|
    |**Name**|The name of the business continuity plan|
    |**Template**|The BCP template to use as a basis for the plan|
    |**Type**|The classification of the plan \(e.g., IT, Departmental, Enterprise\)|
    |**Business Unit**|The business unit responsible for the plan|
    |**Department**|The department responsible for the plan|
    |**Expires**|The expiration date for the plan review|

3.  Assign plan ownership by selecting the appropriate ownership model in the **User Administration** or **Assignment details** section.

<table id="choicetable_vgt_1wx_gkc"><thead><tr><th align="left" id="d123477e206">

 

</th><th align="left" id="d123477e208">

 

</th></tr></thead><tbody><tr><td id="d123477e213">

**Group ownership only**

</td><td>

Select the **Plan owner group** field, select a group from the list \(filtered to show only groups with the Plan Owner or equivalent BCM Manager role\), and leave the **Plan owner** field empty. The plan is owned by the group as a whole, with any member able to take action on the record.

</td></tr><tr><td id="d123477e228">

**Individual ownership only**

</td><td>

Select the **Plan owner** field, select a user, and save the record. This is the legacy ownership model and remains fully supported.

 Group and individual ownership: Select the **Plan owner group** field and choose a group. Then select the **Plan owner** field and select a user from the filtered list \(showing only members of the selected group\). The record is owned by the group with a specific individual designated as the point of contact.

</td></tr><tr><td id="d123477e252">

**Outside group scenario**

</td><td>

If you need to assign an individual owner who is not a member of the selected group, select the individual first in the **Plan owner** field, then select the group in the **Plan owner group** field, and save. This accommodates cases where an individual outside the group is responsible for the record.

</td></tr></tbody>
</table>    **Note:** If the individual owner leaves the group, the group ownership remains intact, and another member can assume the role of individual owner by updating the **Plan owner** field.

4.  Add an asset to the scope of the plan in the **Scope** tab and view the primary elements defined in the plan template.

    When creating a business continuity plan, you can enter details based on the primary asset in the plan record. It includes Recovery Time Objective \(RTO\), Recovery Point Objective \(RPO\), Recovery Tier, and BIA link. Updating the dependencies refreshes the asset details with information from the latest unarchived BIA record.

    You can mark an asset as a primary scope or assign it as a related asset. You can link a related asset to a primary scope within the plan. This simplifies the classification of asset types and enables you to view the relationships directly on the plan record page. You can see which assets are impacted when the primary scope is operationally down.

    The **Asset dependencies** tab displays detailed information about the assets. It replaces the Primary scope and Related asset toggles previously found in the Scope tab. The **Type** column has been renamed to **Types** to allow an asset to be categorized as both a primary scope and a related asset. The **BIA** column has been updated from a document ID type to a reference type. You can now select and access the BIA record and dot-walk to the plan record.

5.  Update the dependencies by selecting the **Update dependencies** button.

    The system pulls both related assets and their relationships. A message indicates that the dependencies are being updated, and you must refresh the page to view the updated dependencies. You can view dependency updates in the snapshot record.

    When you add a dependency in the Scope tab, the system retrieves the most recent Business Impact Analysis \(BIA\). The system uses the BIA's "Finalized RTO" and "Finalized RPO" values for that specific dependency. Values for "Recovery Tier" and "BIA" are also retrieved and displayed in the plan record.

    If you update the BIA's RTO and RPO values after fetching a dependency, select **Update dependencies** to fetch the latest values.

6.  Review the **Finalized RTO** and **Finalized RPO** values columns in the **Scope** tab.

    The Finalized RTO and Finalized RPO fields are populated from the most recent Business Impact Analysis record when you add a dependency.

7.  Add contributors to the business continuity plan by launching the **Contributors** panel from the side-bar.

    BCP contributors with the `sn_bcp.plan_contributor` role have read, write, and delete access to the business continuity plan. If you have the BCP manager, BCM lead, or plan contributor role, you can add or remove contributors. BCP contributors can edit the list of contributors and edit the BCP.

8.  In the **Documentation** tab, record the recovery capabilities of the plan in the documentation sections.

    This tab contains details of the plan in the Sections panel and the Create new section tab. It includes informational fields such as Title, Description, Order, and Contents.

9.  Define recovery teams, loss scenarios, and recovery tasks for the plan in the respective tabs:

    -   **Recovery teams** – Assign recovery teams with their Name, Description, Groups, and Users.

        **Note:** Prior to BCM core 12.x.x, local recovery teams could be added to the plans. Starting with BCM core 12.x.x, you can add global recovery teams to the plans.

    -   **Loss scenarios** – Define applicable loss scenarios with Name and Description
    -   **Recovery tasks** – Create recovery tasks with Planned order, Short description, Owner, Dependencies, Planned duration, Phase, and Asset recovery level. Recovery tasks are organized based on their dependencies; the system determines the sequence based on assigned dependencies, allowing independent tasks to be handled simultaneously.
    **Important:** A cyclic dependency occurs when two or more recovery tasks rely on each other, either directly or indirectly. To prevent cyclic dependencies, verify that the same plan is not triggered multiple times. If plans are activated beyond 10 levels or hierarchical links involve more than 10 levels of plans, an error message is displayed.

10. Complete the remaining required fields on the Plan record form and select **Save**.

    The plan is saved in the **Draft** state and displayed in the List view of the Planning records.

11. Review and confirm the group ownership fields in the PDF and Microsoft Word reports.

    You can generate reports by selecting **More actions** &gt; **Generate PDF** or **More actions** &gt; **Generate MS Word**.

    Starting with BCM Core version 12.x.x and later, issues and group ownership details related to plans appear in separate sections in the PDF and Microsoft Word reports.

12. View your Plan group's pending tasks and Plan owner's assigned items in the **My tasks** page.


## Result

The business continuity plan is created in the Draft state with assigned ownership \(individual, group, or both\). The state and details of the business continuity plan are accessible through the following tabs:

|Tab|Description|
|---|-----------|
|**Overview**|Current state and overall state progression of the BCP|
|**Details**|Plan details including Name, Template, Type, Plan owner, Plan owner group, BCM lead, Business unit, Department, Expires, Description, comments, and Activity panel|
|**Scope**|Asset types list with Item, Types, Recovery time objective, Recovery point objective, Recovery tier, BIA, Status in source, and Synchronized on columns for detailed information. Asset dependencies tab displays hierarchical relationships between parent and child assets.|
|**Documentation**|Recovery capabilities of the plan recorded in documentation sections|
|**Associated plans**|Associated plan types including Upstream plans, Downstream plans, and Related plans|
|**Recovery teams**|Recovery teams assigned for the business continuity plan|
|**Loss scenarios**|Loss scenarios applicable to the business continuity plan|
|**Recovery tasks**|Details of recovery tasks including Planned order, Short description, Owner, Dependencies, Planned duration, Phase, and Asset recovery level|

## What to do next

After creating the business continuity plan, you can perform additional actions by selecting **More actions**:

-   **Discuss** – Add a subject and participants to discuss the plan
-   **Generate MS Word** – Generate a downloadable Word document report
-   **Generate PDF** – Generate a downloadable PDF report \(with Smart assessment details and dependencies\)
-   **Copy** – Create a copy of the BCP with all details, assessments, and questions.

    The copied plan inherits both the original **Plan owner** and **Plan owner group**.

-   **360º view** – Generate 360° relationships for a graphical presentation of the BCP and its relationships
-   **Delete** – Delete the BCP record \(related records may also be deleted\)

To revert an archived business continuity plan to the Draft state, select the **Edit** button on the form. \(Available in release 9.0.x and later\)

-   **[Create Plan form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-new-plan-bcp-uib-ws-reference-form.md)**  
Use the Create Plan form in BCM UIB Workspace to add the details about the business continuity plan \(BCP\).

**Parent Topic:**[Structured workflows for BCPs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/bcp-tasks-performed-by-bcp-owner.md)

**Related topics**  


[Group ownership in BIA, plan, and event records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/group-ownership-bias.md)

[Add or create an issue from a plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/add-or-create-issue-from-plan-uib-ws.md)

