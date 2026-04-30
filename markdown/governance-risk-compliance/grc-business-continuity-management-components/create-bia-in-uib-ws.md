---
title: Create a business impact analysis
description: Create a business impact analysis in BCM UI Builder Workspace to get the necessary information for a plan.
locale: en-US
release: zurich
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 11
breadcrumb: [Structured workflows for BIAs, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Create a business impact analysis

Create a business impact analysis in BCM UI Builder Workspace to get the necessary information for a plan.

## Before you begin

Role required: sn\_bia.bia\_admin, sn\_bia.bia\_manager, sn\_bcm.program\_manager, sn\_bcm.planner

## About this task

**Note:**

The application is configured with an out-of-the-box \(OOB\) limit of 1000 Business Impact Analyses \(BIA\) records, as defined by the **sn\_irm\_shared\_cmn.config.get\_gliderecord\_limit** system property. This means that the system processes up to 1000 BIA records only, as it cannot exceed this threshold.

Beginning with the Yokohama release, you can configure a business impact analysis \(BIA\) template with a legacy assessment or Smart assessment. The Smart assessment offers multiple question types and uses impact automation to calculate the RTO, RPO, and recovery tier based on your answers. To configure a BIA template with the legacy or Smart assessment, see [Configure BIA templates with legacy assessment](configure-bia-template-uib-ws.md) or [Configure BIA templates with Smart Assessment](conf-bia-temp-smart-asmt-type.md).

Beginning with the Xanadu release, you can use the updated dependencies from the latest BIA record to conduct a dependency assessment on an asset. Using these updated dependencies enables for a precise execution of the business impact analysis. The business impact analysis is enhanced through the implementation of these updates:

-   Access the latest BIAs of the dependent items and their recovery objectives such as Recovery Time Objectives \(RTOs\), Recovery Point Objectives \(RPOs\), and Recovery Tiers.
-   Configure the columns in the dependency assessment of a BIA.
-   Schedule automated updates for the dependencies from the CMDB.
-   Configure the updates to be done after a manual review.

Moreover, information from the Related item BIA, Related item Recovery Time Objective \(RTO\), Related item Recovery Point Objective \(RPO\), and Related item Recovery Tier columns is used to ascertain the required recovery timeframe and data backup needs. The updated values are then displayed in the Required Recovery Timeframe and Required Data Backup columns of the BIA record.

The BIA Manager \(sn\_bia.bia\_manager\) now includes the Doc writer \(sn\_doc.writer\) role that provides read and write permissions to the document templates.

## Procedure

1.  Navigate to **Workspaces** &gt; **Business Continuity Workspace**.

2.  In the List view, navigate to **Business Impact Analysis** and select **New**.

    The **Create New Impact analysis** form is displayed as shown in the example.

    ![Create New Impact analysis form.](../image/new-bia-form.png)

3.  On the **Details** tab of the **Create New Impact analysis** form, fill in the required fields.

    For more information on the fields, see [Create New Impact analysis form](../reference/create-new-impact-analysis-reference-form-bcm-uib-ws.md).

    The business impact analysis is created in the **Draft** state and it’s displayed in the List view. The state and details of the business impact analysis are displayed in these tabs:

    -   **Overview**: You can view the current state and overall state progression for the business impact analysis.
    -   **Details**: You can add the details of the business impact analysis such as its name, template, business unit, department, and so on.
    -   **Assessment**: You can fill in responses to the assessment questionnaires for the business impact analysis in the **Recovery time objective assessment**, **Recovery point objective assessment**, and **Dependency assessment** cards.
4.  In the **Details** tab, review the RTO details for the BIA.

    The **Finalized RTO** field is auto-calculated according to the values in the **Recovery time objective** and **Adjusted RTO** fields available on the same form.

    If the BIAs already have the **Recovery time objective** field, the application uses that Recovery time objective value automatically for the finalized RTO. If the BIA has the **Adjusted RTO** field, the application uses that Adjusted RTO value automatically for the finalized RTO. For information on the field, see the field description in the [Create New Impact analysis form](../reference/create-new-impact-analysis-reference-form-bcm-uib-ws.md).

    The example shows that the **Finalized RTO** field is empty because the application didn't run the fix script.

    ![RTO.](../image/finalized-rto-rpo.png)

5.  Add the RTO manually in the **Adjusted RTO** field as an optional step, add the reason for adjusted RTO, and save the changes.

    When you update the value in the **Adjusted RTO** field manually, the **Reason for Adjusted RTO** field is displayed. You can add the reason and save the changes.

    ![Reason.](../image/adjusted-rto-reason.png)

    As a result, the **Finalized RTO** is populated with the **Adjusted RTO** value.

    ![Adjusted RTO.](../image/finalized-rto.png)

6.  In the **Details** tab, review the RPO details for the BIA.

    The **Finalized RPO** field is auto-calculated according to the values in the **Recovery point objective** and **Adjusted RPO** fields available on the same form.

    If the BIAs already have the **Recovery point objective** field, the application uses that Recovery point objective value automatically for the finalized RPO. If the BIA has the **Adjusted RPO** field, the application uses that Adjusted RTO value automatically for the finalized RPO. For information on the field, see the field description in the [Create New Impact analysis form](../reference/create-new-impact-analysis-reference-form-bcm-uib-ws.md).

7.  Add the RPO manually in the **Adjusted RPO** field as an optional step, add the reason for adjusted RPO, and save the changes.

    When you update the value in the **Adjusted RPO** field manually, the **Reason for Adjusted RPO** field is displayed. You can add the reason and save the changes.

    As a result, the **Finalized RPO** is populated with the **Adjusted RPO** value.

8.  On the **Assessments** tab, view the impact analysis assessments and the dependency assessment.

    You can track data specific to the dependency types as shown in the examples.

    ![Track data specific to the dependency types-1.](../image/track-data-spe-to-dep-type-1.png)![Track data specific to the dependency types-2.](../image/track-data-spe-to-dep-type-2.png)

    You can add details from the related BIAs as shown in the example.

    ![Add details from related BIAs.](../image/add-details-from-rel-bias.png)

    Consider a scenario where you’re conducting an importance assessment for a service. This assessment is carried out by the business service owner or the business process owners. It encompasses all the necessary dependencies that support their daily operations, including teams, applications, hardware resources, vendors, and locations, to verify that the process is effectively completed and delivered.

    Beginning with the Xanadu release, when conducting a dependency assessment, the dependencies are pulled in and the requirements are visible within the same record. For example, the business requirement for Business Application: Acrobat specifies that the downtime shouldn’t exceed 72 hours, which is the established recovery time objective \(RTO\) by the business.

    ![RRT example.](../image/rrt-example.png)

    However, the RTO committed by the IT team, as shown in the Related item RTO, is one month. Additionally, viewing details from the Related item Business Impact Analysis \(BIA\), Related item Recovery Time Objective \(RTO\), Related item Recovery Point Objective \(RPO\), and Related item Recovery Tier columns on the same screen enable the BIA owner to evaluate the data and determine the necessary recovery timeframe and data backup requirements.

9.  Launch the impact analysis assessments as an owner of the assessment, select the card for Recovery time objective assessment, Recovery point objective assessment, or Dependency assessment, and respond to the questions.

    Previously, the **Assessments** tab in the BIA displayed a single assessment card and the **Open assessment** button. Beginning with the Yokohama release, the layout of the cards in the **Assessments** tab of the BIA has been updated to display multiple assessments and dependency assessments a two-column arrangement.

    ![Assessments tab.](../image/asmt-tab-bia.png)![Assessment.](../image/asmt-rpo-page.png)

    The example shows the Recovery Time Objective \(RTO\) assessment.

    ![RTO.](../image/bia-new-asmt-rto-example.png)

    The assessment cards are now displayed dynamically, enabling you to attach multiple assessments to a BIA. For instance, if you have one card, it is shown alone in a row. If you have seven cards, they are arranged in four rows \(three rows with two cards each and one row with one card\). You can add multiple assessments or just one.

10. To perform Recovery time objective assessment, select the card for Recovery time objective assessment card and respond to the questions.

11. To perform Recovery point objective assessment, select the card for the Recovery point objective assessment card and respond to the questions.

12. Review the answers in the assessment questionnaire and select **Submit**.

    A message is displayed that the update has been successfully processed.

13. Select **OK**.

    The assessment card in the **Assessments** tab is updated. Selecting the Dependency assessment card opens the BIA assessment.

14. Complete the Dependency assessment.

    In the Dependency assessment, the Related item finalized RTO and Related item finalized RPO columns are now displayed. The values for these columns are derived from the dependencies related BIA.

    ![Related item finalized RTO.](../image/related-item-finalized-rto.png)

    Consider an example where you have the BIA record that applies to the "Acrobat" application. The example shows that the "Application downtime assessment for Acrobat" BIA record applies to "Acrobat" and it has the Finalized RTO and Finalized RPO values filled in.

    ![Acrobat BIA.](../image/acrobat-bia.png)![Values filled in.](../image/acrobat-bia-fin-rto-example.png)

    Example shows that "Acrobat" is added to the dependency assessment of the "My Service Importance Assessment" BIA record.

    ![Acrobat example.](../image/acrobat-example.png)![BIA for Acrobat.](../image/acrobat-bia-added.png)

    When "Acrobat" is added, the Related item finalized RTO and Related item finalized RPO values associated with the "Acrobat" BIA are populated in the Dependency assessment of the "Application downtime assessment for Acrobat" BIA record.

    ![Related item finalized RTO output.](../image/rel-item-fin-rto-output.png)

15. To reassign the assessment to another user, select **More actions** and select **Reassign**.

    A message is displayed that the assessment is reassigned to another user. Only the assigned user can respond to the assessment.

    **Note:** If you open an assessment that isn’t assigned to you, a message is displayed that editing the assessment reassigns it to you. Currently assigned user can no longer edit the assessment. Select **Cancel** to cancel the assessment, select **Edit** to edit and reassign the assessment to you, or select **View** to view the assessment in read-only mode.

    When you choose **Reassign**, it provides a list of all users in the system. You must select a user with the BCM roles to reassign the BIA.

16. To add a contributor from the list to the business impact analysis, launch the **Contributors** panel by selecting the **Contributors** icon in the side-bar and add a contributor.

    If you’re the BIA owner or BCM manager, you can add a contributor to the business impact analysis.

    **Note:** Even though the BIA contributors with the sn\_bia.bia\_contributor role have read access to the BIA, they can complete the assessments on the **Assessment** tab.

    The BIA contributors can’t edit the list of the contributors.

17. Select **Submit**.

    A message is displayed that the assessment is successfully submitted.

    ![Assessment submitted.](../image/bia-asmt-comp.png)

    If you want to update the result in the assessment, you can select the card to update the details. The assessment then moves to the **Open** state again. You can retake and resubmit the assessment, thus completing the workflow.

18. To revert an archived BIA to the **Draft** state, select the **Edit** button.

    Starting with BCM release 9.0.x, you can revert an archived business impact analysis \(BIA\) to the **Draft** state by selecting the **Edit** button on the form. It helps you to have more flexibility in managing business impacted analyses and related records.

19. To perform more actions on the BIA, select **More actions**.

    |Step|Description|
    |----|-----------|
    |**Select __Discuss__.**|Add the subject for the discussion and add participants that have access to the record. Include a brief message for the participants and select **Start discussion**.|
    |**Select __Generate MS Word__.**|Generate a report of the BIA, BCP, exercise, or crisis record in Microsoft Word format. The Microsoft Word copy of the BIA record is successfully generated that you can download.|
    |**Select __Generate PDF__.**|Generate a PDF of the BIA with the legacy or Smart Assessment. The PDF of the BIA record is successfully generated that you can download. In the Impact Assessments section of the PDF, details of the Smart assessment are covered, including questions and answers for RPO and RTO in a tabular format, along with dependencies, contributors, and attachments.|
    |**Select __Copy__.**|Create a copy of the BIA. BIA details, including its state, assessments, questions, and answers, are copied into the instance and displayed on the home page in the BIA section and BIA list. Confirm the name of the new BIA.|
    |**Select __360º view__.**|Generate 360º relationships for the BIA. A graphical presentation of the BIA and its relationships is displayed.|
    |**Select __Delete__.**|Delete the BIA record. A warning message is displayed that deleting the record results in an automatic deletion of related records, which may also cause a cascade of additional records to be deleted.|

20. To save the BIA record, select **Save**.


-   **[Create New Impact analysis form](../reference/create-new-impact-analysis-reference-form-bcm-uib-ws.md)**  
Use the Create New Impact analysis form to add details about the business impact analysis, assessments, approvals, and so on in BCM Configurable Workspace.

**Parent Topic:**[Structured workflows for BIAs](../concept/bia-tasks-performed-by-bia-owner.md)

