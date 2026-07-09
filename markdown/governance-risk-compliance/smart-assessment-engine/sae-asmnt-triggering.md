---
title: Triggering assessments
description: You can trigger a Smart Assessment Engine assessment from the Workflow Studio or from a script. With either method, you specify a published assessment template, the assessors who respond, and other optional inputs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/smart-assessment-engine/sae-asmnt-triggering.html
release: zurich
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Triggering assessments

You can trigger a Smart Assessment Engine assessment from the Workflow Studio or from a script. With either method, you specify a published assessment template, the assessors who respond, and other optional inputs.

**Important:** You can create an assessment only from a published assessment template. You can update a published template only if no active assessment is associated with the template.

-   **Trigger an assessment from Workflow Studio**

    Configure the Trigger Smart Assessment flow action to initiate the Smart Assessment Engine assessments and send them to the specified assessors. You then add the action to your flow.

    For more information, see [Configure the Trigger Smart Assessment Flow action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/smart-assessment-engine/sae-asmnt-trigger-from-flow.md).

-   **Trigger an assessment from a script**

    Use a script to execute the Trigger Smart Assessment flow action to generate Smart Assessment Engine assessments and assign them to the assessors.

    An example trigger condition might be that the state in the control table changes to **Attest**.

    For more information, see [Trigger assessments from a script](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/smart-assessment-engine/sae-asmnt-trigger-from-script.md).


**Related topics**  


[Flow Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/flow-designer.md)

[Building flows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/flows.md)

[Create a flow in Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/create-flow.md)

