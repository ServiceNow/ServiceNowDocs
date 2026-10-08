---
title: Customize classification and scoring formulas
description: Change the factors, weights, rating bands, and rollup formula that determine how classification, risk, and compliance scores are calculated.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/gov-airc-customize-crc-formulas.html
release: brazil
topic_type: task
last_updated: "2026-10-05"
reading_time_minutes: 4
keywords: [risk assessment methodology, scoring formula, rating criteria, rollup configurations, compliance score]
breadcrumb: [Configure, Managing risk and compliance, Govern AI assets, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Customize classification and scoring formulas

Change the factors, weights, rating bands, and rollup formula that determine how classification, risk, and compliance scores are calculated.

## Before you begin

The current factors, weights, and rating bands must be reviewed before a formula is changed. For the current values, see [Regulatory risk classification reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-airc-ref-regulatory-classification.md) and [AI risk score calculation reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-airc-ref-risk-score-calculation.md).

Role required: sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_admin

## About this task

Changing a scoring formula affects every AI asset that uses the risk assessment methodology \(RAM\) or governance pipeline you edit, both for new assessments and for existing scores after they next recalculate.

**Warning:**

Changing factor weights, point values, or rating bands on a predefined RAM changes how every AI asset using that RAM is scored. Consider creating and testing a custom RAM instead of editing a predefined one. Automated Scripted Factors contain script logic, not simple field values, so changing their point thresholds requires editing and testing a script, not just a form field.

## Procedure

-   To customize the regulatory classification or risk score formula, do the following:

    1.  Navigate to **All** &gt; **AI Risk and Compliance** &gt; **Risk Assessments** &gt; **Risk assessment methodologies** and open the RAM that you need to change.

        Consider copying the RAM or creating a custom RAM rather than editing a predefined one, so that other AI assets aren't affected while you test your changes.

    2.  For a risk-based RAM, edit the Rollup configurations section on the RAM form to change the rollup formula for the qualitative and quantitative scores.

        Entity-hierarchy rollups can use Sum, Average, Maximum, or Minimum.

    3.  To change factor weights or point values, navigate to **All** &gt; **AI Risk and Compliance** &gt; **Risk Assessments**, then select **Group Factors**, **Manual Factors**, **Automated Factors**, or **Automated Scripted Factors**, depending on the factor type the RAM uses.

        For the current factor names, fields, and point values for the predefined RAMs, see [Regulatory risk classification reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-airc-ref-regulatory-classification.md) and [AI risk score calculation reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-airc-ref-risk-score-calculation.md).

    4.  To change rating band thresholds or labels, navigate to **All** &gt; **AI Risk and Compliance** &gt; **Risk Assessments** &gt; **Risk Criteria**.

-   To customize the compliance score formula, do the following:

    1.  Navigate to **All** &gt; **AI Risk and Compliance** &gt; **Policy &amp; Compliance Administration** &gt; **Properties**.

    2.  Set **Use weighted control average when calculating compliance scores** \(**sn\_compliance.cal\_score\_by\_weighted\_control**\) to **Yes** to weight controls when averaging a citation's compliance score instead of using a flat average.

        For the weighted and flat average calculations, see [Compliance score calculation for a citation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/compliance-score-calculation-for-a-citation.md).

        **Note:**

        This setting changes citation-level compliance scores only. These scores determine the compliance posture shown for authority documents and policies on the Compliance score card. It doesn't change the AI system's own compliance score, which is calculated separately from linked entities. For that formula, see [AI system compliance score calculation reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-airc-ref-compliance-score.md).

    3.  Set **Enable association of citations to controls mapping** \(**sn\_compliance.enable\_association\_of\_citations\_to\_controls**\) to **Yes** to calculate a citation's compliance score from its directly linked controls instead of its associated control objectives.

        For the control-objective-based and directly-linked-controls formulas, see [Compliance score calculation for a citation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/compliance-score-calculation-for-a-citation.md).

    4.  Set **Entity hierarchy based scoring** \(**sn\_compliance.entity\_hierarchy\_based\_scoring**\) to **Yes** to calculate the compliance score of an entity from its downstream entities and its direct controls.

        When the property is set to **No**, which is the default, the compliance score of an entity comes from its direct controls only. When the property is set to **Yes**, the score of an entity is based on the average compliance score of its downstream entities and the average compliance score of its direct controls.

    5.  If you changed the **Entity hierarchy based scoring** property, navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs** and deactivate the **Compliance Score V2** scheduled job.

    6.  Open the **Update compliance scores for hierarchy entities** scheduled job and select **Execute Now**.

        The job recalculates the compliance scores of all entities with the current value of the property. If the job isn't run after the property changes, the compliance scores of entities can be inconsistent.

    7.  After the job completes, activate the **Compliance Score V2** scheduled job again.


## Result

New assessments use the updated formula. Existing scores update the next time the affected assessments or rollups recalculate.

If the compliance scores of entities are inconsistent after the **Entity hierarchy based scoring** property is changed, the **Update compliance scores for hierarchy entities** scheduled job might not have run. Run the job, and then activate the **Compliance Score V2** scheduled job again.

**Related topics**  


[Configure classification, risk score, and compliance score](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-airc-configure-crc-scores.md)

[Regulatory risk classification reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-airc-ref-regulatory-classification.md)

[AI risk score calculation reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-airc-ref-risk-score-calculation.md)

[AI system compliance score calculation reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-airc-ref-compliance-score.md)

