---
title: Example prompts
description: Explore example prompts for building apps, as well as adding governance, UI and other ServiceNow metadata to help you get started with prompting Build Agent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/building-applications/build-agent-example-prompts.html
release: zurich
product: Building Applications
classification: building-applications
topic_type: reference
last_updated: "2026-04-02"
reading_time_minutes: 6
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Reference, Build Agent, Agentic development on the ServiceNow AI Platform, Developing your application, Building applications]
---

# Example prompts

Explore example prompts for building apps, as well as adding governance, UI and other ServiceNow metadata to help you get started with prompting Build Agent.

To learn more about prompting, see this Community article on [The fastest way to learn Build Agent prompting? Ask Build Agent.](https://www.servicenow.com/community/now-assist-for-creator-articles/the-fastest-way-to-learn-build-agent-prompting-ask-build-agent/ta-p/3533544)

## Prompting overview and tips

Prompts are counted each time you submit a message to Build Agent. If Build Agent asks a clarifying question and you respond, that response counts as a prompt. Approving a plan that Build Agent presents does not count as a prompt. To get the most value from each prompt, draft your message in a text editor before you submit it.

For more guidelines on prompting, see [General guidelines for Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/building-applications/build-agent-general-guidelines.md).

## Prompt reference

Use the following prompts as starting points for common Build Agent goals. Replace the bracketed placeholders with your specific details.

|Goal|Prompt|
|----|------|
|Plan|`I want to build [app idea]. Create a detailed plan including tables, fields, roles, and business rules. Wait for my approval before creating any files.`|
|Prototype|`Build me a [app name] application with [key requirements]. Include basic roles, flows, and a working UI.`|
|Brainstorm|`I need to build something for [business problem]. What tables, flows, and catalog items would I need?`|
|Discover|`List the metadata types you can create or edit in this scope.`|
|Coach|`For [metadata type], coach me on an ideal prompt and common pitfalls.`|
|Extend|`Open [app name]. Add a field called [field] to the [table] table. Update the ACLs so only [role] can edit it.`|
|Extend out-of-box|`Add a custom field to the incident table called [field]. Create a business rule that [logic]. Show the plan before applying.`|
|Learn|`Explain [ServiceNow concept] to me. What is it, when do I use it, and show me an example.`|
|Debug|`I'm seeing this error: [paste exact error]. This happens when: [describe scenario]. Before suggesting fixes: 1) Help me reproduce this consistently. 2) Review the debugger output and logs. 3) Check for access or configuration issues. 4) Examine if this is a known issue.`|
|Document|`Create a README with setup instructions and a user guide for this application.`|
|Test|`Create ATF tests to validate [specific functionality] works correctly.`|
|Security|`Add role-based access so only [role] can edit; others are read-only. Show the plan and ACL changes before applying.`|
|Diagram|`Generate a Mermaid ER diagram showing all tables, fields, and relationships in this application.`|
|Flow|`Create a flow that triggers when [condition] and sends an email notification to [recipient] with [details].`|
|Ideal prompt|`Now that you've built this app, what's the ideal prompt to recreate it from scratch?`|

**Tip:** UI policies handle the common cases declaratively: show, hide, require, or lock fields based on conditions. For example, "when Category is Hardware, show the Asset Tag field and make it required" produces a UI policy that applies the rule without scripting.

## Get started with prompting

To get started with Build Agent, try one of the following approaches.

-   Prototype a simple app: Describe a straightforward application in one or two sentences. Review the plan that Build Agent presents, then approve it to start the build. This approach lets you learn the workflow with low risk.
-   Document an existing app: Open a custom scoped app and ask Build Agent to summarize its architecture, data model, roles, and key components. This produces useful documentation with no risk to the app.
-   Extend an existing app or base system table: Add a field, a business rule, or an ACL to an app you're familiar with. Build Agent supports global-scope tables such as Incident, as well as custom and ServiceNow Store apps.

## Starter prompts

Use the following prompt patterns to get started with common Build Agent tasks. Replace the bracketed placeholders with your specific details.

-   **Extend safely**

    `Open [app name]. Before making changes, document the current state. Then add [feature]. Return a plan for approval. After changes, generate ATF tests and a README.`

-   **Prototype**

    `Build me a [app name] application with [requirements]. Include basic roles, a working UI, and flows for [automation]. Then generate ATF tests and documentation.`

-   **Extend base system**

    `Add a custom field called [field] to the incident table. Create a business rule that [logic]. Show the plan and ACL changes before applying.`

-   **Document**

    `Summarize the app architecture, data model, roles, and key UI components. Don't make any changes.`


## Additional prompt suggestions

After you have the foundation of an app created, save your session and keep prompting to refine and extend your app. For example, you can create Automated Test Framework \(ATF\) tests, generate release notes, and prepare summaries. Some additional prompt ideas include the following examples:

-   Improve generated user interfaces
-   Create ATF tests
-   Create QA and UAT test plans
-   Create a summary of all application functionality
-   Add additional industry-specific use cases
-   Create an announcement
-   Create a user guide
-   Generate release notes
-   Draft change management plans
-   Create training materials for end users
-   Build data migration plans
-   Generate workflow optimization suggestions
-   Prepare executive summary for stakeholders

## Example Build Agent prompt to build an app

Prompt: `Create an application that handles several types of issues related to cash management. Create a custom data model with tables for each type of request. Add fields that are typical for these types of issues to each table. Request tables should extend the Task table. Create custom states for each request type to track issue resolution.`

\[Omitted image "vc-ba-build-app-prompt-result.png"\] Alt text: List of steps completed by Build Agent to build an app

## Example Build Agent prompt to add security to an app

Prompt: `Create a new role and define permissions on the request tables for two types of users:`

1.  `Requesters who submit issues and can only view their own requests.`
2.  `Fulfillers who can view and edit all requests.`

\[Omitted image "vc-ba-security-prompt-result.png"\] Alt text: List of steps completed by Build Agent to add security to an app

## Example Build Agent prompt to add business rules to an app

Prompt: `Create business rules for each request that is triggered by state changes in the workflow. Design the business rules to work together to create business processes aligned to industry best practices for each type of issue.`

\[Omitted image "vc-ba-biz-rules-prompt-result.png"\] Alt text: List of steps completed by Build Agent to add business rules to an app

## Example Build Agent prompt to generate different UIs for an app

Prompt 1: `Create an easy to use UI for users with the cash management fulfiller role to view all issues, update and complete them.`

Prompt 2: `Create a UI for cash management requesters to submit issues and view or edit issues that they have previously created.`

\[Omitted image "vc-ba-ui-prompt-result.png"\] Alt text: List of steps completed by Build Agent to generate fulfiller and requester UIs for an app

## Example prompts for governance

Prompting with governance requirements helps produce secure and compliant applications on the ServiceNow AI Platform. By embedding governance requirements directly into your prompts, you help the AI produce results aligned with your organizational standards for security, compliance, and quality.

For more information on governance, see [Build Agent governance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/building-applications/build-agent-governance.md).

**Tip:** If you have explicit security requirements, include them in your initial prompt.

## Prompt to include security roles and ACLs

`Create an Employee Onboarding app with HR and IT roles, enforce ACLs so only HR can edit personal data.`

## Specify data sensitivity

`Generate a table for medical records with encryption enabled and restrict access to compliance officers.`

## Request audit and logging

`Build a workflow for expense approvals and include audit logging for all status changes.`

## Mention testing requirements

`Create a catalog item for laptop requests and generate ATF tests for submission and approval flows.`

## Call out compliance standards

`Develop a leave management app that meets GDPR requirements and includes consent tracking.`

## Ask for documentation

`Generate a summary of the app and flow logic for governance review.`

**Parent Topic:**[Build Agent reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/building-applications/build-agent-reference-landing.md)

