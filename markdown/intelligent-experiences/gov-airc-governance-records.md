---
title: Governance record types
description: Record types under the Governance section of an AI asset's Risk &amp; Compliance tab in AI Control Tower, used to support governance review.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/gov-airc-governance-records.html
release: australia
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [reference, governance]
breadcrumb: [Reference, Managing risk and compliance, Govern AI assets, AI Control Tower, Enable AI experiences]
---

# Governance record types

Record types under the Governance section of an AI asset's Risk &amp; Compliance tab in AI Control Tower, used to support governance review.

The Governance section of an AI asset organizes related governance records into four categories: Assessments, Governance, Tasks, and Tracking.

|Category|Record type|Description|
|--------|-----------|-----------|
|Assessments|AI assessments|General assessments that evaluate an AI asset against governance criteria, such as intended use, risk classification, and compliance requirements. Risk assessments and regulatory risk assessments \(below\) are the specific assessment types that feed the asset's [regulatory risk classification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/gov-airc-regulatory-classification.md) and [aggregated risk rating](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/gov-airc-risk-score-calculation.md).|
|Assessments|Risk assessments|Assessments that identify and rate the risks associated with an AI asset, including inherent risk and the effectiveness of the controls applied to it. Results contribute to the asset's [aggregated risk rating](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/gov-airc-risk-score-calculation.md) and [risk heat map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/gov-airc-risk-posture.md) placement.|
|Assessments|Regulatory risk assessments|Assessments that determine how an AI asset is classified against regulatory frameworks and requirements, such as unacceptable, high, medium, or low risk. Results populate the asset's [regulatory risk classification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/gov-airc-regulatory-classification.md).|
|Assessments|Bulk risk assessments|A grouping of risk assessments run across multiple AI assets at once, used to assess several assets against the same criteria in a single pass instead of individually. For more information, see [Risk assessment project in AI Risk and Compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/risk-assessment-project-airc.md).|
|Governance|Risks|Individual risk records identified for the AI asset, each describing a potential issue along with its inherent risk level. Risks are the basis for the asset's risk heat map and aggregated risk rating.|
|Governance|Controls|Control records that describe the safeguards applied to mitigate the risks identified for the AI asset. The status and weight recorded on each control determine its control effectiveness score, which directly affects the asset's residual risk.|
|Tasks|Attestations|Records that capture confirmation that a control is in place and operating as expected, tied to a specific compliance framework or policy. Attestation state, such as Complete or Ready to take, feeds the asset's [compliance score](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/gov-airc-compliance-score-calculation.md) and compliance posture for priority frameworks.|
|Tracking|Issues|Records that track a compliance or control gap identified for the AI asset that requires remediation. Open issues surface as high-priority items in the asset's compliance posture and top action items.|
|Tracking|Policy exceptions|Records that document an approved deviation from a policy or control requirement for the AI asset, including justification and expiration. Policy exceptions provide an audit trail for accepted risk.|

