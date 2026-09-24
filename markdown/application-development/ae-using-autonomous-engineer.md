---
title: Using Autonomous Engineer
description: Use Autonomous Engineer to provide requirements, review an implementation plan, and build all work items in parallel using background agents in Build Agent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ae-using-autonomous-engineer.html
release: brazil
topic_type: concept
last_updated: "2026-09-08"
reading_time_minutes: 3
keywords: [Autonomous Engineer, Build Agent, use, implementation plan, work items, plan dashboard, background agents, update set, ServiceNow Studio, requirements]
audience: programmer
breadcrumb: [Autonomous Engineer, Agentic development on the ServiceNow AI Platform, Building applications]
---

# Using Autonomous Engineer

Use Autonomous Engineer to provide requirements, review an implementation plan, and build all work items in parallel using background agents in Build Agent.

Use Autonomous Engineer in ServiceNow Studio to go from requirements to a working implementation without building each piece of metadata manually. Autonomous Engineer guides you through two phases: planning and execution. You review and approve the plan before any building begins.

## Provide requirements and review the plan

Start Autonomous Engineer from the chat panel in ServiceNow Studio and provide your requirements in any of the following forms:

-   A natural language prompt or paragraph.
-   A file upload, such as a CSV of user stories.

Autonomous Engineer conducts an interview to resolve ambiguous or incomplete details, then generates a plan with structured work items. Review each work item before approving the plan. You can open individual work items to read their details and make edits. Nothing is built until you approve.

If the plan includes manual steps, such as activating plugins, complete those steps before starting execution to reduce the risk of work item failures.

## Monitor and review execution

After you approve the plan, Autonomous Engineer generates a background agent for each work item and builds all work items in parallel. Monitor progress from the plan dashboard, which displays the status of each work item as it progresses.

As work items reach a ready-for-review state, open each one to review the generated artifacts and Test Agent \(ATF\) test results. Mark the item complete when it meets your requirements. If your requirements change during execution, edit a work item and ask Autonomous Engineer to retry. You can also roll back changes for an individual work item if needed.

Work items that can't be resolved automatically through retry cycles appear in the plan dashboard and the chat panel for your review.

For more information on using Test Agent, see [Test Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/test-agent-landing-page.md).

## Using the chat panel during a plan

While you navigate the plan and its work items, the chat panel remains in context of the plan. Use the chat panel to ask questions about the plan, check on the status of specific work items, and review any questions that background agents surfaced during execution.

-   **[Use Autonomous Engineer to implement an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/use-autonomous-engineer.md)**  
Use Autonomous Engineer \(powered by Build Agent\) to generate a plan from your requirements and build all work items in parallel, without creating each artifact individually. When implementing a ServiceNow product or application, Autonomous Engineer uses agent packs to give background agents product-specific domain knowledge.
-   **[Manage work items during execution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/manage-autonomous-engineer-work-items.md)**  
Monitor Autonomous Engineer work items as they build. You can review generated artifacts and test results, resolve work items that require attention, and export the update set when all work items are complete.
-   **[Update sets and Autonomous Engineer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ae-update-sets.md)**  
When you work with Autonomous Engineer, your changes are automatically tracked in update sets so you can review, revert, and deploy them without leaving ServiceNow Studio.
-   **[Test what you built with Autonomous Engineer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ae-test-what-you-built.md)**  
Test Agent generates test coverage for each work item that Autonomous Engineer builds, executes the tests, and performs root cause analysis \(RCA\) on failures.
-   **[Deploying what you built with Autonomous Engineer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ae-deployment.md)**  
When all work items are complete, Autonomous Engineer generates an update set that you export and move through the standard ServiceNow deployment process.

**Parent Topic:**[Autonomous Engineer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/autonomous-engineer.md)

