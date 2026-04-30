---
title: Create a risk assessment project
description: Create a risk assessment project to perform assessments on multiple risks and controls simultaneously using Risk Workspace. You can define the project context, including the assessable entity, Risk assessment methodology \(RAM\), project name, description, and identify and add stakeholders.
locale: en-US
release: zurich
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Risk assessment project, Use Risk Workspace, Risk Management, Governance, Risk, and Compliance]
---

# Create a risk assessment project

Create a risk assessment project to perform assessments on multiple risks and controls simultaneously using Risk Workspace. You can define the project context, including the assessable entity, Risk assessment methodology \(RAM\), project name, description, and identify and add stakeholders.

## Before you begin

Role required: sn\_risk\_advanced.project\_user or sn\_risk\_workspace.operational\_risk\_manager or sn\_risk\_workspace.IT\_risk\_manager, or sn\_risk\_workspace.business\_op\_risk\_manager

## Procedure

1.  Navigate to **All** &gt; **Risk** &gt; **Risk Workspace**.

2.  Select the list ![list icon.](../../grc-compliance-case-mgmt/image/list-icon.png) icon.

3.  From the list, navigate to **Risk assessment projects** and select **New**.

4.  Select **New**.

5.  In the Define stage, do the following.

    1.  In the Context section, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Assessable entity|Single or composite entity that needs to be assessed.|
        |Risk assessment methodology|Risk assessment methodology \(RAM\) that you use to assess risks within the project.|

    2.  Select **Next**.

    3.  In the Details section, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Name of the risk assessment project. The name is automatically generated based on the selected assessable entity, followed by the current month and year, with a separator between them. You can modify the name if necessary.|
        |Description|Description about the risk assessment project. It helps the assessors to understand the project in detail.|

    4.  Select **Next**.

    5.  In the Stakeholders section, fill in the fields.

<table id="table_hmb_b2v_2dc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Owner

</td><td>

Name of the project owner. This field is automatically set to the user who created the project, but you can modify it if needed.

</td></tr><tr><td>

Assessor type

</td><td>

User or group who is responsible for assessing the project. Choices are as follows:-   **Users**: Option to select users responsible for assessing the project.
-   **Group**: Option to select group of users responsible for assessing the project.
-   **Entity owner**: Option to select the assessable entity owner as assessor.
-   **Entity stakeholder**: Option to select assessor from the assessable entity stakeholders list.


</td></tr><tr><td>

Assessors

</td><td>

User who is responsible for assessing the project. This field appears only when **Users** is selected from **Assessor type**.

</td></tr><tr><td>

Assessor group

</td><td>

Group that is responsible for assessing the risk. This field appears only when **Group** is selected from **Assessor type**.

</td></tr><tr><td>

Assessors from entity

</td><td>

Assessors from the assessable entity stakeholders list. This field appears only when **Entity stakeholder** is selected from **Assessor type**.

</td></tr><tr><td>

Watchlist type

</td><td>

Users or group who can view and receive notifications about the project. Choices are as follows:-   **Users**: Option to select users who can view and receive notifications about the project.
-   **Group**: Option to select group of users who can view and receive notifications about the project.
-   **Entity stakeholder**: Option to select watchlist users from the assessable entity stakeholders list.


</td></tr><tr><td>

Watchlist users

</td><td>

Users who can view and receive notifications about the project. This field appears only when **Users** is selected from **Watchlist type**.

</td></tr><tr><td>

Watchlist group

</td><td>

Group who can view and receive notifications about the project. This field appears only when **Group** is selected from **Watchlist type**.

</td></tr><tr><td>

Watchlist users from entity

</td><td>

Watchlist users from the assessable entity stakeholders list. This field appears only when **Entity stakeholder** is selected from **Watchlist type**.

</td></tr></tbody>
</table>        The project moves to the Scope risk stage and you can see a list of risks mapped from the underlying entities.

6.  To add risks in the Scope risk stage, you can do the following:

    1.  To create risks from the risk statement, select **Create from risk statements**.

    2.  To add a risk that is not in the library, select **Create ad-hoc risk**.

    3.  To remove risks from the assessment without deleting them from the underlying entities, select the risks, and select **Remove**.

    4.  To add any risks that have been removed, select **Add risk**.

7.  Select **Next**.

    The project moves to the Assess stage, and a notification goes to the assessor.


**Parent Topic:**[Risk assessment project](../concept/risk-assessment-project.md)

