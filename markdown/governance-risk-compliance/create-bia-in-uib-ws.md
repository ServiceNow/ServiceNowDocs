---
title: Create a business impact analysis
description: Create a business impact analysis in BCM UI Builder Workspace to gather information for an impact analysis.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/create-bia-in-uib-ws.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 12
breadcrumb: [Structured workflows for BIAs, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Create a business impact analysis

Create a business impact analysis in BCM UI Builder Workspace to gather information for an impact analysis.

## Before you begin

Role required: sn\_bia.bia\_admin, sn\_bia.bia\_manager, sn\_bcm.program\_manager, sn\_bcm.planner

## About this task

Starting with the Yokohama release, you can configure a business impact analysis \(BIA\) template with a legacy assessment or Smart assessment. The Smart assessment offers multiple question types and uses impact automation to calculate the RTO, RPO, and recovery tier based on your answers. To configure a BIA template with the legacy or Smart assessment, see [Configure BIA templates with legacy assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/configure-bia-template-uib-ws.md) or [Configure BIA templates with Smart Assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/conf-bia-temp-smart-asmt-type.md).

Starting with the Xanadu release, you can use the updated dependencies from the latest BIA record to conduct a dependency assessment on an asset. Using these updated dependencies supports precise execution of the business impact analysis. The business impact analysis includes these updates

-   Access the latest BIAs of the dependent items and their recovery objectives such as Recovery Time Objectives \(RTOs\), Recovery Point Objectives \(RPOs\), and Recovery Tiers.
-   Configure the columns in the dependency assessment of a BIA.
-   Schedule automated updates for the dependencies from the CMDB.
-   Configure the updates to be done after a manual review.

Information from the Related item BIA, Related item Recovery Time Objective \(RTO\), Related item Recovery Point Objective \(RPO\), and Related item Recovery Tier columns is used to ascertain the required recovery timeframe and data backup needs. The updated values are then displayed in the Required Recovery Timeframe and Required Data Backup columns of the BIA record.

The BIA Manager \(sn\_bia.bia\_manager\) includes the Doc writer \(sn\_doc.writer\) role that provides read and write permissions to the document templates.

You can assign ownership of a business impact analysis to an individual owner, to an owner group, or to both. When you create a BIA, you're added as the **BIA owner** by default. To assign the BIA to a group, select a group in the **BIA owner group** field. The list shows only groups that hold the BIA planner or BIA manager role. You must provide either a **BIA owner** or a **BIA owner group** to save the record. When you select an owner group, the **BIA owner** field is limited to members of that group. Clear the **BIA owner** field to assign the BIA to the group only. All members of the owner group have the same edit rights on the BIA as the owner.

\[Omitted image "bia-owner-group-field.png"\] Alt text: Create Impact analysis form with the BIA owner and BIA owner group fields.

## Procedure

1.  Navigate to **Workspaces** &gt; **Business Continuity Workspace** and select **Business Impact Analysis** in the List view and select **New**.

    The **Create Impact analysis** form appears.

    \[Omitted image "create-bia-record-group-fields.png"\] Alt text: Group ownership fields.

2.  On the **Details** tab of the **Create Impact analysis** form, complete the required fields and verify the RTO details for the BIA.

    For more information on the fields, see [Create Impact analysis form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/create-new-impact-analysis-reference-form-bcm-uib-ws.md).

    The **Finalized RTO** field is auto-calculated based on the values in the **Recovery time objective** and **Adjusted RTO** fields available on the same form.

    If the BIAs already have the **Recovery time objective** field, the application uses that Recovery time objective value automatically for the finalized RTO. If the BIA has the **Adjusted RTO** field, the application uses that Adjusted RTO value automatically for the finalized RTO. For information on the field, see the field description in the [Create Impact analysis form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/create-new-impact-analysis-reference-form-bcm-uib-ws.md).

    The example shows that the **Finalized RTO** field is empty because the application didn't run the fix script.

    \[Omitted image "finalized-rto-rpo.png"\] Alt text: RTO.

    The business impact analysis is created in the **Draft** state and it is displayed in the List view. The state and details of the business impact analysis are displayed in these tabs:

    -   **Overview**: View the current state and overall state progression for the business impact analysis.
    -   **Details**: Add the details of the business impact analysis such as its name, template, business unit, department, and so on.
    -   **Assessment**: Fill in responses to the assessment questionnaires for the business impact analysis in the **Recovery time objective assessment**, **Recovery point objective assessment**, and **Dependency assessment** cards.
3.  In the User Administration or Assignment details section of the form, assign BIA ownership.

    1.  To assign group ownership, select the **BIA Owner group** field and select a group from the filtered list.

        Only groups with the sn\_bia.bia\_planner or sn\_bia.bia\_manager role are displayed.

        \[Omitted image "bia-owner-field.png"\] Alt text: BIA Owner field.

    2.  To assign an individual owner, select the **BIA Owner** field and select a user from the list.

        If you selected a group in the previous step, the list shows only members of that group. You can assign

        -   Individual owner only \(leave BIA Owner group empty\)
        -   Group ownership only \(leave BIA Owner empty\)
        -   Both group and individual owner
        At least one ownership field \(group or individual\) must be populated before saving.

    3.  Select **Save**.

    The BIA record ownership is assigned to the selected group, individual, or both. You can also view the group-owned records in the **My group's pending tasks** and **My group's items** tabs in the My Tasks page. For more information, see [My tasks page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/my-tasks-page-uib-ws.md).

4.  Enter the RTO in the **Adjusted RTO** field, enter the reason for adjusted RTO, and save the changes.

    When you update the value in the **Adjusted RTO** field manually, the **Reason for Adjusted RTO** field is displayed. You can add the reason and save the changes.

    \[Omitted image "adjusted-rto-reason.png"\] Alt text: Reason.

    As a result, the **Finalized RTO** is populated with the **Adjusted RTO** value.

    \[Omitted image "finalized-rto.png"\] Alt text: Adjusted RTO.

5.  In the **Details** tab, verify the RPO details for the BIA, enter the RPO in the **Adjusted RPO** field, enter the reason for adjusted RPO, and save the changes.

    The **Finalized RPO** field is auto-calculated based on the values in the **Recovery point objective** and **Adjusted RPO** fields available on the same form.

    If the BIAs already have the **Recovery point objective** field, the application uses that Recovery point objective value automatically for the finalized RPO. If the BIA has the **Adjusted RPO** field, the application uses that Adjusted RTO value automatically for the finalized RPO. For information on the field, see the field description in the [Create Impact analysis form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/create-new-impact-analysis-reference-form-bcm-uib-ws.md).

    When you update the value in the **Adjusted RPO** field manually, the **Reason for Adjusted RPO** field is displayed. You can add the reason and save the changes.

    As a result, the **Finalized RPO** is populated with the **Adjusted RPO** value.

6.  On the **Assessments** tab, view the impact analysis assessments and the dependency assessment.

    Track data specific to the dependency types as shown in the images.

    \[Omitted image "track-data-spe-to-dep-type-1.png"\] Alt text: Track data specific to the dependency types-1.\[Omitted image "track-data-spe-to-dep-type-2.png"\] Alt text: Track data specific to the dependency types-2.

    Add details from the related BIAs as shown in the image.

    \[Omitted image "add-details-from-rel-bias.png"\] Alt text: Add details from related BIAs.

    Consider a scenario where you're conducting an importance assessment for a service. This assessment is carried out by the business service owner or the business process owners. It encompasses all the necessary dependencies that support their daily operations. It includes teams, applications, hardware resources, vendors, and locations, to verify that the process is effectively completed and delivered.

    Starting with the Xanadu release, when conducting a dependency assessment, the dependencies are pulled in and the requirements are visible within the same record. For example, the business requirement for Business Application: Acrobat specifies that the downtime shouldn't exceed 72 hours, which is the established recovery time objective \(RTO\) by the business.

    \[Omitted image "rrt-example.png"\] Alt text: RRT example.

    However, the RTO committed by the IT team, as shown in the Related item RTO, is one month. The Related item columns \(BIA, RTO, RPO, Recovery Tier\) enable the BIA owner to evaluate data and determine necessary recovery timeframes and backup requirements.

7.  Launch the impact analysis assessment and answer the questions.

    The **Assessments** tab in the BIA displayed a single assessment card and the **Open assessment** button earlier. Starting with the Yokohama release, the layout of the cards in the **Assessments** tab has been updated. The BIA displays multiple assessments and dependency assessments in a two-column arrangement.

    \[Omitted image "asmt-tab-bia.png"\] Alt text: Assessments tab.\[Omitted image "asmt-rpo-page.png"\] Alt text: Assessment.

    The example shows the Recovery Time Objective \(RTO\) assessment.

    \[Omitted image "bia-new-asmt-rto-example.png"\] Alt text: RTO.

    The assessment cards are displayed dynamically, allowing you to attach multiple assessments to a BIA. For instance, if you have one card, it is shown alone in a row. If you have seven cards, they are arranged in four rows \(three rows with two cards each and one row with one card\). You can add multiple assessments or just one.

8.  To perform Recovery time objective assessment and Recovery point objective assessment, select the cards for Recovery time objective assessment and Recovery point objective assessment and answer the questions.

9.  Review the answers in the assessment questionnaire, select **Submit**, and select **OK**.

    A message confirms that the update has been successfully processed.

    The assessment card in the **Assessments** tab is updated. Select the Dependency assessment card to open the BIA assessment.

10. Complete the Dependency assessment.

    In the Dependency assessment, the Related item finalized RTO and Related item finalized RPO columns are displayed. The values for these columns are derived from the dependencies related BIA.

    \[Omitted image "related-item-finalized-rto.png"\] Alt text: Related item finalized RTO.

    Consider an example where you have the BIA record that applies to the "Acrobat" application. The example shows that the "Application downtime assessment for Acrobat" BIA record applies to "Acrobat" and it has the Finalized RTO and Finalized RPO values filled in.

    \[Omitted image "acrobat-bia.png"\] Alt text: Acrobat BIA.\[Omitted image "acrobat-bia-fin-rto-example.png"\] Alt text: Values filled in.

    Example shows that "Acrobat" is added to the dependency assessment of the "My Service Importance Assessment" BIA record.

    \[Omitted image "acrobat-example.png"\] Alt text: Acrobat example.\[Omitted image "acrobat-bia-added.png"\] Alt text: BIA for Acrobat.

    When "Acrobat" is added, the Related item finalized RTO and Related item finalized RPO values are populated. These values are associated with the "Acrobat" BIA in the Dependency assessment of the "Application downtime assessment for Acrobat" BIA record.

    \[Omitted image "rel-item-fin-rto-output.png"\] Alt text: Related item finalized RTO output.

    1.  To reassign the assessment to another user, select **More actions** and select **Reassign**.

        A message confirms that the assessment is reassigned to another user. Only the assigned user can answer the assessment.

        You can reassign assessments using the Reassign option in SAE or the contributors functionality.

        **Note:** If you open an assessment that isn't assigned to you, a message confirms that editing the assessment reassigns it to you. Currently assigned user can no longer edit the assessment. Select **Cancel** to cancel the assessment, select **Edit** to edit and reassign the assessment to you, or select **View** to view the assessment in read-only mode.

        When you select **Reassign**, it provides a list of all users in the system. You must select a user with the BCM roles to reassign the BIA.

    2.  To select a contributor from the list to the business impact analysis, launch the **Contributors** panel by selecting the **Contributors** icon in the side-bar and select a contributor.

        If you're the BIA owner or BCM manager, you can select a contributor to the business impact analysis.

        **Note:** Although the BIA contributors with the sn\_bia.bia\_contributor role have read access to the BIA, they can complete the assessments on the **Assessment** tab.

        The BIA contributors can't edit the list of the contributors.

        When you select a contributor to the BIA, that contributor is synchronized to the linked Smart assessment. A contributor who holds an appropriate BIA role can open and complete the assessment. Synchronization of the contributor list requires the Collaborator plugin.

11. Select **Submit**.

    A message confirms that the assessment is successfully submitted.

    \[Omitted image "bia-asmt-comp.png"\] Alt text: Assessment submitted.

    If you want to update the result in the assessment, you can select the card to update the details. The assessment then moves to the **Open** state again. You can retake and resubmit the assessment, thus completing the workflow.

    To revert an archived BIA to the **Draft** state, select the **Edit** button.

    Starting with BCM release 9.0.x, you can revert an archived business impact analysis \(BIA\) to the **Draft** state by selecting the **Edit** button on the form. It helps you to have more flexibility in managing business impacted analyses and related records.

12. To perform more actions on the BIA, select **More actions**.

<table id="choicetable_ypb_yzx_xfc"><thead><tr><th align="left" id="d273385e767">

Step

</th><th align="left" id="d273385e770">

Description

</th></tr></thead><tbody><tr><td id="d273385e776">

**Select __Discuss__.**

</td><td>

Add the subject for the discussion and add participants that have access to the record. Include a brief message for the participants and select **Start discussion**.

</td></tr><tr><td id="d273385e791">

**Select __Generate MS Word__.**

</td><td>

Generate a report of the BIA, BCP, exercise, or crisis record in Microsoft Word format. The Microsoft Word copy of the BIA record is successfully generated that you can download.

</td></tr><tr><td id="d273385e809">

**Select __Generate PDF__.**

</td><td>

Generate a PDF of the BIA with the legacy or Smart Assessment. The PDF of the BIA record is generated and available for download. In the Impact Assessments section of the PDF, details of the Smart assessment are covered. They include questions and answers for RPO and RTO in a tabular format, along with dependencies, contributors, and attachments.

Review and confirm the group ownership fields in the PDF and Microsoft Word reports.

The BIA Group owner and BIA Owner fields are shown in the following sample PDF report.

\[Omitted image "grp-fields-bia-pdf-report.png"\] Alt text: Group fields in the report.View your BIA group's pending tasks and BIA owner's assigned items in the My tasks page.

The BIA group's pending tasks and BIA owner's assigned items are shown in the following sample My tasks page.

\[Omitted image "my-grp-pending-tasks.png"\] Alt text: BIA group's pending tasks and BIA owner's assigned items.

</td></tr><tr><td id="d273385e843">

**Select __Copy__.**

</td><td>

Create a copy of the BIA. BIA details, including its state, assessments, questions, and answers, are copied and displayed on the home page in the BIA section and BIA list. Confirm the name of the new BIA.

The copied BIA inherits the original **BIA owner group** only. You're automatically assigned as the individual **BIA owner** of the copy.

</td></tr><tr><td id="d273385e865">

**Select __360º view__.**

</td><td>

Generate 360º relationships for the BIA. A graphical presentation of the BIA and its relationships is displayed.

</td></tr><tr><td id="d273385e877">

**Select __Delete__.**

</td><td>

Delete the BIA record. A warning message confirms that deleting the record results in an automatic deletion of related records, which may also cause a cascade of additional records to be deleted.

</td></tr><tr><td id="d273385e889">

**Select __Save__.**

</td><td>

Save the BIA record.

</td></tr></tbody>
</table>
-   **[Create Impact analysis form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/create-new-impact-analysis-reference-form-bcm-uib-ws.md)**  
Use the Create Impact analysis form to add details about the business impact analysis, assessments, approvals, and so on in BCM Configurable Workspace.

**Parent Topic:**[Structured workflows for BIAs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/bia-tasks-performed-by-bia-owner.md)

