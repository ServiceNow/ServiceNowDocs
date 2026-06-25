---
title: Assessment templates
description: The AI Risk and Compliance application uses assessment templates to evaluate AI assets for risk, regulatory compliance, and ethical alignment.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/ai-risk-management/airc-assessment-templates.html
release: australia
product: AI Risk Management
classification: ai-risk-management
topic_type: concept
last_updated: "2026-06-09"
reading_time_minutes: 15
keywords: [assessment templates, smart assessment engine, post assessment actions, AI Risk and Compliance]
breadcrumb: [AI governance life cycle, Explore, AI Risk and Compliance, Governance, Risk, and Compliance]
---

# Assessment templates

The AI Risk and Compliance application uses assessment templates to evaluate AI assets for risk, regulatory compliance, and ethical alignment.

## Assessment templates overview

Assessment templates define the questionnaires and evaluation criteria used during AI assessments.

## Smart assessment engine

SAE is the underlying assessment platform that AI Risk and Compliance \(AIRC\) uses to create, manage, and complete all AI assessments. SAE provides the infrastructure for assessment templates, question design, section-based organization, scoring, and collaborative assessment workflows.

AIRC uses the SAE components installed with the AI Risk and Compliance Content application to support assessment creation, scoring, and automation.

After upgrading to version 22.3.5, if you have the AI risk and compliance admin \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_admin\] role, assessment templates support an explicit versioning lifecycle. A new version is created automatically each time you edit and save a template. Publishing a new version retires the previously published version. You can delete template versions that are no longer needed. Existing templates initialize as Version 1 after upgrading. List views and filters in the Assessment Workspace reflect version status, so you can identify which version of a template is currently published.

**Important:** Only one version of a template can be in a Published state at a time. Publishing a new version automatically retires the previous published version.

For more information on template versioning in SAE, see [Template versioning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/template-versioning.md).

## Assessment workspace

AIRC managers \(sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_manager\) manage assessment templates through the Assessment Workspace. Navigate to **Workspaces** &gt; **Assessment Workspace** to view, edit, and publish assessment templates. The workspace displays the template name, published state, and associated metadata for each template.

Use the Assessment Workspace to perform the following actions:

-   View all available assessment templates and their published state.
-   Open a template to review or edit its sections, questions, and scoring logic.
-   Publish draft templates to make them available for use in assessments.
-   Create assessment templates to support custom assessment requirements.

**Note:** Assessment templates are delivered in **Draft** state and must be published before they can be used in assessments. If you have the AIRC manager \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_manager\] role you can publish assessments. To publish a template, navigate to **All** &gt; **Assessment Workspace**, open the template, and select **Publish**. Only one version of a template can be in a **Published** state at a time. Role required: sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_manager. For more information on creating and editing assessments using Smart Assessment Engine, see [Create an assessment template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/sae-asmnt-template-create.md) and [Post-assessment automations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/impact-automation.md).

## Assessment template structure

Each assessment template defines the following components:

-   **Sections**

    Logical groupings that organize related questions within the assessment. Sections provide structure and navigation during assessment completion.

-   **Questions**

    Individual evaluation criteria that assessors respond to during the assessment. Questions can include multiple choice, free text, rating scales, and other response types.

-   **Scoring logic**

    Rules that calculate scores based on assessment responses. Scoring logic determines how individual responses contribute to overall assessment results.

-   **Risk and control mappings**

    Associations between specific responses and predefined risk statements or control objectives. These mappings drive automatic generation of governance records through Post Assessment Actions.


## Post assessment actions

Post Assessment Actions for Smart Assessments \(sn\_smart\_imp\_auto\) provides the automation framework that generates governance records based on assessment responses. When a user completes an assessment, the system evaluates the responses against configured automation rules and creates applicable risks, controls, and other records.

While predefined risk statements and control objectives are delivered through the content library, the conditions that trigger their application are configurable and must be reviewed and validated by each organization.

This framework is critical to the assessment workflow. Without Post Assessment Actions, assessment responses don't automatically generate the risk statements and control objectives that drive downstream governance activities.

The sn-reusable-impact-framework application \(sn\_impact\_fwk\), which is installed with Post Assessment Actions for Smart Assessments, provides the reusable framework components that Post Assessment Actions uses in AI Risk and Compliance.

## How post assessment actions work in AI risk and compliance

When an AI Asset Owner \(sn\_ai\_asset\_mgmt.ai\_asset\_owner\) responds to questions in a Fundamental Rights Impact Assessment \(FRIA\), Post Assessment Actions can evaluate the responses against configured automation rules. If the rule criteria are satisfied, the following sequence occurs:

1.  The system evaluates the assessment responses against the automation rules configured for the assessment template.
2.  Based on the responses, the system identifies applicable risk statements and control objectives from the content library.
3.  The system associates the identified risk statements and control objectives with the assessment record.
4.  After the AI Risk and Compliance analyst \(sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_analyst\) marks the assessment as closed complete, the system generates risk and control records and maps them to the AI asset.

Before governance records are finalized, an AI Risk and Compliance analyst reviews the prescribed list of generated risks and control objectives. This review step helps verify that automatically generated records are accurate, relevant, and appropriate for the specific AI system.

**Note:** Assessment templates do not include pre-configured automation rule mappings. Automation rules that map risk statements and control objectives to AI assets must be configured by your organization before post-assessment actions generate governance artifacts.

## Business configuration

Business configuration enables organizations to tailor assessment automation and risk evaluation behavior to their governance, regulatory, and operational requirements. These configurations are typically performed by AI Risk and Compliance administrators.

-   **Post-assessment actions configuration**

    The AI Risk and Compliance admin \(sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_admin\) configures post-assessment automation rules that determine how assessment responses trigger the association and classification of governance elements for an AI system. These rules govern how control objectives, risk statements, and system characteristics are automatically applied after an assessment is completed and marked as Closed complete.

    Post-assessment actions support a range of action types that translate assessment responses into governance classifications and associations for AI systems, covering areas of use, data categories, output types, affected populations, and human involvement. These action types enable consistent traceability between assessment outcomes and risk and compliance artifacts.

    |Actions|Description|
    |-------|-----------|
    |Map control objectives to AI systems|Links applicable control objectives from your inventory to the AI system in response to the questions profiled for Impact Assessment.|
    |Map risk statements to AI systems|Links applicable risk statements from your registry to the AI system in response to the questions profiled for Impact Assessment.|
    |Map area where the AI system is used: Customer Services|Classifies the AI system as being used in Customer Services to support impact assessment, regulatory risk classification, and governance reporting.|
    |Map area where the AI system is used: External Partner Ecosystem|Classifies the AI system as being used within the External Partner Ecosystem to support risk analysis, third-party impact evaluation, and compliance reporting.|
    |Map area where the AI system is used: Finance &amp; Accounting|Classifies the AI system as supporting Finance &amp; Accounting activities to support regulatory risk classification, control applicability, and governance oversight.|
    |Map area where the AI system is used: HR &amp; Workforce|Classifies the AI system as being used in HR &amp; Workforce contexts to support workforce impact assessment, compliance obligations, and governance requirements.|
    |Map area where the AI system is used: Internal Operations|Classifies the AI system as supporting Internal Operations to support impact evaluation, control requirements, and governance reporting.|
    |Map area where the AI system is used: IT &amp; Security|Classifies the AI system as being used in IT &amp; Security functions to support assessment of operational risk, control applicability, and governance readiness.|
    |Map area where the AI system is used: Sales &amp; Marketing|Classifies the AI system as being used in Sales &amp; Marketing to support impact assessment, risk evaluation, and governance reporting.|
    |Map area where the AI system is used: Supply Chain|Classifies the AI system as being used in Supply Chain activities to support impact evaluation, regulatory risk classification, and governance oversight.|
    |Map data used by the system: Behavioral or Usage Data|Associates Behavioral or Usage Data with the AI system to document data categories used for impact assessment, risk evaluation, and compliance analysis.|
    |Map data used by the system: Business Operational Data|Associates Business Operational Data with the AI system to support assessment of data-related risk, control applicability, and compliance requirements.|
    |Map data used by the system: Customer Interaction Data|Associates Customer Interaction Data with the AI system to support evaluation of customer impact, data protection considerations, and governance reporting.|
    |Map data used by the system: Profile or Account Data|Associates Profile or Account Data with the AI system to document use of identifiable data for risk, impact, and compliance assessment.|
    |Map data used by the system: Public or General Info|Associates Public or General Information with the AI system to document data sources used and support transparency and risk evaluation.|
    |Map data used by the system: Sensitive Business Data|Associates Sensitive Business Data with the AI system to support heightened risk evaluation, control requirements, and governance oversight.|
    |Map intended outcome of the AI system|Captures the intended outcome and purpose of the AI system to support impact assessment, risk classification, and governance decision-making.|
    |Map interaction type with end users|Captures how end users interact with the AI system to support assessment of transparency, user impact, and governance requirements.|
    |Map level of human involvement|Captures the degree of human oversight or intervention associated with the AI system to support accountability, control applicability, and governance readiness.|
    |People affected by the AI system: External Partners|Identifies External Partners as affected stakeholders to support impact assessment, risk evaluation, and accountability analysis.|
    |People affected by the AI system: General Customer Base|Identifies the General Customer Base as affected stakeholders to support evaluation of customer impact, risk, and compliance obligations.|
    |People affected by the AI system: Internal Team|Identifies Internal Teams as affected stakeholders to support workforce impact assessment and governance accountability.|
    |People affected by the AI system: Public or Large Audiences|Identifies Public or Large Audiences as affected stakeholders to support assessment of broad impact, regulatory exposure, and governance risk.|
    |Type of output produced: Automated Decisions|Classifies the AI system as producing Automated Decisions to support assessment of regulatory risk, human oversight requirements, and governance controls.|
    |Type of output produced: Generated Content|Classifies the AI system as producing Generated Content to support evaluation of transparency, misuse risk, and compliance requirements.|
    |Type of output produced: Insight &amp; Summaries|Classifies the AI system as producing Insights or Summaries to support assessment of decision-support risk and governance oversight.|
    |Type of output produced: Ranking &amp; Scores|Classifies the AI system as producing Rankings or Scores to support evaluation of fairness, bias risk, and governance requirements.|
    |Type of output produced: Recommendations|Classifies the AI system as producing Recommendations to support assessment of downstream impact, oversight needs, and compliance obligations.|
    |Type of output produced: Simple Alerts|Classifies the AI system as producing Simple Alerts to support evaluation of operational impact and governance relevance.|
    |Type of output produced: System Actions|Classifies the AI system as initiating System Actions to support assessment of automation risk, control requirements, and governance readiness.|

    These action types enable organizations to consistently associate governance requirements with AI systems based on how assessment questions are answered, helping ensure traceability between assessment outcomes and risk and compliance artifacts.

    Assessment templates provided as part of the base system include predefined control objectives and risk statements in the content library. However, the mapping logic that determines which governance elements are associated with an AI system is defined through post-assessment action configuration.

    **Note:** Content provided with the product is intended to support ease of use only. Your organization is responsible for ensuring compliance with applicable laws, regulations, directives, and standards, and for validating that any content used is accurate and up to date. Organizations may replace or adapt the provided content to align with their regulatory, governance, and operational requirements.

    Configuration is performed in the Assessment Workspace by editing the assessment template and defining automation rules that evaluate assessment responses. Each rule specifies which control objectives or risk statements should be associated when a particular response condition is met.

    After configuration, complete a test assessment and verify that the expected control objectives and risk statements are generated and mapped to the AI system once the assessment is marked as Closed complete.

    For more information on post-assessment automations and configurations, see [Post-assessment automations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/impact-automation.md) and [Configure post-assessment actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/configure-post-assessment-actions.md).

-   **Post-assessment action configuration example**

    The following example illustrates how a post-assessment action can be configured on an assessment template and applied after an assessment is completed.

    In the Assessment Workspace, an AI Risk and Compliance admin reviews a published AI impact assessment template and configures a post-assessment action that evaluates responses to a privacy-related question.

    -   **Condition**

        The automation rule evaluates the response to the assessment question "Does your AI system use personal data?"

    -   **Response**

        Yes.

    -   **Action**

        When the response is Yes, the post-assessment action automatically maps predefined governance elements to the associated AI system.

    Mapped control objectives:

    -   Ensure Data Quality
    -   Collect and Analyze Data
    -   Analyze Field Data
    Mapped risk statements:

    -   Operational Continuity and Downtime
    -   Unintended Consequences
    -   Reputational Damage
    -   Regulatory Non-compliance
    -   Privacy Violations
    -   Overfitting and Underfitting
    -   Model Poisoning
    -   Model Performance Degradation \(Model Drift\)
    -   Lack of Transparency and Accountability
    -   Lack of Transparency and Explainability
    -   Inadequate Data Protection
    -   Failure to Address Ethical Standards
    -   Data Security
    -   Data Bias
    -   Data Integrity
    -   Algorithmic Bias and Discrimination
    -   Data Breaches and Theft
    -   Adversarial Attacks
    -   Unauthorized Access to AI Models
    \[Omitted image "automation-rule-ex.png"\] Alt text: Risk statement mapping automation rule example

    When the assessment is submitted and marked as Closed complete, these mappings are evaluated and the corresponding risk and control records are automatically associated with the AI system.

    **Note:** Content provided with the product is intended to support ease of use only. Your organization is responsible for determining compliance with applicable laws, regulations, directives, and standards, and for validating that any content used is accurate and up to date. Organizations may replace or adapt the provided content to align with their regulatory, governance, and operational requirements.


## Assessment templates inventory

The following table lists assessment templates available for AI systems, AI models, and AI cases. Templates delivered with AI Risk and Compliance are provided in **Draft** state. To publish templates, see the note in the [Assessment workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/ai-risk-management/airc-assessment-templates.md) section.

|Name|Description|Applies to|Default state|When to use|
|----|-----------|----------|-------------|-----------|
|AI impact assessment|Evaluates the potential impact of an AI system on individuals, society, and the organization. Identifies risks related to privacy, non-discrimination, fairness, and other fundamental rights using a questionnaire-based approach. Responses automatically map to predefined risk statements and control objectives from the content pack through Post Assessment Actions. Review automatically generated risk statements and control objectives for usage and applicability in your organization. Role required: AI asset owner or AI risk and compliance business user \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_business\_user\].|AI systems|Draft|After AI use case submission, during the Assess phase.|
|AI impact assessment for EU AI Act conformity assessment|Evaluates whether an AI system may be subject to the EU Artificial Intelligence Act \(AI Act\). Focuses on risk classification, fundamental rights, safety, and transparency requirements. Assessment results determine whether additional governance activities are required, such as a full EU AI Act Conformity Assessment or a Fundamental Rights Impact Assessment \(FRIA\). Role required: AI asset owner or AI risk and compliance business user \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_business\_user\].|AI systems|Draft|When an AI system may be subject to the EU AI Act, especially when high-risk classification is possible.|
|EU AI Act Conformity Assessment|Provides a comprehensive evaluation of whether a high-risk AI system meets applicable EU AI Act requirements, including risk management, data governance, technical documentation, transparency, human oversight, accuracy, and robustness. Role required: AI risk and compliance analyst \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_analyst\] or AI risk and compliance manager \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_manager\].|AI systems|Draft|After initial EU AI Act assessment classifies the system as high risk, and before pre-deployment review.|
|Fundamental Rights Impact Assessment \(FRIA\)|Evaluates how a high-risk AI system may affect fundamental rights such as privacy, non-discrimination, freedom of expression, access to justice, and human dignity. Complete the FRIA before deployment to document and mitigate potential adverse effects. Role required: AI risk and compliance analyst \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_analyst\] or AI risk and compliance business user \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_business\_user\].|AI systems|Draft|After conformity assessment identifies potential fundamental rights implications and before deployment.|
|High-risk AI assessment questionnaire|Captures detailed information for AI systems flagged as potentially high risk, including design, data handling, decision-making, and potential harms. Results determine which governance controls, monitoring requirements, and review processes apply throughout the AI system's life cycle. Role required: AI asset owner or AI risk and compliance business user \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_business\_user\].|AI systems|Draft|When an AI system is flagged as potentially high risk during intake screening or impact assessment.|
|AI Impact Assessment on AI asset inventory|Evaluates risks associated with a specific AI model independent of its parent AI system. Supports model-level governance when a model is shared across systems or has a distinct risk profile. Role required: AI asset owner or AI risk and compliance analyst \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_analyst\].|AI models|Draft|When a model requires independent governance evaluation \(for example, shared model or distinct model risk factors\).|
|AI case assessment questionnaire|Provides a standardized evaluation framework for AI cases reported through the AI Risk and Compliance Workspace, Employee Center, or email. Supports consistent evaluation, case prioritization, and root cause analysis. Role required: AI case analyst \[sn\_ai\_case\_mgmt.ai\_case\_analyst\] or AI risk and compliance analyst \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_analyst\].|AI cases|Draft|During the investigation phase, after the case is triaged and assigned to an analyst.|

**Note:** AI case assessment templates are delivered as part of the AI Case Management application and aren't included in AI Risk and Compliance assessment templates.

