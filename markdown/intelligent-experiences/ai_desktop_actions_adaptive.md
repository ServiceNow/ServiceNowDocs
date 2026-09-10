---
title: Adaptive desktop actions for desktop and web-based tasks
description: Let an AI agent perform automated actions directly on your desktop across browsers, desktop applications, and files using AI Desktop Actions. You maintain control and can pause the automation at any time to review or adjust steps.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ai\_desktop\_actions\_adaptive.html
release: australia
topic_type: concept
last_updated: "2026-07-14"
reading_time_minutes: 4
keywords: [AI Desktop Actions, agentic AI, desktop automation, ServiceNow AI Platform, action execution]
breadcrumb: [Explore, AI Desktop Actions, Enable AI experiences]
---

# Adaptive desktop actions for desktop and web-based tasks

Let an AI agent perform automated actions directly on your desktop across browsers, desktop applications, and files using AI Desktop Actions. You maintain control and can pause the automation at any time to review or adjust steps.

## Adaptive desktop actions overview

AI Desktop Actions extends the ServiceNow AI Platform and executes adaptive tasks on your desktop and applications without manual intervention. AI Desktop Actions is a client application that is installed on the macOS machine. AI Desktop Actions can autonomously process instructions, generate execution plans, and run desktop actions across legacy applications, thick client applications, and web applications. The application can do the following:

-   Open and interact with web browsers
-   Operate desktop applications
-   Manage files and documents
-   Perform multi-step workflows across different applications

The application presents its execution plan for your review and approval before taking any action on your desktop.

## AI Desktop Actions benefits

AI Desktop Actions delivers the following benefits:

-   **Reduced manual effort**

    Automation handles repetitive, multi-step tasks across applications without user intervention.

-   **User control and transparency**

    You review the AI agent's execution plan before it runs and can pause execution to make manual adjustments at any time.

-   **Optimized performance**

    The AI agent batches consecutive actions into single execution calls where possible, minimizing round trips and reducing overall execution time.

-   **Governance and consent**

    Explicit user consent is required before the AI agent can access desktop, third-party services, and files. Administrator-configured security policies may restrict AI agent resource access based on your organization's requirements.

-   **Execution visibility**

    Real-time status tracking shows whether the AI agent is initiating, running, or paused. Non-UI tasks that are processed in the background are tagged in AI steps to clarify execution context.


## How it works

-   **User request**

    You describe the task you want automated in natural language. For example: "Copy last month's invoices from PDFs in the Example folder into a new spreadsheet and save the spreadsheet with name "Nov 2026 invoices" on Desktop."

-   **AI planning**

    The AI Desktop Actions analyzes your request and creates a detailed execution plan with numbered steps.

-   **Plan review**

    The AI Desktop Actions presents the execution plan and Legal Disclaimer for your review. You can accept the plan or request modifications before proceeding.

-   **Execution**

    On your approval, AI agent executes the planned steps on your desktop. The execution workspace shows real-time status, such as Initiated, Running, Input needed, or Stopped.

-   **Control takeover**

    You can take manual control of the execution in the following scenarios:

    -   When AI agents require input, more information, or additional context, it pauses execution and status changes to **Input needed**. You can either provide the details in the chat interface or select **Take control** to perform the step manually.
    -   When you observe that AI agent does not execute the steps according to your expectations, you can select **Take control**. The AI agent pauses the execution and waits for you to make manual changes. You can then return control to the AI agent.
    After you're done, give control back to the AI agent. You can provide notes describing any manual changes you made, ensuring the AI agent resumes with correct context.


## Requirements and scope

The following requirements apply before using AI Desktop Actions:

-   Supported environments: The feature works with web browsers, installed desktop applications, and local file systems on the M-series macOS. Performance and compatibility depend on your target application behavior and configurations.
-   System permissions: On the macOS machine, you must grant the application two system permissions before use:

    -   **Screen Recording**: Enables the agent to see what is on your screen
    -   **Accessibility**: Enables the agent to control your keyboard and mouse
    You're prompted to grant these permissions when you first launch the application. The application requires a restart after permissions are granted.


## Third-party website access

When you use ServiceNow desktop actions to visit, access, log in to, or otherwise interact with \(collectively, “Access”\) websites, applications, or other digital properties owned or operated by a third party \(“Third Party Services”\), that Access is a direct interaction between you and the Third Party Services. You're responsible for adhering to any applicable terms and conditions, including all policies or statements governing the use of personal data, of the third party.

**Important:**

ServiceNow AI Desktop Actions rely on “computer use,” a beta technology provided by Anthropic. As a result, AI Desktop Actions users are subject to unique risks, including as described in Anthropic's documentation. Notwithstanding anything to the contrary in any customer agreement, or any other agreement governing a customer's use of ServiceNow offerings, ServiceNow AI Desktop Actions are provided “as is” and without representations or warranties of any kind, including any warranty that AI Desktop Actions will be uninterrupted, error free, or free of harmful components, or that any data, including customer data, will be secure or not otherwise lost or damaged.

**Related topics**  


[AI Desktop Actions user interface](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai_desktop_actions_reference_adaptive.md)

[Download AI Desktop Actions installer for adaptive desktop actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/download-agentic-desktop-installer-adaptive.md)

[Controlling what AI Desktop Actions can access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/security_policy_governance_concept.md)

[Execute adaptive desktop actions for desktop and web](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/use_ai_desktop_actions_adaptive.md)

