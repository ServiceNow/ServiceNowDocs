---
title: Configure RTO and RPO Smart Assessment templates workflow
description: Configure Recovery Time Objective \(RTO\) and Recovery Point Objective \(RPO\) assessments using the Smart Assessment Engine for Business Impact Analysis \(BIA\). The Smart Assessment Engine replaces the traditional non-smart assessment questionnaires with an automated, rule-based approach.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/configure-rto-rpo-sa-templates.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Setup for a BIA, Configure, Business Continuity Management, Governance, Risk, and Compliance]
---

# Configure RTO and RPO Smart Assessment templates workflow

Configure Recovery Time Objective \(RTO\) and Recovery Point Objective \(RPO\) assessments using the Smart Assessment Engine for Business Impact Analysis \(BIA\). The Smart Assessment Engine replaces the traditional non-smart assessment questionnaires with an automated, rule-based approach.

## Before you begin

Role required: sn\_bcm.admin

## About this task

Prerequisites

|Applications|Names|App id|
|------------|-----|------|
|Required applications|Smart Assessment Designer \(sn-smart-assessment-designer\) - Core designer functionality|\(sn\_smart\_asmt\_desg\)|
|Connected component for Smart Assessment instance \(sn-amrt-assessment-connected\) - Base components|\(sn\_smart\_asmt-conn\)|
|Smart Assessment Impact Automation \(Post Assessment Actions for Smart Assessments\) - Enables automation tab and RTO and RPO calculations|\(sn\_smart\_imp\_auto\)|
|Smart Assessment Core - Foundation application|\(sn\_smart\_asmt\)|
|Optional applications|Basic Scoring for Smart Assessment \(Enable scoring for Smart Assessments\)|\(sn\_smart\_scoring\)|
|Smart Assessment Advanced Response Automation - \(Set up automatic responses for assessment questions based on specific conditions\)|\(sn\_smart\_resp\_auto\)|
|Smart Assessment for Mobile - \(Reusable application offers common mobile functionalities for Smart Assessment\)|\(sn\_smart\_asmt\_mob\)|
|Now Assist for Smart Assessment - \(AI-powered assistance\)|\(sn\_smart\_ai\_assist\)|

The **Automations** tab only appears when the Impact Automation \(Post Assessment Actions for Smart Assessments, sn\_smart\_imp\_auto\) app is installed. Similarly, the **Scoring** tab requires the Scoring \(sn\_smart\_scoring\) app.

## Procedure

1.  Navigate to **All** &gt; **Business Continuity** &gt; **Business Impact Analysis** &gt; **Smart Assessment template Categories**.

    Assessment template categories determine which templates can be selected in BIA templates.

    \[Omitted image "bia-sa-temp-categories.png"\] Alt text: Categories.

    1.  Verify that the out-of-the-box category is configured as "Business impact assessment."

        This category has the following configuration: Template category role: sn\_bcm.core\_viewer and Active: true.

        \[Omitted image "bia-sa-temp-categories-imp-asmt.png"\] Alt text: Business impact assessment category.

        **Note:** Only templates assigned to the “Business impact assessment” category are displayed in the **Impact assessment templates** field when configuring a BIA template.

        \[Omitted image "bia-sa-temp-categories-rpo-rto-templates.png"\] Alt text: Impact assessment templates field.

        **Note:** The **Business impact assessment** template category also controls how the Smart Assessment Engine handles open BIA assessments when an impact assessment template is re-versioned. Set **Assessment handling on version retirement** to **Retain** to let in-progress BIAs complete on the retired version, or to **Cancel** to force in-progress BIAs to a canceled state so all active BIAs use the latest version. For more information, see [Using latest assessment template for conducting BIAs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/using-smart-asmt-template.md).

2.  Select **New template** in the Assessment Workspace or open an existing template.

    When you select **New template**, the Create assessment template form is displayed.

    1.  To configure the **General** tab, fill in the fields in the Create assessment template form and select **Create**.

        |Field|Description|
        |-----|-----------|
        |Template name|Unique and descriptive name for the template, for example, "BIA RTO/RPO” or “Recovery point objective assessment template."|
        |Assessment name|Name for the assessment used to conduct the BIA.|
        |Description|Details about the template’s purpose. For example, Regulatory reporting assessment of IT incidents.|
        |Purpose|Purpose or intended use of the template. This is a critical step. To enable selection in BIA templates, select **Business impact assessment**.|
        |Assessment target|Table records that are used for the assessment. Select **Impact analysis** so that the template assesses the impact analysis records.|
        |Settings|
        |Duration \(number of days\)|Assessment duration to be specified as needed.|
        |Assessment reader role|Role set to \(sn\_bcm.core\_viewer\).|

        \[Omitted image "bia-asmt-ws-general-tab-settings.png"\] Alt text: General tab settings.

        For more information on creating templates, see [Create an assessment template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/sae-asmnt-template-create.md).

    2.  To save your changes, select **Save**.

        The General settings are saved.

3.  Set up the assessment questions in the **Questions** tab.

    Questions gather the information needed to calculate RTO and RPO values automatically.

    \[Omitted image "bia-asmt-ws-questions-tab-2.png"\] Alt text: Data change frequency.\[Omitted image "bia-asmt-ws-questions-tab.png"\] Alt text: Data value.

    The following steps show examples for Data change frequency and Data value questions.

    1.  Select **Add section** in the **Questions** tab.

    2.  Name the section.

        According to your requirements, you can add a section name such as Data change frequency.

    3.  Add a question and its description.

        The table shows sample questions text for Section 1: Data change frequency.

        |Sample question|Sample answer|
        |---------------|-------------|
        |Section 1: Data change frequency|
        |Question text|What is the data change frequency?|
        |Question type|Dropdown|
        |Selection type|Single select|
        |Required|Yes|
        |Choices|Low, Medium, High|
        |Question description|Mention the frequency at which the data in the asset is updated.|

        The table shows sample questions text for Section 2: Data value.

        |Sample question|Sample answer|
        |---------------|-------------|
        |Section 2: Data value|
        |Question text|What is the value of data?|
        |Question type|Dropdown|
        |Selection type|Single select|
        |Required|Yes|
        |Choices|Low, Medium, High|
        |Question description|Mention the value of data stored in the asset.|

    4.  Select the **Publish** button and verify that the template status changes to Published.

        **Note:** The Create automation option only appears after publishing the template.

        **Note:** Starting with GRC: Business Continuity Management - Core, version 11.0.1, Smart Assessment templates support version control, and version details are displayed on each template.

4.  Create automation rules in the **Automations** tab.

    Automations define the rules that automatically calculate RTO and RPO based on the question responses.

    \[Omitted image "bia-asmt-ws-automations-tab-2-set-condi.png"\] Alt text: Conditions.

    The following steps show examples with conditions and actions.

    1.  Select **Create automation** in the **Automations** tab.

    2.  Select or create an automation.

        According to your requirements, you can add an automation such as Recovery point objective as shown in the example.

        \[Omitted image "bia-asmt-ws-automations-tab.png"\] Alt text: Automations.

        The table shows sample conditions and actions for Action set 1 and "High" data change frequency. Each automation consists of action sets with If-Then logic.

        \[Omitted image "bia-asmt-ws-automations-tab-2-set-condi-high.png"\] Alt text: High frequency.\[Omitted image "bia-asmt-ws-automations-tab-2-set-actions-high-imme.png"\] Alt text: Actions for high frequency.

<table id="table_j14_ddr_23c"><thead><tr><th>

Sample condition

</th><th>

Sample action

</th></tr></thead><tbody><tr><td colspan="2">

Action set 1: High data change frequency + High data value

</td></tr><tr><td>

If

</td><td>

Response based &gt; Section: Data change frequency &gt; What is the data change frequency? **is** High

 **and**

 Response based &gt; Section: Data value &gt; What is the value of data? **is** High

</td></tr><tr><td>

Then

</td><td>

Set recovery point objective: **Immediately**

 Impact analysis: Scope based &gt; Impact analysis

</td></tr></tbody>
</table>        The table shows sample conditions and actions for Action set 2 and "Medium" data change frequency. Each automation consists of action sets with If-Then logic.

        \[Omitted image "bia-asmt-ws-automations-tab-2-set-condi-medium.png"\] Alt text: Medium frequency.\[Omitted image "bia-asmt-ws-automations-tab-2-set-actions-medium-24hrs.png"\] Alt text: Actions for medium frequency.

<table id="table_yrj_g2r_23c"><thead><tr><th>

Sample condition

</th><th>

Sample action

</th></tr></thead><tbody><tr><td colspan="2">

Action set 2: Medium data change frequency + High data value

</td></tr><tr><td>

If

</td><td>

Response based &gt; Section: Data change frequency &gt; What is the data change frequency? **is**Medium

 **and**

 Response based &gt; Section: Data value &gt; What is the value of data? **is** Medium

</td></tr><tr><td>

Then

</td><td>

Set recovery point objective: **24 Hours**

 Impact analysis: Scope based &gt; Impact analysis

</td></tr></tbody>
</table>        The table shows sample conditions and actions for Action set 3 and "Low" data change frequency. Each automation consists of action sets with If-Then logic.

        \[Omitted image "bia-asmt-ws-automations-tab-2-set-condi-low.png"\] Alt text: Low frequency.\[Omitted image "bia-asmt-ws-automations-tab-2-set-actions-low-one-week.png"\] Alt text: Actions for low frequency.

<table id="table_c4c_m2r_23c"><thead><tr><th>

Sample condition

</th><th>

Sample action

</th></tr></thead><tbody><tr><td colspan="2">

Action set 2: Medium data change frequency + High data value

</td></tr><tr><td>

If

</td><td>

Response based &gt; Section: Data change frequency &gt; What is the data change frequency? **is**Low

 **and**

 Response based &gt; Section: Data value &gt; What is the value of data? **is** Low

</td></tr><tr><td>

Then

</td><td>

Set recovery point objective: **1 week**

 Impact analysis: Scope based &gt; Impact analysis

</td></tr></tbody>
</table>        Conditions use Response based filtering to check question answers. Multiple conditions can be combined with and/or operators. The "Else" clause provides a fallback action if none of the conditions match. Each action set can have multiple conditions and actions.

    3.  To enable automation, select **Activate** after configuring all action sets and verify that the automation status shows as “Active.”

        **Note:** Automations only run when they’re activated. Deactivated automations don’t set RTO and RPO values.

    4.  Review and publish Post Assessment Actions after publishing a new template version.

        A new version is required when a change affects question meaning, scoring, or structure. When a new version is published, the Smart Assessment Engine automatically copies the existing Post Assessment Actions to the new version in the **Draft** state.

        Draft Post Assessment Actions do not run until published — BIAs triggered from the new version do not update RTO, RPO, MTPD, or Recovery Tier fields until you publish the Post Assessment Actions.

        BIAs triggered from the retired version continue to use that version's Post Assessment Actions.

5.  Verify the Action type subflows in the Workflow Studio.

    Action types are implemented as Flow Designer subflows. Each subflow:

    -   Receives inputs from the automation:
        -   Recovery timeframe - The value to set \(for example, “Immediately”, “24 hours”, “1 week”\)
        -   Impact analysis - The scope-based impact analysis record being assessed
    -   Updates the corresponding field on the impact analysis record:
        -   Recovery point objective field
        -   Recovery time objective field
        -   MTPD field
    You can create custom action types by performing the following steps:

    1.  Creating a Flow Designer subflow.
    2.  Defining required input parameters.
    3.  Adding logic to update impact analysis fields.
    4.  Registering the subflow as an action type.
    5.  Selecting the custom action type in the automation configuration.
    A use case example: A single questionnaire can update RTO, RPO, and MTPD simultaneously, or you can create separate assessments for each metric depending on your organization’s requirements.

    1.  Search for the Set recovery point objective action type subflow in the Workflow Studio.

        \[Omitted image "bia-subflow-set-rpo.png"\] Alt text: Subflow.

    2.  Verify that the Recovery timeframe and Impact analysis are selected as the subflow inputs.

        \[Omitted image "bia-subflow-set-rpo-update.png"\] Alt text: Inputs.

    3.  Review the update action that sets the field value.

        \[Omitted image "bia-subflow-set-rpo-update-2.png"\] Alt text: Action inputs.

6.  Link the assessment templates to the BIA templates.

    1.  Access **BIA templates** in the Business Continuity Workspace.

    2.  Open your BIA template.

        The example shows the BIA RTO/RPO template.

    3.  Configure the template.

        The example shows a BIA template and its parameters.

        \[Omitted image "bia-templates-example.png"\] Alt text: Example.

        -   Name: BIA RTO/RPO
        -   Primary element assessed: Datacenters
        -   Assessment type: Smart assessment
        -   Impact assessment templates: Select “Recovery time objective assessment template”, select “Recovery point objective assessment template."
        \[Omitted image "bia-templates-imp-asmt-templates.png"\] Alt text: Templates.

    4.  Select **Update**.

        Verify that automations are activated in the selected assessment templates. Inactive automations do not calculate RTO/RPO values.

7.  To create a BIA, select **New** in the Business Continuity Workspace.

    For more information, see [Create a business impact analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-bia-in-uib-ws.md).

8.  Complete the BIA configuration and save the BIA.

    -   **Assessment generation**

        When you create a BIA using the configured template, assessment records are automatically created:

        1.  Assessments appear in Assessment Workspace &gt; Lists &gt; Business Impact Analysis &gt; In draft.
        2.  Each assessment contains the questions defined in the template.
    -   **Completion of assessments**

        You can complete assessments by performing the following tasks:

        1.  Open the assessment.
        2.  Answer all required questions \(for example, data change frequency, data value\)
        3.  Submit the assessment.
    -   **Automatic RTO and RPO calculation after submission**

        After submission, the system calculates the RTO and RPO:

        1.  Automation rules evaluate the question responses.
        2.  Matching conditions trigger the corresponding actions.
        3.  RTO and RPO fields are automatically populated on the impact analysis record.
        4.  Values appear in the Business Impact Analysis record.

**Parent Topic:**[Setup for a business impact analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/bcm-admin-tasks.md)

