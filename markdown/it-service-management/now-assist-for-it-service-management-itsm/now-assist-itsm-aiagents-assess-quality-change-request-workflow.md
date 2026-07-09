---
title: IT Service Management AI agent collection assess quality of a change request agentic workflow
description: Use the assess quality of a change request agentic workflow to assess the quality of a change request and generate suggestions to improve the information in the fields. The workflow uses an active change policy document if one applies, or falls back to similar closed change requests.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm-aiagents-assess-quality-change-request-workflow.html
release: zurich
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 9
keywords: [Now Assist, agentic AI, generative AI, Gen AI]
breadcrumb: [Agentic AI in the Change Management application, Use agentic AI in IT Service Management, Now Assist for IT Service Management \(ITSM\), IT Service Management]
---

# IT Service Management AI agent collection assess quality of a change request agentic workflow

Use the assess quality of a change request agentic workflow to assess the quality of a change request and generate suggestions to improve the information in the fields. The workflow uses an active change policy document if one applies, or falls back to similar closed change requests.

## Change quality assessor AI agent overview

The change quality assessor AI agent analyzes the quality of a change request and suggests values for change request fields to improve it.

When the workflow runs, the agent first checks for an active change policy document using the **Get Change Quality Policy Document** tool:

-   **Policy document found**: The agent rates the change request using the policy document and suggests values only for the fields defined in it.
-   **No policy document found**: The agent falls back to similar closed change requests to assess the change request.

The agent assesses the following areas and assesses each one:

-   Short description
-   Description
-   Implementation plan
-   Backout plan
-   Test plan
-   Risk and impact analysis
-   Justification

The assessment report covers the overall change request and each area listed. It rates information as **Excellent**, **Very good**, **Good**, **Fair**, **Poor**, **Very poor**, or **Incomplete**. If all fields are rated **Excellent**, no suggestions are provided. The report is added to the **Work notes** field of the change request. You can also view the report in the `ai_change_quality_score` table.

**Note:** The assess quality of a change request agentic workflow has no trigger and must be run manually. To modify the workflow, duplicate it and adjust the settings to meet your requirements. To clone an agentic workflow that is available by default, you must run the semantic index for similarChangeRequests. The Business Rule \(\[Chg Quality\] Trigger semantic index\) does not run automatically for cloned workflows. Activate it manually or run the script in the business rule to confirm that the index runs. When you modify an agentic workflow, AI agent, or tool, update all instructions accordingly.

## Create a change policy document

A change policy document defines how the agent rates each field of a change request. Change policy documents are stored in the Change Policy Control table. If no active change policy document applies, the workflow falls back to the similar changes path.

To create a change policy document:

1.  Navigate to **All** and search for and open **Change Policy Control**.
2.  Select **New**.
3.  Enter a description and then set either the **Change model** field or the **Change type** field.
4.  Attach the policy document to the record.
5.  Select **Submit**.

When you save the record, the **Ingest policy document** business rule runs automatically. It calls to extract the policy criteria from the attached document, populates the **Policies** field with the results, and selects the **Active** check box.

\[Omitted image "Assess\_change\_quality\_using\_change\_policy\_control.png"\] Alt text: Change Policy Control form for Normal Type showing the Name, Active, Policies, and Change Type fields populated after ingesting a policy document.

Keep the following in mind when working with change policy documents:

-   To deactivate a policy, clear the Active check box.
-   Only one policy can be active for a scope at a time. Creating a new active policy automatically deactivates any existing active policy for that scope.
-   To activate an existing policy, first deactivate the currently active one for that scope.
-   To reuse a policy for another change request, select Copy Policy on an existing Change Policy Control record.

## Update custom fields using extraction prompts

**Important:** The extraction prompt for each field is defined in the `ChangeQualityUtilSNC` script. To support custom fields, override the prompt in the `ChangeQualityUtil` script instead.

`ChangeQualityUtilSNC` includes the following field entries for each out-of-box field: `justification`, `implementation_plan`, `backout_plan`, `test_plan`, and `risk_impact_analysis`. To add custom fields or change how the agent evaluates an existing field, override `POLICY_EXTRACTION_KEYS` in the `ChangeQualityUtil` script. Changes there are preserved across upgrades.

One entry is included as a starting point for customization:

-   **u\_custom\_field**

    A placeholder for a custom field. Copy it, set `name` to the element name of your field, and write a `description` that explains what the field should contain. Add one entry per custom field.


The following example shows a `ChangeQualityUtil` override with a `u_custom_field` entry:

```
POLICY_EXTRACTION_KEYS: [
    {
        "name": "justification",
        "description": "The business or technical reason explaining why the change is necessary. Look for references to a specific problem, incident, risk, compliance requirement, or performance goal. Should explain the consequence of not making the change. Examples: 'Resolving incident INC0012345 causing nightly job failures', 'Remediating CVE-2024-1234 on the authentication service', 'Meeting PCI-DSS audit requirement by 31 March deadline'."
    },
    {
        "name": "implementation_plan",
        "description": "The step-by-step sequence of actions required to execute the change. Look for numbered or ordered steps, each describing who does what, on which system, and when. Should reference specific scripts, config files, commands, or components. Examples: 'Step 1 - Prior to cutover, disable the scheduler service on app-server-01', 'Step 2 - Run migration script db_migrate_v4.sql on PROD-DB-02 during maintenance window', 'Step 3 - Restart the Orders API and confirm health check returns HTTP 200'."
    },
    {
        "name": "backout_plan",
        "description": "The specific steps to restore the previous state if the change fails or produces unacceptable results. Look for concrete rollback actions (not just 'revert the change'), trigger conditions that define when to initiate rollback, who is responsible, and whether rollback is feasible within the change window. Examples: 'If health check fails after Step 3, on-call engineer to restore previous WAR file from /backup/releases/v2.1.3 and restart service', 'Trigger: error rate exceeds 5% within 10 minutes of deployment — rollback owner: J. Smith (primary implementer)'."
    },
    {
        "name": "test_plan",
        "description": "The specific tests or checks performed after implementation to confirm the change succeeded and nothing unintended broke. Look for named test cases, expected outcomes, who performs the testing, which environment (production post-deployment required), and a clear pass/fail criterion. Examples: 'Post-deployment: verify login endpoint returns HTTP 200 using test account svc-smoketest@acme.com', 'Confirm nightly batch job completes without errors in PROD within 15 minutes of deployment — pass criterion: zero error entries in /var/log/batch/run.log'."
    },
    {
        "name": "risk_impact_analysis",
        "description": "An assessment of what could go wrong if the change fails, who or what would be affected, and how severely. Look for identified risks, affected users or services, likelihood/severity language, and blast radius estimates. Should be distinct from the implementation plan — focused on failure scenarios, not planned actions. Examples: 'Low probability but high impact — a failed schema migration could render the Orders API unavailable for up to 2 hours, affecting approximately 300 internal users', 'Risk of session timeouts during restart affecting users currently logged in, estimated 50 concurrent sessions'."
    },
    {
        "name": "u_custom_field",
        "description": "Explanation of what the custom field is"
    }
],
```

## Access the workflow

The workflow requires the `sn_itsm_aia.sn_aia_chg_quality` role. This role is included in the `itil` and `sn_change_write` roles.

To make the workflow available in the panel:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Open the **Assess quality of a change request** agentic workflow.
3.  In the left navigation, select **Select channels and status**.
4.  For **Engage via the Now Assist panel**, turn on the **Display** toggle.
5.  Select **Save and test**.

**Note:** Turning on the **Display** toggle is the only configuration required. The remaining configuration is available out of the box. Turning on this toggle also triggers a business rule that activates the text index the workflow requires for change requests.

## Assess a change request from the Now Assist panel

To assess a change request, open the change request and enter a prompt in the Now Assist panel, such as assess quality of &lt;change request number&gt;. You can enter the change request number from the list of suggestions, add keywords, or type a custom prompt.

\[Omitted image "Assess\_change\_request\_using\_AI.png"\] Alt text: Now Assist panel showing a prompt to assess the quality of a change request and the resulting quality assessment with field ratings and suggested improvements.

The agent returns a quality assessment in the panel. The assessment includes:

-   An overall quality rating, for example, **Very Good**.
-   A summary of the assessed fields with a justification for each rating.
-   Suggested improvements for fields that are not rated **Excellent**.

The agent asks for confirmation before updating any field. When you confirm a suggested value, the agent updates the field, saves the change request, and marks the update as **AI Generated**. The agent then asks whether to record the quality summary. If you confirm, the summary is added to **Work notes** and a record is created in the **AI Change Quality Scores** table.

For more information, see [Request the generative AI capabilities in ITSM by using the Now Assist panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/now-assist-for-it-service-management-itsm/request-gen-ai-capabilities-itsm-now-assist-panel.md).

## Change quality scores

The workflow records the quality summary in the **AI Change Quality Scores** \[`ai_change_quality_score`\] table. Each record stores the overall score, the rating, the explanation, and the per-field scores for the change request. When a change policy document is used to rate the change request, the record also stores a reference to the Change Policy Control record. This allows change management teams to track how scores trend over time as a policy document changes.

To view the recorded scores, search for **AI Change Quality Scores**. The table includes the following information:

|Field|Description|
|-----|-----------|
|Change Policy Control|The change policy document used to rate the change request. This field is empty when the change request is rated through the similar changes path.|
|Change Request|The change request that was rated.|
|Explanation|The natural language explanation of the overall score.|
|Rating|The overall quality rating, for example, Very Good.|
|Score|The overall numeric score, from 0 through 100.|
|Per field score|The per field rating values for the assessed fields.|

If a record already exists for a change request, the workflow overwrites it with the latest assessment.

## Visualize change quality scores

Use Platform Analytics to track trends in the `ai_change_quality_score` table. A line chart of average score by month shows whether change quality is improving or declining.

Hover over a point to see the score for that month. Select **Go to record list** to open the records behind that data point.

Use **Group by** to break the trend down by a change request dimension, such as **Assignment group**, **Model**, or **Change Model Template**. This lets you compare change quality across teams or change types.

\[Omitted image "Assess\_change\_quality\_using\_visual\_change\_quality\_score\_grouping.png"\] Alt text: Line chart showing average change quality scores grouped by a change request dimension, such as assignment group or change model.

When the chart is grouped, hover over a point to see the score and percentage for each group. Select **Go to record list** to view the change requests behind any value.

Select **Add to Dashboard** to pin the report to a dashboard for ongoing monitoring.

