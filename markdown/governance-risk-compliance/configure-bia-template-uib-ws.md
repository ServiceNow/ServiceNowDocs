---
title: Configure BIA templates with legacy assessment
description: Configure a business impact analysis \(BIA\) template in the Business Continuity Workspace with a legacy assessment. Select the type of elements, impact categories, and dependencies to be assessed. The legacy assessment uses the older method of selecting impact categories.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Setup for a BIA, Configure, Business Continuity Management, Governance, Risk, and Compliance]
---

# Configure BIA templates with legacy assessment

Configure a business impact analysis \(BIA\) template in the Business Continuity Workspace with a legacy assessment. Select the type of elements, impact categories, and dependencies to be assessed. The legacy assessment uses the older method of selecting impact categories.

## Before you begin

Role required: sn\_bcm.admin

## About this task

You can use the preconfigured BIA templates that are provided with the base system.

-   Application Technical Impact Assessment
-   BIA for Business processes
-   Business Process Impact Assessment
-   Business Service Impact Assessment
-   Data Center Analysis Template
-   Service Offering Impact Assessment
-   Workplace Impact Assessment

Beginning with the Yokohama release, you can configure the BIA template with the legacy or Smart assessment. The legacy assessment shows only drop-down questions, while the Smart assessment enables multiple question types and configures RTO, RPO, and recovery tier calculations based on the responses to the questionnaire.

## Procedure

1.  Navigate to **All** &gt; **Business Continuity** &gt; **BIA Configuration** &gt; **BIA Templates**.

    You can use the preconfigured BIA templates provided with the instance or select this option to configure a new BIA template.

2.  Select **New**.

    The BIA template record is displayed.

    ![BIA template new record.](../image/new-bia-temp-record.png)

3.  On the form, fill in the fields.

    For more information on the fields in the form, see [BIA template form for the legacy assessment](../reference/bia-template-new-record-form.md).

4.  Add the name and description for the BIA template.

5.  Select the type of elements that are using this template, such as, Business Processes.

6.  To select the legacy assessment for performing the BIA, select **Legacy assessment** in the **Assessment type** field.

    A sample BIA template with the legacy assessment is shown in the example.

    ![BIA template Legacy assessment.](../image/bia-temp-legacy-asmt.png)

7.  To assess the type of impact, select the impact category in the **Impact categories** field.

    You can select different impact categories such as Legal impact, Regulatory impact, Reputation impact, or Revenue impact. Based on the impact category, you can calculate the recovery time objective \(RTO\) and recovery point objective \(RPO\). For information on configuring the impact category of the BIA, see [Configure impact category for BIA](configure-impact-category-uib-ws.md).

8.  Select the dependencies in the **Dependency assessments** field.

9.  To include Confidentiality, Integrity, and Availability \(CIA\) information for the primary element in the BIA, select **Yes**.

    A sample BIA template is shown in the example.

    ![Sample BIA template.](../image/bia-legacy.png)

10. Select **Update**.

    The BIA template with the legacy assessment is configured in the instance.


-   **[BIA template form for the legacy assessment](../reference/bia-template-new-record-form.md)**  
Use the BIA template form to configure the business impact analysis with the legacy template. You can add details such as name, description, elements, impact categories, and so on in the form.

**Parent Topic:**[Setup for a business impact analysis](../concept/bcm-admin-tasks.md)

