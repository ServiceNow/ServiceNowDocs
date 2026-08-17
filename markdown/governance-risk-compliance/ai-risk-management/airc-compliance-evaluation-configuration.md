---
title: Create a compliance evaluation configuration
description: Create a compliance evaluation configuration that defines which AI systems, control objectives, metrics, and schedule a compliance evaluation applies to.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/ai-risk-management/airc-compliance-evaluation-configuration.html
release: zurich
product: AI Risk Management
classification: ai-risk-management
topic_type: task
last_updated: "2026-07-25"
reading_time_minutes: 3
breadcrumb: [Configure, AI Risk and Compliance, Governance, Risk, and Compliance]
---

# Create a compliance evaluation configuration

Create a compliance evaluation configuration that defines which AI systems, control objectives, metrics, and schedule a compliance evaluation applies to.

## Before you begin

Role required: sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_manager

## About this task

A compliance evaluation configuration monitors AI systems for compliance and updates evaluation scores on an ongoing basis. Use evaluation frameworks from ServiceNow and Traceloop to produce trace, session, or span records for your AI systems. These frameworks help you derive a comprehensive evaluation of your AI systems.

## Procedure

1.  Navigate to **All** &gt; **AI Risk and Compliance** &gt; **AI Risk and Compliance Workspace**.

2.  Select the list icon \[Omitted image "list-icon-airc-ws.png"\] Alt text:.

3.  From the **Controls monitoring** module, select the **Compliance evaluation configurations** and select **New**.

4.  Define the evaluation details and data scope details.

<table id="table_p4b_cwk_bkc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

**Basic details**

</td></tr><tr><td>

Evaluation name

</td><td>

A unique, descriptive name for this evaluation, using specific terms that identify the AI system, assessment scope, or version being evaluated \(for example, *Monitoring AI Toxicity*\).

</td></tr><tr><td>

Description

</td><td>

The purpose and scope of this evaluation, including what is being assessed, why it matters, and any key constraints or context users should know.

</td></tr><tr><td class="sub-head" colspan="2">

**Data scope details**

</td></tr><tr><td>

Authority documents

</td><td>

The authority documents that govern this evaluation. The following options are provided: -   **NIST AI Risk Management Framework**
-   **EU Artificial Intelligence Act**
-   **AI Content Safety &amp; Toxicity Standard**


</td></tr><tr><td>

Policies

</td><td>

The policies that this evaluation aligns with or enforces. The following options are provided: -   **Artificial Intelligence Software Development Lifecycle Policy**
-   **Enterprise Artificial Intelligence Governance Policy**
-   **Internal use of AI Systems**


</td></tr><tr><td>

AI system type

</td><td>

The category of AI system being evaluated. The following options are provided:-   **Agentic AI**
-   **Generative AI**


</td></tr><tr><td>

Provider

</td><td>

The provider. The following options are provided:-   **ServiceNow**
-   **Others**


</td></tr><tr><td>

Metric category

</td><td>

The metric category used in this evaluation:-   **Safety**
-   **Security**
-   **Quality**


</td></tr></tbody>
</table>    \[Omitted image "airc-configure-evaluation-define.png"\] Alt text: Form showing compliance evaluation configuration with fields for evaluation details and data scope. The fields shown include options for selecting authority documents, policies, AI system type, and metric category.

5.  Select **Next**.

6.  Select **Add control objectives** to add control objectives to the scope.

7.  Map control objectives from the filtered list by selecting the check box of each desired control objective.

8.  Select **Add** to complete the control objective mapping, and then select **Next**.

    \[Omitted image "airc-configure-evaluation-scope-control-obj.png"\] Alt text: Form showing a table of compliance control objectives with checkboxes to select controls for evaluation scope.

9.  Define the evaluation criteria and frequency in the **Evaluation criteria and frequency** section.

<table id="table_kx1_2dj_bkc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Frequency

</td><td>

The frequency at which evaluations are conducted. The following options are provided:-   Daily
-   Weekly
-   Monthly
 For example, for AI toxicity, a monthly evaluation monitors control drift.

</td></tr><tr><td>

Success condition result

</td><td>

The result, Passed or Failed, assigned to an AI system when the evaluation criteria is met.

</td></tr></tbody>
</table>10. In the **All Evaluations** section, define the conditions and the metrics under which the configuration is applicable.

    If multiple conditions are specified, they are evaluated in the order listed to determine applicability.

<table id="table_tt5_cdj_bkc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

A name for the evaluation.

</td></tr><tr><td>

Conditions

</td><td>

The field, operator, and value that filter which records this configuration applies to, for example, \[Risk classification\] \[is\] \[High\]. Select "and" or "or" to combine multiple conditions, and select **New condition set** to add a condition set that is evaluated independently of other condition sets.

</td></tr><tr><td class="sub-head" colspan="2">

**Metric thresholds**

</td></tr><tr><td>

Metric

</td><td>

The metric, operator, and threshold value that determine when a control is evaluated as compliant or non-compliant, for example, \[Toxicity\] \[is\] \[True\]. Select **Add metric** to define additional metric thresholds for this configuration.

</td></tr></tbody>
</table>    \[Omitted image "airc-configure-evaluation.png"\] Alt text: Compliance evaluation configuration form showing the final step of the Configuring evaluation. The form displays evaluation conditions and metric thresholds.

11. Select **Submit**.


## What to do next

The compliance evaluation configuration is ready to be mapped to one or more AI systems. For information on mapping an evaluation configuration to AI systems, see [Use a compliance evaluation on an AI system record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/ai-risk-management/airc-use-compliance-evaluation-ai-system.md).

