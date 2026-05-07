---
title: Example prompts
description: Explore example prompts for building apps, as well as adding governance, UI and other ServiceNow metadata to help you get started with prompting Build Agent.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-04-30"
reading_time_minutes: 4
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Reference, Build Agent, Vibe coding and AI app development on the ServiceNow AI Platform, Building applications]
---

# Example prompts

Explore example prompts for building apps, as well as adding governance, UI and other ServiceNow metadata to help you get started with prompting Build Agent.

**Tip:**

-   You can craft a prompt and then feed it to an LLM, such as Claude, and ask for it to be made more specific for ServiceNow. To learn more about prompting, see this Community article on [The fastest way to learn Build Agent prompting? Ask Build Agent](https://www.servicenow.com/community/now-assist-for-creator-articles/the-fastest-way-to-learn-build-agent-prompting-ask-build-agent/ta-p/3533544).
-   If you're using Build Agent, include as much context as possible in your first prompt to enable more robust development. Include roles, data requirements, and success criteria.
-   If you're using Build Agent, ask it to create an overview of the app in a file, such as Markdown. Then ask Build Agent to use the file as context for its work.
-   You can use ESLint on the ServiceNow AI Platform to define your preferred coding style, and ask Build Agent to manage and enforce the ESLint configuration, for example using snake case for variables.

## Example Build Agent prompt to build an app

Prompt: `Create an application that handles several types of issues related to cash management. Create a custom data model with tables for each type of request. Add fields that are typical for these types of issues to each table. Request tables should extend the Task table. Create custom states for each request type to track issue resolution.`

![List of steps completed by Build Agent to build an app](../../vibe-coding/image/vc-ba-build-app-prompt-result.png "Build an app prompt outcome")

## Example Build Agent prompt to add security to an app

Prompt: `Create a new role and define permissions on the request tables for two types of users:`

1.  `Requesters who submit issues and can only view their own requests.`
2.  `Fulfillers who can view and edit all requests.`

![List of steps completed by Build Agent to add security to an app](../../vibe-coding/image/vc-ba-security-prompt-result.png "Add security to an app prompt outcome")

## Example Build Agent prompt to add business rules to an app

Prompt: `Create business rules for each request that is triggered by state changes in the workflow. Design the business rules to work together to create business processes aligned to industry best practices for each type of issue.`

![List of steps completed by Build Agent to add business rules to an app](../../vibe-coding/image/vc-ba-biz-rules-prompt-result.png "Add business rules to an app prompt outcome")

## Example Build Agent prompt to generate different UIs for an app

Prompt 1: `Create an easy to use UI for users with the cash management fulfiller role to view all issues, update and complete them.`

Prompt 2: `Create a UI for cash management requesters to submit issues and view or edit issues that they have previously created.`

![List of steps completed by Build Agent to generate fulfiller and requester UIs for an app](../../vibe-coding/image/vc-ba-ui-prompt-result.png "Generate different UIs for an app prompt outcome")

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

## Example prompts for governance

Prompting with governance requirements helps produce secure and compliant applications on the ServiceNow AI Platform. By embedding governance requirements directly into your prompts, you help the AI produce results aligned with your organizational standards for security, compliance, and quality.

For more information on governance, see [Build Agent governance](../concept/build-agent-governance.md).

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

**Parent Topic:**[Build Agent reference](build-agent-reference-landing.md)

