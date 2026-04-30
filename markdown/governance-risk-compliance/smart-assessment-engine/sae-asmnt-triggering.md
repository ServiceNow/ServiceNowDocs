---
title: Triggering assessments
description: You can trigger a Smart Assessment Engine assessment from the Workflow Studio or from a script. With either method, you specify a published assessment template, the assessors who respond, and other optional inputs.
locale: en-US
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

    For more information, see [Configure the Trigger Smart Assessment Flow action](../task/sae-asmnt-trigger-from-flow.md).

-   **Trigger an assessment from a script**

    Use a script to execute the Trigger Smart Assessment flow action to generate Smart Assessment Engine assessments and assign them to the assessors.

    An example trigger condition might be that the state in the control table changes to **Attest**.

    For more information, see [Trigger assessments from a script](../task/sae-asmnt-trigger-from-script.md).


**Related topics**  


[Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer&version=zurich&pubname=zurich-application-development&ft:locale=en-US)

[Building flows](https://www.servicenow.com/docs/access?context=flows&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)

[Create a flow in Workflow Studio](https://www.servicenow.com/docs/access?context=create-flow&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)

