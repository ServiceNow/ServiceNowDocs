---
title: Assess impact categories and dependencies
description: Assess the impact categories and dependencies in BCM UIB Workspace to get the necessary information for a plan. Use the business impact analysis to identify the recovery time objective for an item and prioritize the assets that have the least and most critical dependencies. Use the information to establish their recovery strategies during the planning phase.
locale: en-US
release: australia
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 10
breadcrumb: [Structured workflows for BIAs, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Assess impact categories and dependencies

Assess the impact categories and dependencies in BCM UIB Workspace to get the necessary information for a plan. Use the business impact analysis to identify the recovery time objective for an item and prioritize the assets that have the least and most critical dependencies. Use the information to establish their recovery strategies during the planning phase.

## Before you begin

Role required: sn\_bia.bia\_admin, sn\_bcm.program\_manager, sn\_bcm.planner, sn\_bcm.contributor or sn\_bia.bia\_contributor \(can respond to BIAs in which they are tagged as a contributor\)

## About this task

Beginning with the Xanadu release, these new columns are added to the BIA dependency tables. The values of these columns can be refreshed by selecting the **Update dependencies** button in the Dependency assessment.

-   Related item BIA - The latest unarchived impact analysis done on the dependency item
-   Related item RTO - The Recovery time objective of the above impact analysis. It will take the value of adjusted RTO instead of RTO if there is any.
-   Related item RPO - The Recovery point objective of the above impact analysis. It will take the value of adjusted RPO instead of RPO if there is any.
-   Related item recovery tier - The recovery tier of the above impact analysis.

## Procedure

1.  Navigate to **Workspaces** &gt; **Business Continuity Workspace**.

2.  To update an existing business impact analysis, select the link to the business impact analysis record in the **Name** column and navigate to the **Assessments** tab.

3.  To assess different types of business impact categories on the business process, select the **Recovery time objective assessment** tab.

    A sample questionnaire for the Recovery time objective assessment \(RTO assessment\) is shown in the example.![RTO assessment questionnaire.](../image/rto-assessment.png)You must configure all impact categories in the Recovery time objective assessment. A business process draws a set of impact categories, by default, from the template that you have used for the business impact analysis. For more information, see: [Review an impact category and assess its downtime](review-impact-category-bia.md).

4.  Respond to the questions in the Recovery time objective assessment questionnaire and select **Next**.

    For information on recovery time objective and calculation of recovery time objective, see [RTO, RPO, and recovery tiers](../concept/rto-rpo-recovery-tiers.md) and [Calculating RTO and RPO](../concept/rto-rpo-calculation.md).

5.  To answer questions related to the data component of the asset, select the **Recovery point objective assessment** tab.

    A sample assessment questionnaire for the Recovery point objective assessment \(RPO assessment\) is shown in the example. ![RPO assessment questionnaire.](../image/rpo-assessment.png)You must configure all impact categories in the Recovery point objective assessment. For more information, see [Assess RPO impact of technology assets on the business](RPO-asset-impact-assessment.md). For information on recovery point objective and calculation of recovery point objective, see [RTO, RPO, and recovery tiers](../concept/rto-rpo-recovery-tiers.md) and [Calculating RTO and RPO](../concept/rto-rpo-calculation.md).

6.  Respond to the questions in the Recovery point objective assessment and select **Next**.

    You can respond to the questions and complete the Recovery point objective assessment.

7.  To assess the dependencies and identify the items within each dependency that your business process depends on, select the **Dependency Assessment** tab.

    You can select the dependency in the Dependency panel to view the group and items that belong to that group. For example, if the group is **Locations**, you can select one or more locations and assess the dependencies associated with them. A sample Dependency assessment is shown in the example. ![Dependency assessment.](../image/dependency-assessment.png)

8.  To add an item to a dependency group, select one of the options.

<table id="choicetable_fjs_hqz_dyb"><thead><tr><th align="left" id="d54496e259">

Step

</th><th align="left" id="d54496e262">

Description

</th></tr></thead><tbody><tr><td id="d54496e268">

**__Add__**

</td><td>

Add an item from all the records. The relationship source is BCM. All items from the respective table, irrespective of its relationship in the CMDB are displayed. When you select **Add**, the filter for selecting the dependencies is displayed as shown in the example:![Dependencies selection.](../image/add-dependencies-filter-assessment.png)

 To update the selected dependency item, you can add details and select **Update**.

-   **Depends on**
-   **Required Recovery Timeframe**
-   **Required Data Backup**
-   **Description of Use**
-   **Additional details - Comment**
 A sample assessment is shown in the example.![Update the dependencies.](../image/update-dependencies.png)

</td></tr><tr><td id="d54496e331">

**__Add first level CMDB dependencies__**

</td><td>

Add dependencies for which the relationships are identified in CMDB.

**Note:** Both the **Add** and **Add first level CMDB dependencies** UI actions mark the dependency source as Manual because inserting the dependency is a manual action. The CMDB source is used only when dependencies are automatically inserted by the application through the **Update dependencies** action. The **Add first level CMDB dependencies** UI action streamlines the manual addition of dependencies by pre-filtering the list to show only CMDB relationships, rather than displaying all CI items within an element definition.

 A sample assessment is shown in the example.![Add first level CMDB dependencies.](../image/first-level-of-dependencies.png)

</td></tr><tr><td id="d54496e376">

**__Update dependencies__**

</td><td>

Import all CMDB relationships manually in the respective categories that are defined in the instance.

</td></tr><tr><td id="d54496e389">

**Edit __Required Recovery Timeframe__ \(RTO\) for one dependency**

</td><td>

If you have one dependency in the **Pending** state, you can update its RTO by updating the inline value in the **Required Recovery Timeframe** field as shown in the example.![Updating RTO for one dependency at a time.](../image/req-recovery-timeframe-inline.png)

</td></tr><tr><td id="d54496e416">

**Edit __Required Recovery Timeframe__ for multiple dependencies**

</td><td>

Similarly, you can update the RTO for multiple dependencies as shown in the step-by-step examples:

 1.  Select multiple dependencies.![Multiple dependencies.](../image/edit-all-dependencies-at-once.png)
2.  Select **Edit**. The Edit items Dependency panel is displayed.![Edit items dependencies window.](../image/select-multiple-dependencies-and-edit-rto.png)
3.  Update the RTO for multiple dependencies in the **Required recovery Timeframe** field.![Update the RTO for multiple dependencies.](../image/update-rto-for-multiple-dependencies.png)

RTO is updated for multiple dependencies and the dependency assessment is marked as Complete.

![RTO is updated for multiple dependencies.](../image/deleting-one-rto-value.png)

If you edit the RTO for one dependency, the dependency assessment moves to the **Pending** state.

![Delete one RTO.](../image/deleting-one-rto-value.png)![Dependency-assessment-in-pending-state.](../image/one-rto-empty-dep-assessment-pending.png)

 When you have updated the RTO value for all entries in the **Required Recovery Timeframe** field, then that particular category of dependency is marked as Complete by the application.

**Note:**

If the administrator has set the **Required Recovery Timeframe** field in the dependency assessment as mandatory, the BIA user can update the required recovery timeframe for the dependency assessment. If the administrator has set the **Required Recovery Timeframe** field in the dependency assessment as optional, the BIA user can complete the dependency assessment without updating the **Required Recovery Timeframe** field.

 Data from the Required Recovery Timeframe and Required Data Backup columns is now pulled into the BCP record.

</td></tr><tr><td id="d54496e510">

**Select __Complete__**

</td><td>

This is the final step. You must complete all the pending assessments before selecting **Complete**. Selecting **Complete** marks all the assessments in the business impact analysis as Complete.

 **Note:** After selecting **Complete**, if you see the message that the dependency groups are in the **Not started** state, you must complete the procedures explained in this table for single and multiple dependencies. Selecting **Confirm** in the message window marks all dependency groups as Complete without actually completing them. ![Confirmation of dependencies.](../image/dependencies-selection-confirmation.png)

</td></tr></tbody>
</table>    You can prioritize your business continuity and recovery plans based on the criticality of the assets that your business process uses.

    The completed assessments are shown in the example. The state of each assessment is marked as Complete and it is highlighted in Green. You can open the completed assessments and view their details for reference at any time.

    ![Completed assessment.](../image/rto-assessment-completed.png)

9.  Select **Submit for review**.

    **Note:** Before submitting the business impact analysis for a review, verify that all assessments are complete and the name of the BCM lead is updated in the **BCM Lead** field on the **Details** tab.

    The business impact analysis is submitted for a review to the BIA owner or BCM lead. The business impact analysis is updated to the **In Review** state.

10. Review the assessments in the business impact analysis if you are the BIA owner or BCM lead.

    ![Generate the BIA PDF.](../image/bia-pdf-generate-pdf.png)

11. Select **Submit for approval**.

    The business impact analysis is updated to the **Pending approval** state.

    **Note:** If an approval record is already created for a BIA, the **Approve** or **Reject** buttons are not displayed in the BIA form.

12. Select **Save**.

13. Select the **Generate PDF** button to generate the BIA in a PDF format.

    A message appears that the PDF has been generated.

    ![Information message that includes a link to download a PDF](../image/PDFDownload.png "PDF download")

    Select the link in the message to download the PDF.

    -   If you have view-only access to the BIA, the option to generate a PDF helps you to download the document to your local hard drive.
    -   You can download the BIA before its **Approval** state.
    -   By default, the PDF is generated and attached after the BIA is approved.
14. To move a BIA from **Approved** to **Draft** state, select the **Edit** button.

15. To create a copy of the BIA, select the **Copy** button.

    If you have the permission to read and create a BIA, then you can also copy the BIA.

    1.  Enter the name of the new BIA in the Copy impact analysis pop-up.

        The copy action creates an exact replica of the BIA with the name that you enter in the Copy impact analysis pop-up. It also copies all its dependencies and dependency groups on to the new BIA.

    2.  Select **Confirm**.

        -   The new BIA that is copied from the original BIA has all the RTO, RPO impact, dependency assessment structural details similar to the original BIA.
        -   However, the impact category details for each of these assessments are editable for you to assess the dependency details exclusively for the copied BIA.
        -   When a BIA that has the RTO or RPO impacted assessments completed is copied, the new copied BIA won't have the new assessment in the **Pending** state. If the impact categories of the RTO and RPO impact assessments in the original BIA are in the **Complete** state, then the impact categories in the copied BIA are in the **Complete** state.
        -   Therefore, you must assess and enter the disruption duration, response, and required recovery timeframe relevant to the copied BIA.
        -   You can assess the details in the **Results** section. The RTO and RPO values are recalculated after you complete the assessments.
        -   Activities and Work notes are not copied to the new BIA. Enter this information relevant to the new BIA.
        -   Any attachments attached to the original BIA in any format are copied to the new BIA. However, the PDF generated for the original BIA using the **Generate PDF** button will not be copied over to the new BIA as the assessment data pertain to the original BIA. Since you have the flexibility to modify the assessment details in the copied BIA and generate a PDF, copying the PDF generated for the original BIA has no relevance.
        **Note:** You can delete a BIA \(and its related tables\) that is in the **Draft** state. BCM planner and program manager can delete a BIA that is in the **In Review** and **Returned** states, whereas a BCM admin can delete a BIA irrespective of its state.


**Parent Topic:**[Structured workflows for BIAs](../concept/bia-tasks-performed-by-bia-owner.md)

