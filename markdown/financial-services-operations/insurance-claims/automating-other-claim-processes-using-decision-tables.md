---
title: Automating Insurance claims processes by using decision tables
description: You can apply the decision table rules and subflow or flow that executes the decision table to automate claims processes in the Insurance claims application.
locale: en-US
release: xanadu
product: Insurance Claims
classification: insurance-claims
topic_type: concept
last_updated: "2024-10-10"
reading_time_minutes: 1
breadcrumb: [Setting up Insurance claims, Insurance claims, Claims applications, Insurance applications, Financial Services Operations \(FSO\)]
---

# Automating Insurance claims processes by using decision tables

You can apply the decision table rules and subflow or flow that executes the decision table to automate claims processes in the Insurance claims application.

You can configure decision rules to automate claims processes. These decision rules are executed in the background through a subflow or flow during the claim life cycle. By using this approach, you can automate labor-intensive tasks, streamline decision-making processes, and ensure consistency in how claims are handled throughout their life cycle.

Some examples include:

-   Introducing claim validation rules in a decision table, with a subflow that executes these rules. The outcome of this subflow determines how the flow proceeds, automating the validation process for claims.
-   Introducing claim fraud detection rules in a decision table, where the outcome dictates the flow's logic. If a potential fraud is detected, the process can be routed for further investigation or other actions.

You can create and add input parameters to the Insurance claims automation rules decision tables based on your specific business requirements. By doing so, you can further customize your claims workflow automation, ensuring that the decision table aligns with your organization's processes. As an example, the Claim triage rules are provided with this application.

If you add new input parameters, you can also add or modify the corresponding subflows. This adjustment ensures that the subflow properly passes the new parameters to the decision table, which allows it to function correctly with the updated logic.

You can modify the included decision table in the Insurance claims application so that you can define how claims are triaged in your workflow. For more information, see [Use claim automation decision tables](../task/update-insurance-claims-automation-using-decision-tables.md).

**Related topics**  


[Using decision tables](https://www.servicenow.com/docs/access?context=using-decision-builder&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)

[Configure flows](../../fso-common/task/configure-flow-designer-flows-fso-apps.md)

[Designer flows for Financial Services Operations applications](../../fso-common/reference/flow-designer-flows-fso-apps.md)

