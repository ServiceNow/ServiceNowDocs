---
title: Structured workflows for BIAs
description: Perform the tasks that are outlined in this section to create a business impact analysis in Business Continuity Workspace \(also known as BCM Configurable Workspace\).
locale: en-US
release: xanadu
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Structured workflows for BIAs

Perform the tasks that are outlined in this section to create a business impact analysis in Business Continuity Workspace \(also known as BCM Configurable Workspace\).

Typically, the business impact analysis owner performs the following tasks:

-   Create a business impact analysis. For more information, see [Create a business impact analysis](../task/create-bia-in-uib-ws.md).
-   Assess the impact categories and submit the analysis for a review and approval.

    **Note:** If an approval record is already created for a BIA, the **Approve** or **Reject** buttons are not displayed in the BIA form.

    For more information, see [Assess impact categories and dependencies](../task/assess-impact-categories-bia-in-uib-ws.md).

-   As the BCM lead, approve the BIA. For more information, see [Approve the business impact analysis](../task/approve-bia-in-uib-ws.md).
-   Generate and save the PDF of the analysis for reference.

## BIA updates in the Xanadu release

Beginning with the Xanadu release, the reliability of business impact analysis is enhanced through the implementation of following updates.

-   Access the latest BIAs of the dependent items and their recovery objectives such as Recovery Time Objectives \(RTOs\), Recovery Point Objectives \(RPOs\), and Recovery Tiers.
-   Configure the columns in the dependency assessment of a BIA.
-   Schedule automated updates for the dependencies from the CMDB.
-   Configure the updates to be done after a manual review.

**Note:** If an approval record is created for a BIA, the **Approve** or **Reject** button is not displayed on the BIA form. For a user to view the **Approve** or **Reject** button, the following conditions must be fulfilled:

-   The user should have the sn\_bia.bia\_manager role.
-   The BIA should be in the **Pending approval** state.
-   The BIA should not have any approval records created.

## Additional information on Business Impact Analysis

-   For information on the **Business impact analysis** tab in the Home page, see [Home page view](home-page-uib-ws.md).
-   For information on business impact analysis, see [Business impact analysis](bia-uib.md).
-   For information on the administrative tasks in business impact analysis, see [Setup for a business impact analysis](bcm-admin-tasks.md).

-   **[Impact categories and ratings](bia-impact-categories.md)**  
Impact categories are the types of an impact that you can assess during a business impact analysis. The BCM administrator of an organization is responsible for defining the impact categories and the timeframe during which an organization may experience a downtime. This information is used to determine the recovery time objective and recovery point objective of the assets.
-   **[RTO, RPO, and recovery tiers](rto-rpo-recovery-tiers.md)**  
Due to unforeseen disruptive events, the business processes in your organization can face a downtime. It is important to classify your business processes in the recovery tiers and calculate the amount of time and amount of data loss that your organization can handle without significant effect on the operations.
-   **[Calculating RTO and RPO](rto-rpo-calculation.md)**  
The BCM application provides an assessment questionnaire for calculating the recovery time objective \(RTO\) and recovery point objective \(RPO\) in the business impact analysis \(BIA\). As a pre-requisite to the BIA, the BCM administrator defines the impact ratings and sets up the assessment questions. After receiving the responses to the assessment, the BCM application calculates the RTO and RPO.
-   **[BIA states and UI actions](states-ui-actions-bia.md)**  
When you create a business impact analysis, certain UI actions are associated with each state.
-   **[Configuring Dictionary, UI policy, element variables](bcm-enhanced-bia-logic.md)**  
Starting with Release 6.1.x, administrators have the capability to configure different aspects of a dependency. This includes the Dictionary, UI policy, element variables, and UI view. These configurations play a crucial role in determining specific columns, required fields, and overall display in the list view and form view of a dependency within the dependency assessment of a BIA.
-   **[Using latest assessment template for conducting BIAs](using-smart-asmt-template.md)**  
Beginning with the Yokohama release, you can use the latest assessment template for conducting a Business Impact Analysis \(BIA\). The BIA template is now integrated with the Smart Assessment Engine, enabling you to use the Smart assessment along with the legacy assessment.
-   **[Create a business impact analysis](../task/create-bia-in-uib-ws.md)**  
Create a business impact analysis in BCM UI Builder Workspace to get the necessary information for a plan.
-   **[Scheduling auto-update of dependencies](update-impactanalysis-dep-based-on-cmdb-changes.md)**  
You can schedule an auto-update of the dependencies in the business impact analysis based on the source data and relationships in the CMDB. You can receive an email notification with details of the BIA dependency updates from the BCM application.
-   **[Assess impact categories and dependencies](../task/assess-impact-categories-bia-in-uib-ws.md)**  
Assess the impact categories and dependencies in BCM UIB Workspace to get the necessary information for a plan. Use the business impact analysis to identify the recovery time objective for an item and prioritize the assets that have the least and most critical dependencies. Use the information to establish their recovery strategies during the planning phase.
-   **[Approve the business impact analysis](../task/approve-bia-in-uib-ws.md)**  
Approve the business impact analysis in BCM UI Builder Workspace in the BCM application. If you’re the business impact analysis owner or the BCM lead for the business impact analysis, you can approve the business impact analysis.
-   **[Update dependencies of BIAs in Self-Service](../task/update-dependency-details-of-BIA-in-self-service-as-contributor.md)**  
Use the contributor role to update the impact category result, RPO Impact analysis responses, state of the impact dependency group, and the work notes in the **Activity** section in the BCM application.
-   **[Visualize 360° relationships for BIAs](../task/visualize-360-degree-view-for-bia.md)**  
Visualize the 360° relationships for a business impact analysis and its associated entities in BCM UIB Workspace. You can access the 360° view at any time while creating a business impact analysis.
-   **[Generate BIA reports in PDF or Microsoft Word formats](../task/generate-pdf-for-bia.md)**  
Generate a PDF or Microsoft Word copy of a business impact analysis in the BCM Configurable Workspace and save it for a future reference.

**Parent Topic:**[Managing BCM workflow tasks](manage-bcm-with-uib-workspace.md)

