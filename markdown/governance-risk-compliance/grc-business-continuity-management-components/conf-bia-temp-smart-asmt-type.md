---
title: Configure BIA templates with Smart Assessment
description: Configure a business impact analysis \(BIA\) template in the Business Continuity Workspace with the Smart Assessment. Select the type of the elements, impact categories, and dependencies that are assessed in the BIA. The Smart Assessment lets you choose a custom Smart Assessment template for the BIA.
locale: en-US
release: australia
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Setup for a BIA, Configure, Business Continuity Management, Governance, Risk, and Compliance]
---

# Configure BIA templates with Smart Assessment

Configure a business impact analysis \(BIA\) template in the Business Continuity Workspace with the Smart Assessment. Select the type of the elements, impact categories, and dependencies that are assessed in the BIA. The Smart Assessment lets you choose a custom Smart Assessment template for the BIA.

## Before you begin

Role required: sn\_bcm.admin

## About this task

A BIA created using the Smart Assessment template includes Smart Assessment instances in the assessment section. BCM users can complete the assessment, and upon submission, the automation set up by the BCM admin triggers to update impact analysis data, including RTO, RPO, and recovery tier, based on the defined configuration.

Impact category completion configuration for Smart Assessment: To configure Impact category completion for Smart Assessment, navigate to **All &gt; Business Continuity &gt; General Administration &gt; Properties**. Set the **Mark the Impact Assessment as Complete once all required questions are answered, or all questions \(required and optional\) are answered** property. Choose the preferred option to show completion based on required or all questions.

For the initial setup checklist for Smart Assessment Engine, see [Configuring Smart Assessment Engine](../../assessment-engine/concept/smart-assessment-engine-cf-config.md).

## Procedure

1.  Navigate to **All** &gt; **Business Continuity** &gt; **BIA Configuration** &gt; **BIA Templates**.

2.  Select **New**.

    You can use the preconfigured BIA templates in the instance or select this option to configure a new BIA template.

3.  On the form, fill in the fields.

    For more information on the fields in the form, see [BIA template form for the legacy assessment](../reference/bia-template-new-record-form.md).

4.  Select **Smart Assessment** as the assessment type.

    A sample BIA template with the Smart Assessment type is shown in the example.

    ![Smart Assessment type.](../image/bia-smart-asmt-type.png)

    When you select the Smart Assessment, the **Impact categories** field is not displayed in the BIA template form. Instead, the **Impact assessment templates** field is displayed. The templates shown, like Recovery point objective and Recovery time objective, are demo data with a format similar to legacy assessments.

    The Impact assessment template is the Smart Assessment template you configured following the steps outlined in [Create Smart Assessment templates for BIA](conf-impact-asmt-template.md).

5.  Choose the Impact assessment templates for assessments.

6.  Configure other settings as needed.

7.  To save the BIA template, select **Submit**.

8.  To display result fields on the assessment card in the Impact analysis record within the Workspace, open the BIA template, map the BIA fields to the Impact assessment template, and save the mapping.

    The BIA template with the Smart Assessment type is set up in the instance. The related list for the BIA template depends on the selected impact assessment template. For example, choosing the Recovery Point Objective template shows the same related list mapped to the BIA fields. For more information, see [Create Smart Assessment templates for BIA](conf-impact-asmt-template.md).

    ![Related list.](../image/bia-rel-list.png)

    Selecting the related list opens the Assessment template BIA fields record. Here, you can view a summary of RPO or RTO details and prioritize the field order on the card. Choose the BIA fields that the assessment contributes to, and they will be displayed on the BIA assessment card in the specified order. For example, if the selection shown in the diagram is used, the card displays the selected fields.

    ![BIA fields.](../image/asmt-temp-bia-field.png)

    The example shows the Recovery Point Objective card, Recovery Time Objective card, and Dependency assessment created for the BIA.

    ![Cards.](../image/bia-asmts-based-on-imp-asmt-templates.png)

    Previously, the **Assessments** tab showed a single assessment card and an **Open assessment** button. Beginning with the Yokohama release, the layout has been updated to a two-column arrangement. Assessment cards are now displayed dynamically, enabling you to attach multiple assessments to a BIA. For example, one card is shown alone in a row, while seven cards are arranged in four rows \(three rows with two cards each and one row with one card\).

    **Note:** The selected BIA fields are populated on the cards only if they are not empty.

    Selecting the Dependency assessment card opens the BIA assessment. When BCM users submit the assessment, the automation configured in the Smart Assessment template updates the configured result fields.


-   **[BIA template record form for the Smart assessment](../reference/bia-smart-temp-ref-form.md)**  
Use the BIA template record form to configure the business impact analysis with the Smart assessment. You can add details such as name, description, primary element assessed and select the impact assessment template in the form.

**Parent Topic:**[Setup for a business impact analysis](../concept/bcm-admin-tasks.md)

