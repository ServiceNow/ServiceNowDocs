---
title: Governance record types
description: Record types under the Governance section of an AI asset's Risk &amp; Compliance tab in AI Control Tower, used to support governance review.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/gov-airc-governance-records.html
release: australia
topic_type: concept
last_updated: "2026-07-21"
reading_time_minutes: 1
keywords: [reference, governance]
breadcrumb: [Reference, Managing risk and compliance, Govern AI assets, AI Control Tower, Enable AI experiences]
---

# Governance record types

Record types under the Governance section of an AI asset's Risk &amp; Compliance tab in AI Control Tower, used to support governance review.

The Governance section of an AI asset organizes related governance records into four categories: Assessments, Governance, Tasks, and Tracking.

|Category|Record type|Description|
|--------|-----------|-----------|
|Assessments|AI assessments|Assessments that evaluate an AI asset against governance criteria, such as intended use, risk classification, and compliance requirements. Results feed the asset's regulatory risk classification and aggregated risk rating.|
|Assessments|Risk assessments|Assessments that identify and rate the risks associated with an AI asset, including inherent risk and the effectiveness of the controls applied to it. Results contribute to the asset's aggregated risk rating and risk heat map placement.|
|Assessments|Regulatory risk assessments|Assessments that determine how an AI asset is classified against regulatory frameworks and requirements, such as unacceptable, high, medium, or low risk. Results populate the asset's regulatory risk classification.|
|Assessments|Bulk risk assessments|A grouping of risk assessments run across multiple AI assets at once, used to assess several assets against the same criteria in a single pass instead of individually.|
|Governance|Risks|Individual risk records identified for the AI asset, each describing a potential issue along with its inherent risk level. Risks are the basis for the asset's risk heat map and aggregated risk rating.|
|Governance|Controls|Control records that describe the safeguards applied to mitigate the risks identified for the AI asset. Control effectiveness ratings recorded here directly affect the asset's residual risk.|
|Tasks|Attestations|Records that capture confirmation that a control is in place and operating as expected, tied to a specific compliance framework or policy. Attestation state, such as Complete or Ready to take, feeds the asset's compliance score and compliance posture for priority frameworks.|
|Tracking|Issues|Records that track a compliance or control gap identified for the AI asset that requires remediation. Open issues surface as high-priority items in the asset's compliance posture and top action items.|
|Tracking|Policy exceptions|Records that document an approved deviation from a policy or control requirement for the AI asset, including justification and expiration. Policy exceptions provide an audit trail for accepted risk.|

