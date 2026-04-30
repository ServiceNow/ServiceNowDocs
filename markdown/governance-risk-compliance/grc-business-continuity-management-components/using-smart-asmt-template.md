---
title: Using latest assessment template for conducting BIAs
description: Beginning with the Yokohama release, you can use the latest assessment template for conducting a Business Impact Analysis \(BIA\). The BIA template is now integrated with the Smart Assessment Engine, enabling you to use the Smart assessment along with the legacy assessment.
locale: en-US
release: yokohama
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Structured workflows for BIAs, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Using latest assessment template for conducting BIAs

Beginning with the Yokohama release, you can use the latest assessment template for conducting a Business Impact Analysis \(BIA\). The BIA template is now integrated with the Smart Assessment Engine, enabling you to use the Smart assessment along with the legacy assessment.

## Integrating BIA with the Smart Assessment Engine

Integrating business impact analysis \(BIA\) with the Smart Assessment Engine allows you to configure impact analysis assessments with various question types, set up multiple impact assessment templates for a single BIA, and calculate metrics such as Recovery Time Objective \(RTO\), Recovery Point Objective \(RPO\), Recovery Tier \(RT\), Maximum tolerable period of disruption \(MTPD\), and other based on user responses.

A BIA created with the Smart assessment template includes Smart assessment instances in the assessment section. The assessment template introduced with the Smart Assessment Engine allows you to create various question types and automate responses from existing data sources. BCM users can complete the assessment, and upon submission, the automation set up by the BCM administrator triggers to update impact analysis data, including recovery time objective \(RTO\), recovery point objective \(RPO\), recovery tier, or maximum tolerable downtime, based on the defined configuration.

## Components used for the integration

For BIA integration with the Smart Assessment Engine, the following BCM components are used:

-   BCM core
-   BIA
-   Smart Assessment Engine

## Workflow for integrating BIA with the Smart Assessment Engine

The ServiceNow® Smart Assessment Engine \(SAE\) application helps you to reduce the manual burden and costs of your assessment processes through automation.

You can create the assessment templates and add instructions, questions, and reference information by using the template designer in the Smart Assessment Engine application.

The Smart Assessment Engine uses the rule engine, where the rules are based on user responses. You can fill one assessment template \(only one assessment for RTO, RPO, and RT\) or multiple assessment templates \(one for each RTO, RPO, and RT\).

The workflow for integrating BIA with the Smart Assessment Engine is shown in the illustration.

![Workflow.](../image/bia-sae-workflow.png)

## Configuring BIA templates

You can configure the BIA template with the legacy or Smart assessment. The legacy assessment shows only drop-down questions, while the Smart assessment enables multiple question types and configures RTO, RPO, and recovery tier calculations based on the responses to the questionnaire. For more information, see [Setup for a business impact analysis](bcm-admin-tasks.md).

## Roles and responsibilities

The roles and responsibilities for the Smart assessment template are listed in the table.

<table id="table_cd2_5cd_ydc"><thead><tr><th>

Roles

</th><th>

Responsibilities

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Administrator \[admin\]

</td><td>

System administrator role that can set up the flow to update the BIA record based on the rules inside the Smart assessment template.

</td><td>

 

</td></tr><tr><td>

BCM administrator \[sn\_bcm.admin\]

</td><td>

BCM administrator role that can perform the following tasks:-   Read and write the Smart assessment template.
-   Configure the BIA template.
-   Configure rules inside the Smart assessment template.

</td><td>

-   \[sn\_smart\_asmt.template\_manager\]: Provides access to create a Smart assessment template.
-   \[sn\_smart\_imp\_auto.automation\_creator\]: Contains the Smart assessment impact automation creator role.

</td></tr><tr><td>

BCM core\_viewer \[sn\_bcm.core\_viewer\]

</td><td>

BCM core viewer role that can read the Smart assessment template.

</td><td>

-   \[sn\_smart\_asmt.assessment\_reader\]: Contains a Smart assessment reader role to give read access to Smart assessment instance.
-   \[sn\_smart\_imp\_auto.automation\_reader\]: Contains a Smart assessment impact automation reader role.
-   \[sn\_smart\_asmt.template\_reader\]: Contains a Smart assessment template reader role.

</td></tr><tr><td>

BCM Program Manager \[sn\_bcm.program\_manager\]

</td><td>

BCM Program Manager

</td><td>

-   \[sn\_smart\_asmt.actor\]: Contains the Smart assessment actor role to provide update access to the Smart assessment instance.
-   \[sn\_smart\_asmt.reassign\]: Contains the Smart assessment reassign role.

</td></tr><tr><td>

BCM Contributor \[sn\_bcm.contributor\]

</td><td>

BCM Contributor

</td><td>

-   \[sn\_smart\_asmt.actor\]: Contains a Smart assessment actor role to give update access to Smart assessment instance.
-   \[sn\_smart\_asmt.reassign\]: Contains the Smart assessment reassign role.

</td></tr><tr><td>

BCM Planner \[sn\_bcm.planner\]

</td><td>

BCM Planner

</td><td>

-   \[sn\_smart\_asmt.actor\]: Contains a Smart assessment actor role to give update access to Smart assessment instance.
-   \[sn\_smart\_asmt.reassign\]: Contains the Smart assessment reassign role.

</td></tr></tbody>
</table>**Note:** Smart assessment template category: The category for the BIA is created for the Smart Assessment Engine. The BCM core\_viewer \[sn\_bcm.core\_viewer\] role is assigned in the Smart assessment template category for the BIA.

<table id="table_zg3_ldd_ydc"><thead><tr><th>

Roles

</th><th>

Responsibilities

</th></tr></thead><tbody><tr><td>

BIA viewer \[sn\_bia.viewer\]

</td><td>

BIA viewer role that can read the assessment.

</td></tr><tr><td>

BIA contributor \[sn\_bia.contributor\]

</td><td>

BIA contributor role that can perform the tasks:-   Can read the assessment \(if you are in the contributor list of the BIA\).
-   Can take the assessment \(if you are in the contributor list of the BIA and the BIA is in the **Draft**, **In review**, and **Returned** state\).

</td></tr><tr><td>

BIA planner \[sn\_bia.planner\]

</td><td>

BIA planner role that can perform the tasks:-   Can read the assessment \(if you are the owner of the BIA\).
-   Can take the assessment \(if you are the owner of the BIA and the BIA is in the **Draft**, **In review**, and **Returned** state\).

</td></tr><tr><td>

BIA manager \[sn\_bia.manager\]

</td><td>

BIA manager role that can perform the tasks:-   Can read the assessment.
-   Can respond to the assessment when the BIA is in the **Draft**, **In review**, or **Returned** state.

</td></tr></tbody>
</table>## UI actions

The UI actions used for performing the Smart assessment are listed in the table.

|Roles|Responsibilities|
|-----|----------------|
|**Open assessment**|Action to open the assessment. The BIA viewer, BIA contributor, BIA planner, and BIA manager can read the impact analysis and they can also view the **Open assessment** UI action. This UI action redirects you to the Smart assessment page in read-only mode.|
|**Edit assessment**|Action to edit the assessment. The BIA planner, BIA contributor, and BIA manager can write the impact analysis and they can also view the **Edit assessment** UI action. This UI action redirects you to the Smart assessment page in edit mode.|

## UI page with the Smart assessment component for an assessment instance

The UI page containing only the Smart assessment component is created in the BCM core application and it can be accessed by the BCM Workspace users. This page allows users to open the Smart assessment in read-only or edit mode.

## User experience

-   BCM administrators can configure the Smart assessment template from the Business Continuity Workspace.
-   You can view the Smart assessment instance card in the assessment list from the **Assessments** tab in the BIA, if the BIA template is configured to use the Smart assessment template.
-   For the Smart assessment instance card, you can either view both **Edit assessment** and **Open assessment**, or only the **Open assessment** button based on your role.
-   The **Open assessment** action opens the Smart assessment page for you to read the responses.
-   The **Edit assessment** action opens the Smart assessment page for you to edit the responses.

**Parent Topic:**[Structured workflows for BIAs](bia-tasks-performed-by-bia-owner.md)

