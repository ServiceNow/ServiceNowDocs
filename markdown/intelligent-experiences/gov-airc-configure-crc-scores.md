---
title: Configure classification, risk score, and compliance score
description: Configure the applications, properties, and data that the classification, risk score, and compliance score depend on for an AI asset.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/gov-airc-configure-crc-scores.html
release: brazil
topic_type: task
last_updated: "2026-10-05"
reading_time_minutes: 4
keywords: [regulatory risk classification, aggregated risk score, compliance score, primary RAM, Migrate to Advanced Risk Assessments]
breadcrumb: [Configure, Managing risk and compliance, Govern AI assets, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Configure classification, risk score, and compliance score

Configure the applications, properties, and data that the classification, risk score, and compliance score depend on for an AI asset.

## Before you begin

Role required: sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_admin, admin

## About this task

You don't configure these three metrics in the Risk and Compliance views. The views only display the results of the configuration described in this topic.

## Procedure

-   To configure regulatory risk classification, do the following:

    1.  Navigate to **All** &gt; **AI Risk and Compliance** &gt; **Risk Assessments** &gt; **Risk assessment methodologies**, then publish the risk assessment methodology \(RAM\) that you need to use for automated classification, or publish a custom RAM.

        RAMs ship in the Draft state and can't classify assets until published.

    2.  Navigate to **All** &gt; **AI Risk and Compliance** &gt; **General Administration** &gt; **Properties**.

    3.  Set the **sn\_grc\_ai\_gov.ai\_system\_automated\_risk\_classification\_asmt\_ram** property to the published RAM.

        For more information, see [Set up AI Risk and Compliance properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/configure-airc-properties.md).

    4.  Confirm the Use and purpose record is linked to the governance details record of each AI asset.

        This link is created automatically during intake. If a condition isn't met, the classification remains To be determined. For the full set of conditions, see [Classifying AI assets by regulatory risk](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-airc-regulatory-classification.md).

-   To configure the aggregated risk score \(inherent, control effectiveness\), do the following:

    1.  Install the Advanced Risk application.

        Skip this step if you're using AI Control Tower — it includes this application.

    2.  Navigate to **All** &gt; **Advanced Risk assessment** &gt; **Administration** &gt; **Properties**.

    3.  Set the **Migrate to Advanced Risk Assessments** property to **Yes**.

        This is a one-way configuration change. Until this property is set to **Yes**, risk score rollup isn't supported and no aggregated risk score appears. For what changes after you enable it, see [Set up Advanced Risk assessments properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/advanced-risk-assessments-properties-airc.md).

    4.  Navigate to **All** &gt; **AI Risk and Compliance** &gt; **Risk Assessments** &gt; **Risk assessment methodologies**, then publish the **Risk assessment for AI inventory** RAM, or a custom risk-based RAM that assesses risks and belongs to the AI risk and compliance domain.

    5.  Set a primary RAM directly on each AI system record, or navigate to **All** &gt; **AI Risk and Compliance** &gt; **General Administration** &gt; **Properties** and set a portfolio-wide default in the **sn\_grc\_ai\_gov.aisystem\_primary\_ram** property.

        An AI system without a primary RAM doesn't show rollup scores. For the full requirements and default-selection order, see [AI risk score calculation reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-airc-ref-risk-score-calculation.md).

-   To configure the compliance score, do the following:

    1.  Open the AI system record and map every relevant entity in the Related Entities related list.

        An entity that isn't mapped doesn't affect the score, so a missing entity can make the score look better or worse than the real compliance posture.

    2.  Navigate to **All** &gt; **AI Risk and Compliance** &gt; **General Administration** &gt; **Properties**.

    3.  Set the **sn\_grc\_ai\_gov.highlighted\_authority\_document** and **sn\_grc\_ai\_gov.highlighted\_policy** properties to choose up to two authority documents and two policies to show as priority frameworks on the Compliance score card.

        For more information, see [Set up AI Risk and Compliance properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/configure-airc-properties.md).


## Result

Regulatory risk classification, aggregated risk score, and compliance score are available on the AI asset record and in the Risk and Compliance views in AI Control Tower and the AI Risk and Compliance Workspace. To view them, see [View classification, risk, and compliance scores](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-airc-view-classification-risk-compliance-scores.md).

If the Risk and Compliance dashboards on the AI asset record page or the landing page show a `No data found` error, see [Risk score and compliance score dashboard errors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-airc-ref-troubleshooting.md).

**Related topics**  


[Classifying AI assets by regulatory risk](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-airc-regulatory-classification.md)

[Risk rating calculation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-airc-risk-score-calculation.md)

[Compliance score calculation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-airc-compliance-score-calculation.md)

[View classification, risk, and compliance scores](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-airc-view-classification-risk-compliance-scores.md)

[Customize classification and scoring formulas](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-airc-customize-crc-formulas.md)

[Configuring AI Risk and Compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/configuring-ai-risk-and-compliance.md)

