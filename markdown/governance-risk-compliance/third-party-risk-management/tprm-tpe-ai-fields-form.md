---
title: AI use case and AI model element fields
description: The Elements grid displays dynamic fields when you add or edit an AI use case or AI model element in the Third-party Risk Management application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/third-party-risk-management/tprm-tpe-ai-fields-form.html
release: brazil
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 5
keywords: [AI use case, AI model, third-party element, Elements grid]
breadcrumb: [Manage elements in the grid, Monitoring third-party elements, Monitor third-party risk, Third-party Risk Management, Governance, Risk, and Compliance]
---

# AI use case and AI model element fields

The Elements grid displays dynamic fields when you add or edit an AI use case or AI model element in the Third-party Risk Management application.

## Dynamic field behavior

Some fields in the Elements grid are static and appear for every element regardless of classification. For static fields, see [Third-party element form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-tpe-form.md). The fields in this topic are dynamic and appear only when you add or edit an AI use case or AI model element.

## AI use case dynamic fields

<table id="table_ai_use_case_fields"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Interaction type with end users

</td><td>

How the AI system interacts with end users.

 -   Not applicable
-   No direct interaction
-   Background support
-   Notifications &amp; prompts
-   User facing recommendations
-   Chat based interaction
-   Interactive experience

</td></tr><tr><td>

AICT State

</td><td>

The life cycle state of the AI use case.

 -   Draft
-   Deployed
-   Development

</td></tr><tr><td>

Area where the AI system is used

</td><td>

The business area or domain where the AI system operates.

 -   Internal operations
-   Customer services
-   Sales &amp; Marketing
-   Finance &amp; Accounting
-   IT &amp; Security
-   Supply chain
-   HR &amp; Workforce
-   External partner ecosystem

</td></tr><tr><td>

System autonomy level

</td><td>

The degree of autonomy the AI system has when making decisions or taking actions without human intervention.

 -   Not applicable
-   Assistive \(AI suggests\)
-   Semi automated
-   Condition based automation
-   Event triggered automation
-   Fully automated execution

</td></tr><tr><td>

Intended outcome of the AI system

</td><td>

The outcome the AI system produces.

 -   Not Applicable
-   Efficiency Boost
-   Quality Enhancement
-   Decision Guidance
-   Automation of Tasks
-   Customer Experience Upgrade
-   Insight Generation

</td></tr><tr><td>

Level of human involvement

</td><td>

The extent to which a human reviews or approves the AI system's outputs before they take effect.

 -   Not applicable
-   Full user control
-   User guided with AI support
-   Shared control
-   AI initiated with user approval
-   Fully automated workflow

</td></tr><tr><td>

Data used by the system

</td><td>

The type or category of data the AI system uses to generate its outputs.

 -   Public or general info
-   Business operational data
-   Customer interaction data
-   Behavioral or usage data
-   Profile or account data
-   Sensitive business data

</td></tr><tr><td>

Type of output produced

</td><td>

The kind of output the AI system generates.

 -   Simple alerts
-   Insight &amp; summaries
-   Ranking &amp; scores
-   Recommendations
-   Generated content
-   Automated decisions
-   System actions

</td></tr><tr><td>

Asset type

</td><td>

The type of underlying AI asset the use case is built on.

 -   Agentic AI
-   Classic AI
-   Digital worker
-   Generative AI

</td></tr><tr><td>

People affected by the AI system

</td><td>

The individuals or groups whose rights, safety, or opportunities may be affected by the AI system's use.

 -   Internal team
-   Specific customer groups
-   General customer base
-   External partners
-   Public or large audiences

</td></tr><tr><td>

Version

</td><td>

The version number of the AI use case.

</td></tr><tr><td>

Description

</td><td>

A description of the AI use case.

</td></tr><tr><td>

Provider

</td><td>

The organization that provides the AI use case.

</td></tr><tr><td>

Supported locations

</td><td>

The geographic locations where the AI use case applies or is supported.

</td></tr><tr><td>

Documentation

</td><td>

Links to documentation describing the AI use case, such as technical specifications or governance records.

</td></tr><tr><td>

License details

</td><td>

Information about the licensing terms that apply to the AI use case. **Note:** Check your entitlements to determine whether licensing terms apply to this AI use case.

</td></tr><tr><td>

Additional use &amp; purpose

</td><td>

Additional context about how or why the AI use case is used, beyond its primary intended outcome.

</td></tr><tr><td>

Department

</td><td>

The department responsible for, or using, the AI use case.

</td></tr><tr><td>

Related assets: AI models

</td><td>

Links the AI models the use case relies on. For more information, see [Manage elements in the grid](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-elements-grid-manage.md).

</td></tr></tbody>
</table>## AI model dynamic fields

<table id="table_ai_model_fields"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Global AI model

</td><td>

A global AI model can be linked to AI use case elements across multiple third parties. A local AI model \(with **Global AI model** cleared\) is available only within the third party where you created it. For more information, see [Manage elements in the grid](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-elements-grid-manage.md).

</td></tr><tr><td>

Deployment guidelines

</td><td>

Guidance on how to deploy the AI model, such as configuration or environment requirements.

</td></tr><tr><td>

Context window

</td><td>

The maximum amount of input the AI model can process in a single request, typically measured in tokens.

</td></tr><tr><td>

Model card

</td><td>

A link to or summary of the model card documenting the AI model's intended use, performance, and limitations.

</td></tr><tr><td>

Model size \(in MB\)

</td><td>

The size of the AI model, in megabytes.

</td></tr><tr><td>

Training procedure

</td><td>

The method used to train the AI model.

 -   Linear regression
-   Logistic regression
-   Decision trees
-   Random forest
-   Supervised learning
-   Unsupervised learning
-   Reinforcement learning
-   Transfer learning
-   Semi supervised learning
-   Instruction finetuning
-   Supervised finetuning

</td></tr><tr><td>

Required infrastructure

</td><td>

The hardware or infrastructure needed to run the AI model.

</td></tr><tr><td>

Model weights info

</td><td>

Information about the numerical weights learned during training that influence how the AI model generates outputs.

</td></tr><tr><td>

Model parameters info

</td><td>

Information about the AI model's parameters, such as the parameter count.

</td></tr><tr><td>

Evaluation metrics report

</td><td>

A report describing how the AI model was evaluated and the results of that evaluation.

</td></tr><tr><td>

Related assets: Base models

</td><td>

Links the base models the AI model relies on.

 A base model is a foundational AI model that has been pretrained on a large dataset and can be further fine-tuned for specific use cases. These models serve as a starting point for developing specialized AI models adapted to domain-specific data and requirements.

</td></tr><tr><td>

Version

</td><td>

The version number of the AI model.

</td></tr><tr><td>

Description

</td><td>

A description of the AI model.

</td></tr><tr><td>

Provider

</td><td>

The organization that provides the AI model.

</td></tr><tr><td>

Supported locations

</td><td>

The geographic locations where the AI model applies or is supported.

</td></tr><tr><td>

Supported languages

</td><td>

The languages the AI model supports.

</td></tr></tbody>
</table>**Related topics**  


[Third-party element form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-tpe-form.md)

[Manage elements in the grid](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-elements-grid-manage.md)

[Monitoring third-party elements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-monitor-tp-elements.md)

