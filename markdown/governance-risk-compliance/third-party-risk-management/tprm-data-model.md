---
title: Third-party risk management data model
description: Use the Third-party Risk Management \(TPRM\) data model to assess, monitor, and mitigate the risks for your risk management program.
locale: en-US
release: yokohama
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 10
breadcrumb: [Reference, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Third-party risk management data model

Use the Third-party Risk Management \(TPRM\) data model to assess, monitor, and mitigate the risks for your risk management program.

## TPRM data model overview

The Third-party Risk Management application is one of the Governance, Risk, and Compliance products.

The following model is used to support TPRM's capabilities.

![Relationship between due diligence, third-party management, policy and compliance, and risk main tables. For a text description, refer to the text that follows.](../image/tprm-data-model.png "TPRM data model")

The third-party risk assessment data model includes various components and relationships:

Components:

-   Risk intelligence score \[sn\_vdr\_risk\_asmt\_security \_score\]
-   Internal assessment \[sn\_vdr\_asmt\_internal\_assessment\]
-   Tiering assessment \[sn\_vdr\_risk\_asmt\_vdr\_tiering\_assessment\]
-   Event-driven management history \[sn\_tprm\_dd\_rule\_execution\_history\]
-   Third-party due diligence request \[sn\_tprm\_dd\_request\]
-   Company \[core\_company\]
-   Event-driven management rule \[sn\_tprm\_dd\_generation\_rule\]
-   Third-party risk assessment \[sn\_vdr\_risk\_asmt\_assessment\]
-   Third-party engagement \[sn\_vdr\_risk\_asmt\_vendor\_engagement\]
-   Vendor contact \[vm\_dr\_contact\]
-   Assessment metric type \[asmt\_metric\_type\]
-   Assessment template \[sn\_vdr\_risk\_asmt\_assessment\_template\]
-   Third-party risk issue \[sn\_vdr\_risk\_asmt\_issue\]
-   Engagement risk scoring rule \[sn\_vdr\_risk\_asmt\_engagement\_risk\_scoring\_rule\]
-   Engagement level risk rating \[sn\_vdr\_risk\_asmt\_engagement\_level\_rating\]
-   Risk \[sn\_risk\_risk\]
-   Control \[sn\_compliance\_control\]

Relationships:

-   The third-party risk assessment component can have a one-to-many relationship with the following components:
    -   Event-driven management histories
    -   Third-party due diligence requests
    -   Company
    -   Third-party engagements
    -   Third-party risk issues
    -   Assessment templates
-   The Event-driven management histories component can have a many-to-one relationship with the Event-driven management rules component.
-   The Event-driven management rules component can have a one-to-many relationship with the Assessment metric type component and the Assessment template component.
-   The third-party engagement component can have a one-to-many relationship with the following components:
    -   Company
    -   Engagement risk scoring rule
    -   Third-party risk issue
-   The Third-party engagement component can have a many-to-many relationship with the Vendor contact component.
-   The Vendor contact component can have a one-to-many relationship with the Company and a Third-party risk issue component.
-   The Engagement level risk rating component can have a one-to-many with the Third-party engagement component.
-   The Third-party engagement component is related to the Risk and Control component.
-   The Risk intelligence score component is related to the Third-party due diligence component.
-   The Tiering assessment component can have a one-to-many relationship with the following components:
    -   Third-party due diligence
    -   Third-party engagement
    -   Company
-   The Tiering assessment component can have a many-to-many relationship with the Assessment metric type component.
-   The Third-party due diligence component can have one-to-many relationships with the following components:
    -   Event-driven management history
    -   Third-party risk assessment
    -   Company
-   The following components are related to Risk due diligence:
    -   Event-driven management rule
    -   Event-driven management history
    -   Third-party risk due diligence request
-   The following components are related to Third-party management:
    -   Risk intelligence score
    -   Internal assessment
    -   Tiering assessment
    -   Third-party risk assessment
    -   Third-party engagement
    -   Assessment template
    -   Third-party risk issue
    -   Engagement risk scoring rule
    -   Engagement level risk rating
-   The internal assessment component is an extension of the tiering assessment component.
-   The Control component is related to Policy and Compliance Management.
-   The Risk component is related to Risk Management.
-   The following components are Global:
    -   Vendor contact
    -   Company
    -   Assessment metric type

The following table lists the roles that are required for the components in the TPRM data model.

|Role|Description|
|----|-----------|
|sn\_vdr\_risk\_asmt.approver|Approve due diligence requests in the third-party risk management process.|
|sn\_vdr\_risk\_asmt.contract\_negotiator|Work in the contract risk process stage of the onboarding process.|
|sn\_vdr\_risk\_asmt.vendor\_assessment\_reviewer|Edit assessments.|
|sn\_vdr\_risk\_asmt.vendor\_assessor|Manage third parties, third-party contacts, third-party risk assessments, and issues, and complete third-party risk assessment requests.|
|sn\_vdr\_risk\_asmt.vendor\_risk\_admin|Have full control over all vendor risk management data and assessment metric types.|
|sn\_vdr\_risk\_asmt.vendor\_risk\_manager|Manage third parties, third-party contacts, third-party assessment templates, questionnaire templates, documentation request templates, and scheduled assessments.|

For more information on the roles, see [Roles in Third-party Risk Management](../../grc-vendor-risk-implementation/reference/tprm-roles.md).

## Core components

TPRM is based on sending assessments and calculating scores from the received responses.

You can use these core components to perform assessments:

-   Third-party risk assessment
-   Third-party engagement
-   Third-party due diligence
-   Scoring setup
-   Risk intelligence

The following diagram shows the main tables and flow for a third-party risk assessment of the TPRM data model.

![Relationship between due diligence, third-party management, policy and compliance, and risk main tables or third-party risk assessments. For a text description, refer to the text that follows.](../image/tprm-tpra-data-model.png "Third-party risk assessment data model")

Here are the components and relationships that make up the Third-party risk assessment data model.

Components:

-   Internal assessments \[sn\_vdr\_risk\_asmt\_internal\_assessment\]
-   Tiering assessments \[sn\_vdr\_risk\_asmt\_vdr\_tiering\_assessment\]
-   External assessments \[sn\_vdr\_risk\_asmt\_assessment\]
-   Assessment template \[sn\_vdr\_risk\_asmt\_template\]
-   Questionnaire templates \[asmt\_metric\_type\]
-   Questionnaire instance \[asmt\_assessment\_instance\]
-   Category \[asmt\_metric\_category\]
-   Metric \[asmt\_metric\]

Relationships:

-   The Metric component can have a many-to-one relationship with the Category component.
-   The Category component can have a many-to-one relationship with the Questionnaire component.
-   The Questionnaire templates component can have a many-to-one relationship with the following components:
    -   Assessment template
    -   Tiering assessments
    -   External assessments
-   The Questionnaire instance component can have a many-to-one relationship with the following components:
    -   External assessments
    -   Tiering assessments
-   The Assessment template component can have a one-to-many relationships with the following components:
    -   Tiering assessments
    -   External assessments
-   The Internal assessment component is an extension of the Tiering assessment component.
-   The Internal assessment components are related to Risk due diligence.
-   The following components are related to Third-party management:
    -   Tiering assessments
    -   External assessments
    -   Assessment templates
-   The following components are Global:
    -   Questionnaire templates
    -   Category
    -   Metric
    -   Questionnaire instance

For more information on assessments, see [Assessing your third-party risk](../concept/tprm-assessing-tpr.md).

The following diagram shows the main tables and flow that are used for the due diligence in the TPRM data model.

![Relationship between the risk due diligence, third-party management, policy and compliance, and risk main tables used for due diligence. For a text description, refer to the text that follows.](../image/tprm-dd-data-model.png "Due diligence data model")

Here are the components and relationships that make up the due diligence data model.

Components:

-   Third party \[core\_company\]
-   Engagements \[sn\_vdr\_risk\_asmt\_vendor\_engagement\]
-   Due diligence \[sn\_tprm\_dd\_request\]
-   Issues \[sn\_vdr\_risk\_asmt\_issue\]
-   Tasks \[sn\_vdr\_risk\_asmt\_task\]
-   Vendor contacts \[vm\_vdr\_contact\]
-   Risk intelligence scores \[sn\_vdr\_risk\_asmt\_security\_score\]
-   External assessments \[sn\_vdr\_risk\_asmt\_assessment\]
-   Tiering assessments \[sn\_vdr\_risk\_asmt\_vdr\_tiering\_assessment\]
-   Internal assessments \[sn\_vdr\_risk\_asmt\_vdr\_internal\_assessment\]

Relationships:

-   The Third party component has a one-to-many relationship with subsidiaries.
-   The Third party component has a one-to-many relationship with the following components:
    -   Vendor contacts
    -   Internal assessments
    -   External assessments
    -   Tiering assessments
    -   Risk intelligence scores
    -   Issues
    -   Tasks
-   The Due diligence component has a one-to-many relationship with the following components:
    -   Vendor contacts
    -   Internal assessments
    -   Tiering assessments
    -   Risk intelligence scores
-   The Engagements component has a one-to-many relationship with the following components:
    -   Vendor contacts
    -   Internal assessments
    -   External assessments
    -   Tiering assessments
    -   Issues
    -   Tasks
-   The Third party component is related to the Due diligence component.
-   The Engagements component is related to the Due diligence component.
-   The External assessments component is related to the Due diligence component.
-   The Internal assessment component is an extension of the Tiering assessment component.
-   The following components are related to Risk due diligence:
    -   Due diligence
    -   Internal assessments
-   The following components are related to Third-party management:
    -   Engagements
    -   Issues
    -   Tasks
    -   Risk intelligence scores
    -   External assessments
    -   Tiering assessments
-   The following components are Global:
    -   Third party
    -   Vendor contact

The following diagram shows the required roles, processes, and choices that are part of the due diligence workflow.

![Work flow that shows the required roles, processes, and choices that exist as part of the due diligence workflow.](../image/tprm-ddw-data-model.png "Due diligence workflow")

For more information on the due diligence workflow, see [Due diligence workflow](../../grc-workspace-vrm/concept/tprm-workflow-in-workspace.md).

The following diagram shows the main tables that are used for scoring the TPRM data model.

![Relationship between due diligence, third-party management, policy and compliance, and risk main tables that are used for scoring risk. For a text description, refer to the text that follows.](../image/tprm-score-data-model.png "Scoring data model")

Here are the components and relationships that make up the scoring data model.

Components:

-   Third party \[core\_company\]
-   Third-party risk scoring rule \[sn\_vdr\_risk\_asmt\_vendor\_risk\_scoring \_rule\]
-   Component criteria \[sn\_vdr\_risk\_asmt\_component\_criteria\]
-   Components \[sn\_vdr\_risk\_asmt\_component\]
-   Engagement \[sn\_vdr\_risk\_asmt\_vendor\_engagement\]
-   Engagement risk scoring rule \[sn\_vdr\_risk\_asmt\_engagement\_risk\_scoring\_rule\]
-   Risk area criteria \[sn\_vdr\_risk\_asmt\_\_risk\_area\_criteria\]
-   Risk domains \[sn\_vdr\_risk\_asmt\_risk\_area\_definition\]

Relationships:

-   The Risk area criteria component has a one-to-many relationship with the Risk domain component.
-   The Risk area criteria component has a one-to-one relationship with the Engagement risk scoring rule component and the Third-party risk scoring rule component.
-   The Engagement risk scoring rule has a one-to-many relationship with the Engagement component.
-   The Component criteria has a one-to-many relationship with Components.
-   The Component criteria has a one-to-one relationship with the Third-party risk scoring rule component.
-   The Third-party risk scoring rule component has a one-to-many relationship with the Third-party component.
-   All of these components are related to Third-party management.

Use the scoring setup in TPRM configure how the scores from the external risk assessments are aggregated to the engagements and third parties. The criteria tables have the information that is related to the aggregation of the scores of multiple records \(MIN, MAX, AVG\) or from multiple tables \(weights for each table\). Use the scoring rules to group third parties or engagements and assign criteria. You can configure all the records in these tables without any customization.

For more information on scoring, see [Scoring calculations using the classic assessment engine](../concept/vendor-ratings-scoring.md).

The following model diagram shows the main tables that are used for risk intelligence in the TPRM data model.

![Relationship between the risk due diligence, third-party management, policy and compliance, and risk main tables. For a text description, refer to the text that follows.](../image/tprm-ri-data-model.png "Risk intelligence model")

Here are the components and relationships that make up the Risk intelligence data model.

Components:

-   Third party \[core\_company\]
-   Provider Services \[sn\_vdr\_risk\_asmt\_tpss\_provider\]
-   Risk intelligence scores \[sn\_vdr\_risk\_asmt\_security\_score\]
-   Score subfactors \[sn\_vdr\_risk\_asmt\_tpss\_subfactor\]

Relationships:

-   The Risk intelligence providers component has a one-to-many relationship with the Providers Services component.
-   The Providers Services component has a one-to-many relationship with the Risk intelligence scores component.
-   The Risk intelligence scores component has a one-to-many relationship with the Scores subfactors component.
-   The Risk intelligence scores component is related to the Risk intelligence providers component.
-   All of these components are related to Third-party management.

For more information on risk intelligence, see [Risk intelligence report requests management](../../grc-workspace-vrm/reference/tprm-ws-dd-mgt-pg-rir-tab.md).

## SAE TPRM data model

The following model diagram shows the main tables that are used for Smart Assessment Engine in TPRM.

![For a text description, refer to the text that follows.](../image/tprm-sae-data-model.png "SAE TPRM data model")

Here are the components and relationships that make up the SAE TPRM data model.

Components:

-   Assessment to SAE Questionnaire Templates \[sn\_vdr\_risk\_asmt\_m2m\_tiering\_sae\_template, sn\_vdr\_risk\_asmt\_m2m\_tpra\_sae\_template\]
-   TPRM Assessments \[sn\_vdr\_risk\_asmt\_assessment, sn\_vdr\_risk\_asmt\_internal\_assessment\]
-   Engagement \[sn\_vdr\_risk\_asmt\_vendor\_engagement\]
-   Scoring Rules \[sn\_vdr\_risk\_asmt\_vendor\_risk\_scoring\_rule, sn\_vdr\_risk\_asmt\_engagement\_risk\_scoring\_rule\]
-   SAE Instance \[sn\_smart\_asmt\_instance\]
-   SAE Questionnaire Template \[sn\_vdr\_risk\_asmt\_sae\_questionnaire\_template\]
-   SAE Rating Scale \[sn\_vdr\_risk\_asmt\_sae\_rating\_scale\]
-   Scoring Normalization \(represented by SAE rating scale and score‑mapping tables: sn\_vdr\_risk\_asmt\_sae\_rating\_scale, sn\_vdr\_risk\_asmt\_score\_mapping\)
-   Issue-generation rule \[sn\_vdr\_risk\_asmt\_issue\_generation\_rule\]
-   Post-assessment Automation \(issue generation, workflow triggers\)

Relationships:

-   The Assessment to SAE Questionnaire Templates component has a many-to-one relationship with TPRM assessments.
-   The Assessment to SAE Questionnaire Templates component has a one-to-one relationship with the SAE instance component.
-   The TPRM Assessments component has a many-to-one relationship with the Engagement component.
-   The Engagement component has a many-to-one relationship with the Scoring Rules component.
-   The SAE Questionnaire Template component has a many-to-many relationship with the SAE Rating Scale component.
-   The SAE Rating Scale component has a one‑to‑many relationship with the Scoring Normalization component.
-   The SAE Questionnaire Template component has a many-to-one relationship with the Issue-generation rule component.
-   The SAE Questionnaire Template component has a one-to-many relationship with the Post-assessment Automation component.

For more information on Smart Assessment Engine and TPRM, see [Smart assessments with Third-party Risk Management](../concept/tprm-sae-using.md).

**Parent Topic:**[Third-party Risk Management reference](../concept/tprm-reference.md)

