---
title: Create and manage plan documentation sections
description: Use the documentation section to document the recovery capabilities of the plan.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/maintain-bcp-plan-documentation.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Structured workflows for Business Continuity Planning, Using BCM Classic Workspace, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Create and manage plan documentation sections

Use the documentation section to document the recovery capabilities of the plan.

## Before you begin

Role required: sn\_bcm.admin, sn\_bcm.program\_manager, or sn\_bcm.planner

## About this task

Document all additional information such as the goals, objectives, and scope that are required in the context of your plan as separate sections within the document.

## Procedure

1.  Navigate to **Business Continuity** &gt; **Business Continuity Workspace**.

2.  Click the lists icon \(\[Omitted image "ListsIcon.jpg"\] Alt text: Lists icon.\).

3.  Click **In Draft** state in the Planning list.

4.  Click the link to the plan record in the **Name** column.

5.  Click the **Documentation** related list of the plan.

    You can view each section of the documentation in a separate text box. The documentation sections that are part of the plan template, which you used to create the plan, default to this plan. You can create new sections to the documentation and edit existing sections as well.

6.  To edit a documentation section, click the edit icon \(\[Omitted image "EditIcon.png"\] Alt text: Edit icon.\).

    Use this icon to edit the title as well as the text in the description of the documentation section.

7.  To edit the text in a section, click the **Edit** button in the text box.

8.  To undo all your updates and revert to the original text of the documentation section, click **Reset to template** and click **Reset** to confirm your action.

    **Note:** **Reset to template** button is enabled only when the document section is in Pending state and not in Complete state.

    When you reset, both the title and description along with the text in the documentation section are reset to the title, description, and documentation content in the plan template.

9.  To delete a documentation section, click the delete icon \(\[Omitted image "DeleteIcon.png"\] Alt text: Delete icon.\).

    This action deletes the documentation section.

10. To create a section in the documentation tab, click **New section**.

    1.  In the New section pop-up, enter a title and a description for the section.

    2.  Click **Create**.

    3.  Click the **Edit** button to enter the contents in the text box for the section.

11. To save the updates and continue to edit the content, click **Save**.

12. To save and exit the edit mode, click **Complete**.

    After you click **Complete**, both the \[Omitted image "EditIcon.png"\] Alt text: Edit icon. and \[Omitted image "DeleteIcon.png"\] Alt text: Delete icon. icons are disabled. To enable the icons, click the **Edit** button in the documentation section text box.

13. To view the subsequent section and scroll through all the sections, collapse the section after you complete editing.

    -   **Change section order at the plan level**

        You can change the order in which the sections appear in the **Documentation** related list to help the user review the sections in a logical sequence. However, you must set the order preference for the sections by entering an integer value in the **Order** field of the Plan Documentation form for each documentation section in the plan. This customization overrides the order preference set at the plan template level.

    -   **Change section order at the plan template level**

        You can define the order of document sections in the Plan template as well. This order is applied to all the plans that use the template. However, only a BCM administrator can change the order of the sections in the Plan Template form, when the template is created.

        1.  To rearrange the section order, navigate to **Business Continuity** &gt; **Plan Configuration** &gt; **Plan Templates**
        2.  Click the plan template in the **Name** link.
        3.  Click unlock document sections icon \(\[Omitted image "UnlockDocumentSectionicon.png"\] Alt text: Unlock document sections icon\)
        4.  Click the add/remove multiple icon \(\[Omitted image "AddRemoveMultipleIcon.png"\] Alt text: Add or remove multiple icon\) and move the items in a preferred order in the **Document Sections** field.

            \[Omitted image "DocumentSectionConfigure.png"\] Alt text: Rearrange the order of document sections

        5.  Click **Update**.
    As a program manager, planner, viewer, or BCM administrator, you can only view the rearranged order of the sections in the workspace when your plan uses that template.

    \[Omitted image "DocumentSectionOrder.png"\] Alt text: Order of documentation sections


