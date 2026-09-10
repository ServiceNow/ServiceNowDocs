---
title: Exploring Autonomous Workforce
description: Learn more about Autonomous Workforce and review the benefits AI specialists can provide for different users in your organization.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/exploring-ai-workforce.html
release: australia
topic_type: concept
last_updated: "2026-08-11"
reading_time_minutes: 4
keywords: [explore, autonomous workforce, AI specialist, AI agents, service desk]
breadcrumb: [Autonomous Workforce, Enable AI experiences]
---

# Exploring Autonomous Workforce

Learn more about Autonomous Workforce and review the benefits AI specialists can provide for different users in your organization.

## Autonomous Workforce overview

Your autonomous workforce is made up of AI specialists. Each specialist combines individual AI agents that solve discrete tasks, such as prioritizing an incident or identifying similar records. Working together, these agents tackle bigger goals like task triage or updating requesters with solutions that worked for similar issues. The AI specialist performs tasks and is capable of functioning as a reliable extension of your workforce, taking on work that would bottleneck your team. Spend less time on ticket volume and more time delivering meaningful resolutions.

Assign your AI specialist to specific assignment groups and roles to limit the scope of its work and the data it can access. Once configured, you can test your AI specialist to confirm it behaves as expected before putting it to work. After activation, your AI specialist runs against real records, and you can monitor its performance and activity over time to confirm it continues to meet your needs.

## Accessing AI specialists

To access AI specialists, you must have the following plugins installed:

-   Zero Touch Service Desk plugin \[sn\_ztsd\] version 2.3.19+
-   ServiceNow Otto AI Agents \[sn\_aia\] version 7.1+
-   AI Engagement Experience \[sn\_now\_canvas\_ai\] version 3.1.1+

Your instance must also be at least on Zurich Patch 10 or Australia Patch 3.

## Autonomous Workforce users

Different users interact with Autonomous Workforce in various ways depending on their role and responsibilities.

|User|Role|Description|
|----|----|-----------|
|AI administrator|sn\_aia.admin|The AI administrator can configure and activate AI specialists using AI Agent Studio. After AI specialists are activated, they can monitor their performance and activity to track their effectiveness, efficiency, and customer satisfaction.|
|Service Desk manager|sn\_sow\_itsm\_common.sn\_service\_desk\_manager|Service Desk managers have the capabilities of a standard Service Desk Agent \(sn\_service\_desk\_agent\) and team level oversight and task resolution. They can view and manage team performance reports, analytics, and tasks and onboard an AI specialist to the team in Service Operations Workspace.|
|Service Desk agent|sn\_itsm\_common.sn\_service\_desk\_agent|Service Desk agents resolve tasks, such as incidents and cases, using their knowledge, research, and experience. They have access to the Service Operations Workspace, where they can view the work of an AI specialist on a record.|

## Autonomous Workforce workflow

Follow this workflow to implement and manage AI specialists in your organization.

For more information about considerations to make before deployment, see [General guidelines for deploying AI specialists](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gg-ai-workforce.md).

1.  Onboard an AI specialist.

    As an AI administrator, you can use AI Agent Studio to configure your AI specialists.

    After installing the applications and plugins and activating the sn\_aia.enable\_ai\_workers system property, you can activate an AI specialist as-is or configure any of the following:

    -   Basic details, including name, profile icon, department, and description
    -   Profile, including the roles and assignment groups
    -   Tasks, things the AI specialist can do
    -   Triggers, for running the AI specialist after specified events occur
2.  Manually assign tickets to your AI specialist to see how it works. Once you have built trust, create assignment rules or configure [Advanced Work Assignment](https://www.servicenow.com/docs/r/conversational-interfaces/advanced-work-assignment/awa-application-landing-page.html) to route work to your AI specialist automatically.
3.  Monitor AI specialist activity. You can review the records that the AI specialist has worked on individually to check how it's doing.
4.  Track AI specialist performance. Analytics for AI specialists that track their effectiveness, efficiency, and value can be found in AI Agent Studio and Service Operations Workspace. Use the analytics routinely to confirm that the AI specialist keeps up if things change. If performance isn't where you want it to be, you can configure it again at any time.

## Autonomous Workforce benefits

Autonomous Workforce provides specific benefits for different types of users in your organization.

|Benefit|Feature|
|-------|-------|
|Automate high-volume, repeatable requests to reduce manual effort and free up agents for complex work|AI specialist capabilities|
|Classify and triage incoming work to route requests to the right team faster|AI specialist tasks|
|Investigate related records to surface relevant context and accelerate resolution|AI specialist tasks|
|Communicate with requesters throughout the lifecycle of a request to keep them informed|AI specialist tasks|
|Monitor team and AI specialist performance to track efficiency and identify areas for improvement|Performance metrics|
|Test AI specialist behavior before activation to validate outcomes and reduce risk|AI specialist guided setup in AI Agent Studio|
|Simplified agentic AI setup reduces configuration complexity and helps accelerate time to value|AI specialist guided setup in AI Agent Studio|
|Enforce data security for agentic AI by assigning roles to control what each AI specialist can access and act on|AI specialist assigned roles|

## What to explore next

To learn more about configuring and using Autonomous Workforce, see:

-   [Configure AI specialist profiles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/modify-aiw-profile.md)
-   [Edit AI specialist tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/modify-aiw-tasks.md)
-   [Test AI specialists](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/test-aiw-ais.md)
-   [Monitor AI specialist activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/view-aiw-activity.md)
-   [Track AI specialist performance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/view-aiw-performance.md)

## Related products

For more information about the AI specialist for ServiceNow Otto for IT Service Management \(ITSM\), see [L1 IT Service Desk AI Specialist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/l1-service-desk-ai-specialist.md).

