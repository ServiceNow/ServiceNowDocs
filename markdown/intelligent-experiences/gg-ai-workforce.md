---
title: General guidelines for deploying an autonomous workforce
description: AI specialists, like other agentic AI, benefit from strategic planning for testing, deploying, and monitoring performance. Learn guiding principles to help your AI specialists achieve their highest chances of success.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/gg-ai-workforce.html
release: australia
topic_type: concept
last_updated: "2026-08-11"
reading_time_minutes: 9
keywords: [AI specialists, autonomous workforce, deployment, general guidelines, agentic AI]
breadcrumb: [Explore, Autonomous Workforce, Enable AI experiences]
---

# General guidelines for deploying an autonomous workforce

AI specialists, like other agentic AI, benefit from strategic planning for testing, deploying, and monitoring performance. Learn guiding principles to help your AI specialists achieve their highest chances of success.

## Overview of deploying an autonomous workforce

AI specialists use artificial intelligence to perform work, but they don't require extensive knowledge about AI to set up and use. The possible tasks available to an AI specialist come pre-configured. You can choose which ones apply, test to verify that the AI specialist works as you expect, and then activate.

Like all AI, strategic planning for autonomous workforce implementation can be key to getting the most out of your AI specialists.

Questions to ask before you begin activating AI specialists might be:

-   What problems do I want my AI specialist to solve, and why?
-   Would an AI specialist be the best solution for these problems, or would they be better solved with an AI skill, AI agent, or agentic workflow?
-   What counts as success in terms of AI specialist effectiveness, efficiency, and customer satisfaction?
-   How do I want my team members to interact with an AI specialist?

AI specialists perform best under the following conditions:

-   Strong knowledge base: Well-maintained, procedural knowledge articles with clear self-service instructions for end users
-   High-volume of similar issues: Incidents with a single dominant root cause and clear resolution paths
-   Existing catalog items: Well-defined catalog items for accurate redirection of misclassified incidents
-   Clear policy rules: Approve/reject criteria that are explicit and well-documented

AI specialists don't perform well under the following conditions:

-   Sparse or outdated knowledge: knowledge articles that are incomplete, out of date, or written for internal audiences
-   Complex multi-step troubleshooting: issues that require orchestration across multiple external systems or remote device access
-   Undocumented internal knowledge: resolutions that depend on tacit knowledge not captured in formal systems
-   Highly sensitive categories: Personally identifying information, security incidents, or areas with severe cost of error should be avoided

## Configuring AI specialists in your autonomous workforce

When configuring an AI specialist, there are several important aspects to consider.

Within the AI specialist's profile, the sections each relate to different aspects of the AI specialist's suitability for certain work:

-   **Assignment groups: the work the AI specialist is assigned**

    The AI specialist can't work on tasks not assigned to those assignment groups. If you don't want the AI specialist to work on certain tasks, confirm that the correct assignment groups are selected.

-   **Roles: what data the AI specialist has access to**

    See the section [Data access security for AI specialists](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gg-ai-workforce.md).


The AI specialist's tasks specify the actions that it can take to solve problems within the domains. Each task has different options to configure the actions further. For more information about the different tasks available, see [Edit the tasks of an AI specialist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/modify-aiw-tasks.md).

## Operating modes: from supervised to autonomous

-   **Supervised \(Copilot\) mode**

    The AI specialist researches and drafts a proposed solution, but a person reviews and approves it before it reaches the requester. Use this mode when you don't yet have confidence in autonomous resolution for a given category.

-   **Autonomous mode**

    The AI specialist resolves and communicates independently, escalating to a human when its confidence is low.


Move an AI specialist to autonomous operation as soon as it has proven itself in testing. See the following section for guidance on when to hold a category back.

## Confidence, cost of error, and escalation

Before posting a resolution, an AI specialist scores its proposed solution and compares that score against a confidence threshold you configure. If the score meets the threshold, the solution is posted; if it falls short, the work routes to a human fulfiller instead. That score is informed by how well the solution is supported by evidence, how closely it fits the specific task, how likely it is to resolve the issue, and the AI specialist's overall certainty.

Not every category carries the same risk, so weigh cost of error alongside confidence: financial impact if the resolution is wrong, sensitivity if the category involves personally identifying information or security data, and whether the resolution is internal-facing or reaches a customer directly. Categories with a higher cost of error should stay in supervised mode, or stay outside the AI specialist's assignment groups, regardless of how well-suited they otherwise seem.

## Data access security for AI specialists

AI specialists only have access to the data that you specify. AI specialists can be assigned roles to limit their data access to certain scopes. Verify that the roles granted to the AI specialist are enough to enable it to complete its tasks, but not enough to access data it shouldn't. The roles function the same as the roles for a human user.

Consider these security principles when configuring AI specialist roles:

-   Apply the principle of least privilege by granting only the minimum roles necessary for the AI specialist to perform its assigned tasks.
-   Review role assignments regularly to verify they remain appropriate as your AI specialist's responsibilities evolve.
-   Test role configurations in a non-production environment before deploying to production.

**Important:** AI specialists can access and modify data based on their assigned roles. Verify that role assignments align with your organization's data governance and security policies.

## Assigning work to the AI specialist

Tasks must be assigned to the AI specialist. You can assign tasks to the AI specialist like any other user. Manual assignment, business rules or other triggers, and Advanced Work Assignment \(AWA\) all work. AWA allows you to select rules for assigning work so that work can be assigned automatically when the record is created or updated.

The User record associated with the AI specialist can be found on its [profile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/modify-aiw-profile.md). You can use business rules, triggers, or AWA to assign work to the AI specialist referencing that User record.

When setting up assignment rules, consider these factors:

-   Volume and complexity of work to confirm the AI specialist can handle the assigned workload
-   Priority levels to determine which tasks the AI specialist should handle first
-   Escalation paths for cases where the AI specialist can't complete a task

## Common failure modes to validate against

Certain conditions are reliable early warnings that a deployment will encounter issues. Validate against each of these before activating an AI specialist.

-   Task states that don't change during AI specialist execution, which can suggest extensive customizations that fall outside foundational readiness. Run the AI Readiness Evaluation application to assess foundational readiness before proceeding.
-   Task states that don't change during AI specialist execution, which can also suggest a state model that isn't mapped to the AI specialist's processing states. See [Edit the tasks of an AI specialist in the legacy AI Agent Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/modify-aiw-tasks.md) for steps to configure state mapping.
-   Test queries that return no results or surface internal-only content, which points to a knowledge base that isn't ready. Complete a knowledge audit and enforce audience separation before proceeding.
-   Poor knowledge base search results despite a ready knowledge base, which points to an AI Search profile misconfiguration. Inspect and adjust the Zero Touch Service Desk \(ZTSD\) search profile and AI Search configuration to target the right content for the AI specialist to rely on.
-   Zero assignments after activation, which points to an assignment rule or routing misconfiguration. Validate routing in a non-production environment and run a test task through the full routing chain across all intake channels.
-   A spike in reopened tasks, which points to accuracy issues. Start with thorough testing and gate any move to autonomous operation on whether you consistently meet the expected thresholds.
-   Work that sits with the AI specialist for more than 2 hours with no state change, which points to a broken escalation path. Validate escalation and run escalation test cases before activation.

## Previewing your AI specialist

Previewing your AI specialist on multiple records can show you what to expect when the AI specialist is activated and running.

**Important:** Changes made by the AI specialist during previews are actually made to the record.

Follow these testing guidelines to validate your AI specialist's performance:

-   Use representative tasks for initial validation. Selecting tasks that mirror the ones the AI specialist will handle enable you to check basic functions. You could also create dummy tasks that simulate active ones.

    **Note:** The AI specialist won't send any communications to users during tests.

-   Test across different incident and case categories. Testing multiple categories allows you to confirm that the AI specialist is working effectively in multiple domains.
-   Run at least 5 to 10 tests before activating. Try to create tests that cover all situations assigned to the AI specialist.
-   Test edge cases and unusual scenarios to see how the AI specialist handles unexpected situations.
-   Validate that the AI specialist respects data access controls and role-based permissions during testing.

## Improving AI specialist performance with feedback

AI specialists can make mistakes. With feedback or changes to the sources they access, you can improve their performance for next time.

Use these methods to monitor and improve AI specialist performance:

-   Administrators and Service Desk managers can review the individual steps an AI specialist took to reach its conclusions, in either Service Operations Workspace or the Core UI.
-   AI administrators and Service Desk managers can view an AI specialist's activity in AI Agent Studio. You can see the different tasks that your AI specialist has worked on. In the list, there is the option to provide granular feedback of either **Helpful** or **Not helpful**. You can open the record, check the AI specialist's work, and then submit the feedback in the activity list.
-   If the AI specialist makes errors based on knowledge articles that contain outdated or faulty information, knowledge administrators can update the articles to improve AI specialist performance.

Establish regular performance review cycles to:

-   Analyze AI specialist activity logs and success rates
-   Identify patterns in errors or suboptimal performance
-   Update knowledge base content based on AI specialist performance
-   Adjust AI specialist configuration based on performance data

## Ongoing monitoring and optimization

After deploying your AI specialist, continuous monitoring helps maintain optimal performance and identify opportunities for improvement. You can track the performance analytics of an AI specialist by selecting them in AI Agent Studio. See [View AI specialist performance metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/view-aiw-performance.md).

Key metrics include:

-   Task completion rates and mean time to resolution
-   User satisfaction scores and feedback
-   Escalation rates to human agents
-   Durable auto-resolve rate: the percentage of work the AI specialist resolves with no reopen during the post-resolution monitoring window
-   AI coverage rate: the percentage of eligible volume the AI specialist is actually eligible to handle, which keeps scaling honest rather than cherry-picking easy work
-   Time to value: how quickly enough production data exists to quantify impact after go-live

Regular optimization activities should include:

-   Refining assignment rules to improve work distribution
-   Updating knowledge base content to address new scenarios
-   Adjusting role assignments based on security reviews and changing requirements

