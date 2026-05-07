---
title: AI Desktop Actions
description: ServiceNow AI Desktop Actions enables you to design, configure, and manage desktop actions that automate repetitive tasks in your desktop and web environment. AI agents can autonomously and semi-autonomously process instructions, generate execution plans, and run desktop actions across legacy systems, thick client applications, and web applications without APIs.
locale: en-US
release: australia
topic_type: reference
last_updated: "2025-10-12"
reading_time_minutes: 5
breadcrumb: [Enable AI experiences]
---

# AI Desktop Actions

ServiceNow® AI Desktop Actions enables you to design, configure, and manage desktop actions that automate repetitive tasks in your desktop and web environment. AI agents can autonomously and semi-autonomously process instructions, generate execution plans, and run desktop actions across legacy systems, thick client applications, and web applications without APIs.

-   Automating multi-step desktop or web tasks that involve conditional logic, so agents can focus on work that needs a human touch.
-   Adapting to changes in application state and UI in real-time, reducing the need to maintain rigid scripts.
-   Helping detect and recover from errors by evaluating context and trying alternative approaches when something doesn't go as expected.

## Types of desktop actions

There are two types of desktop actions: defined path and adaptive path. Both enable AI agents to automate tasks on behalf of users, but they differ in how steps are designed and executed, what applications they support, and how they handle variation in the user interface.

-   **[Adaptive desktop actions for web-based tasks](../concept/web-agents-overview.md)**

    With adaptive path desktop actions, you describe what task you want to accomplish on web at a high level in the tool configuration. The AI agent processes the request, generates an execution plan, and dynamically determines the specific steps needed to complete the task.

    Best for: Tasks that require flexibility, decision-making, or adaptation to changing UI elements.

-   **[Defined desktop actions for desktop and web-based tasks](../concept/desktop-actions.md)**

    With defined path desktop actions, you record or capture a fixed sequence of steps in the AI Desktop Actions Windows application. The AI agent executes these predefined steps in order without deviation.

    Best for: Repeatable tasks with consistent steps and predictable UI interactions.


For more information, see [When to use adaptive vs. defined path desktop actions](../concept/adaptive-vs-fixed-desktop-action.md).

## Get started

<table id="table_l3z_3x3_ygc" class="nav-card presentation"><tbody><tr><td>

[Explore![](../../../reuse/icons/brand-icons/bus-explore.svg)Learn about AI Desktop Actions concepts and features](../concept/explore-agentic-desktop.md)

</td><td>

[Configure![](../../../reuse/icons/brand-icons/bus-sdlc.svg)Set up AI Desktop Actions to automate desktop tasks](../task/configure-agentic-desktop.md)

</td><td>

[Design![](../../../reuse/icons/brand-icons/bus-low-code-dev-tools.svg)Design automations for legacy applications that do not have APIs](../concept/desktop-actions-designer-workspace-ad.md)

</td></tr><tr><td>

[Create an AI agent![](../../../reuse/icons/brand-icons/bus-virtual-agent.svg)Create your own custom AI agents with advanced multi-agent reasoning frameworks](../concept/create-ai-agents-ad.md)

</td><td>

[Use ![](../../../administer/document-intelligence/image/icon-use-docintel.png) Use the AI Desktop Actions application to execute automations using AI agents.](../concept/use-agentic-desktop.md)

</td><td>

[Reference![](../../../reuse/icons/brand-icons/bus-learn.svg)Get details about the AI Desktop Actions properties and components](agentic-desktop-reference.md)

</td></tr></tbody>
</table>**Important:**

-   Not all model providers are available for customers with in-country SKUs, and some Now Assist products/features are currently unavailable for in-country customers. For more information, see the [KB1584492](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1584492) article in the Now Support Knowledge Base. Be sure to check for model provider availability updates in future releases.
-   Some Now Assist products/features are currently unavailable for customers in the FedRAMP, NSC DOD IL5, or Australia IRAP-Protected data centers, self-hosted customers, or in other restricted environments. For more information, see the [KB0743854](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0743854) article in the Now Support Knowledge Base. Be sure to check for availability updates in future releases.
-   Some Now Assist products/features are currently available only for customers in some regions. Be sure to check for availability updates in future releases.
-   Some AI products and skills are not available in Regulated Markets. For more information, see [KB2593939: Regulated Markets AI Products/Skills Not Available](https://support.servicenow.com/kb?id=kb_article_view&sys_kb_id=e8d7cc82475aba90b7832920326d4362). Be sure to check for availability updates in future releases.

## Helpful resources

-   [Workflow Automation product on the ServiceNow Community](https://www.servicenow.com/community/workflow-automation/ct-p/workflow-automation)
-   [Search the Known Error Portal for known error articles](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0597477)
-   [Contact Customer Service and Support](https://support.servicenow.com/now?draw=case)

## AI limitations

This application uses artificial intelligence \(AI\) and machine learning, which are rapidly evolving fields of study that generate predictions based on patterns in data. As a result, this application may not always produce accurate, complete, or appropriate information. Furthermore, there is no guarantee that this application has been fully trained or tested for your use case. To mitigate these issues, it is your responsibility to test and evaluate your use of this application for accuracy, harm, and appropriateness for your use case, employ human oversight of output, and refrain from relying solely on AI-generated outputs for decision-making purposes. This is especially important if you choose to deploy this application in areas with consequential impacts such as healthcare, finance, legal, employment, security, or infrastructure. You agree to abide by [ServiceNow’s AI Acceptable Use Policy](https://www.servicenow.com/ai-acceptable-use-policy.html), which may be updated by ServiceNow.

## Data processing

This application requires data to be transferred from ServiceNow customers' individual instances to a centralized ServiceNow environment, which may be located in a different data center region from the one where your instance is, and potentially to a third-party cloud provider, such as Microsoft Azure. This data is handled per ServiceNow's internal policies and procedures, including our policies available through our [CORE Compliance Portal](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0564067).

## Data collection

ServiceNow collects and uses the inputs, outputs, and edits to outputs of this application to develop and improve ServiceNow technologies including ServiceNow models and AI products. In addition, this application will collect information about scripts \(and associated script records\) in which Now Assist for code generation is called. Customers can opt out of future data collection at any time, as described in the [Now Assist Opt-Out page](../../../administer/now-assist-admin/task/opt-out-of-data-sharing-for-now-assist.md).

For more information, see the [Now Assist documentation](../../../administer/now-assist-platform/concept/platform-now-assist-landing.md).

