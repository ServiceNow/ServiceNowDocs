---
title: Work on a Health and Safety case
description: Work on a safety case to provide information, ensure that any outstanding tasks are completed, and resolve the employee's questions and compensation claims related to health and safety.
locale: en-US
release: zurich
product: Health and Safety Case Management
classification: health-and-safety-case-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Health and Safety Case Management, Health and Safety, Employee Service Management]
---

# Work on a Health and Safety case

Work on a safety case to provide information, ensure that any outstanding tasks are completed, and resolve the employee's questions and compensation claims related to health and safety.

## Before you begin

Role required: sn\_hs\_cm.case\_manager, sn\_hs\_cm.case\_writer, sn\_hs\_cm.rtw\_writer, or sn\_hs\_cm.claim\_case\_writer

## About this task

When an employee or a worker submits a health and safety question or compensation claim, a safety case is created and assigned to the safety team.

## Procedure

1.  Navigate to **All** &gt; **Health and Safety** &gt; **Health and Safety Workspace**.

2.  Select the cases icon \(![Health and safety cases icon.](../image/icon-hs-cases.png)\).

3.  In the **Lists** tab, under the **Cases**, open the case list.

    -   For your assigned cases, select **Assigned to me**.
    -   For all safety cases, select **All**.
4.  In the list, select the case to work on.

    To work on a case that is not assigned to you yet, assign it to yourself using the **Assigned to** field on the safety case form.

5.  On the form, fill in the fields.

    For information about safety case form fields, see [Health and Safety case form](../reference/hs-case-form.md).

6.  If the case is set as **Return to Work**, assess the employee's capability to work before they return from their injury or illness.

    Only a user with the Return to work case writer \[sn\_hs\_cm.rtw\_writer\] role can edit fields in this section.

    1.  In the **Return to work details** section, fill in the fields.

    2.  In the **Leaves** tab, select **New** to fill in the employee's leave details.

    3.  In the **Injury and Illness** tab, review any injuries and illnesses associated with this case.

        The injury record is auto-populated in the **Injury and Illness** tab if:

        -   this case is added to the **RTW case record** field in the injury and illness report of the associated safety incident. For more information, see [Injury and illness fields](../../ohs-incident-management/reference/hs-injury-illness-form.md).
        -   or, this case was created from the associated injury and illness record. For more information, see [Create a return to work case from an injury or illness](../../ohs-incident-management/task/create-rtw-case-injury-illness.md).
7.  If the case is set as **Compensation claim case**, fill in these sections.

    Only a user with the Claim case writer \[sn\_hs\_cm.claim\_case\_writer\] role can access these sections.

    1.  In the **Employee claim details** section, review the claim and provide details, including a breakdown of the claim amount into different components that add up to the total claim cost.

    2.  In the **Closure details** section, fill in the compensation outcome details, amount paid, and closure date.

8.  In the **Documents** tab, add any documents related to the case.

    -   Select **Add** to link an existing document stored in the **Health and Safety document library** list.
    -   Select **New** to upload a new document.
    For more information, see [Add a new Health and Safety related document](../../ohs-incident-management/task/add-hs-related-document.md).

9.  In the **Actions** tab, select **New** to add any actions for the case.

    For field descriptions, see [Health and Safety action form](../../ohs-incident-management/reference/hs-action-form.md).

10. Provide additional information requested in this case.

    You can use these sections to provide the information and resolve the case:

    -   **Attachments** section to attach any information.
    -   **Compose** section to add information in the form of free text. You can also use this section to add links to related knowledge base articles.
11. Research content related to the case by selecting the Agent assist icon \(![agent assist icon](../../../common/image/Form_AgentAssistIcon.png)\).

    Agent assist searches the knowledge base using the text from the case's **Short description** field and shows relevant articles.

12. Generate a report for the safety case, if needed.

    1.  Select **Generate report**.

        **Note:** The **Generate report** button appears only when the Health and Safety case \[sn\_hs\_cm\_case\] table is enabled for report field mapping. For more information, see [Enable a Health and Safety table for configuring report field mapping](../../ohs-incident-management/task/enable-hs-table-report-field-mapping.md).

    2.  In the **Generate report** dialog box, select a report mapping in the **Select report** field.

        Only the report mapping forms created and published for the Health and Safety case \[sn\_hs\_cm\_case\] table are available to select in the **Select report** field. For more information, see [Create a safety report field mapping for generating reports](../../ohs-incident-management/task/create-safety-report-field-mapping.md).

    3.  Select **Generate**.

13. Select **Close case** to close the safety case after all activities are complete.


## Result

The safety case moves to the Closed Complete state.

