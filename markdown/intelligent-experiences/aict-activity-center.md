---
title: Activity Center
description: Track and act on the governance work generated across AI Control Tower from a single workspace, including lifecycle tasks, security tasks, change and offboarding requests, and AI recommendations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/aict-activity-center.html
release: zurich
topic_type: concept
last_updated: "2026-07-16"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Explore, AI Control Tower, Enable AI experiences]
---

# Activity Center

Track and act on the governance work generated across AI Control Tower from a single workspace, including lifecycle tasks, security tasks, change and offboarding requests, and AI recommendations.

## Key benefits

-   Find every piece of governance work that needs your attention across AI Control Tower in one place, instead of switching between asset records, dashboards, and email.
-   Distinguish work assigned to you, work your team owns, work with no owner, and work you've submitted, so you can focus on what's yours and route what isn't. Team-level visibility is available to the AI steward.
-   Resolve AI-generated recommendations directly or hand them off to the part of AI Control Tower where the resolution happens.

\[Omitted image "aict-activity-center.png"\] Alt text: Tasks in Activity Center grouped by Task type.

## Required roles

The AI steward \[sn\_ai\_governance\_ai\_steward\] or AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\] role is required to access the **Activity Center** in AI Control Tower.

## Accessing Activity Center

Access the **Activity Center** in AI Control Tower by navigating to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Activity Center**. Select **Work** to track governance work items or **Recommendations** to review AI-generated recommendations.

## Use cases

Activity Center organizes governance work into two views: **Work** and **Recommendations**.

On the Work page, items are organized by ownership across four tabs: **Assigned to you**, **Team**, **Unassigned**, and **Submitted by you**. The **Team** tab is available only to the AI steward role. Within each tab, items are grouped into sub-tabs by type, such as lifecycle tasks, security tasks, requests, cases, risk assessments, issues, attestations, policy exceptions, and inquiries, each showing a count of open items.

-   Focus on the work that's yours to complete on the **Assigned to you** tab, including your active lifecycle tasks, security tasks, requests, and other governance items sorted by due date. For example, complete an impact assessment that's due today before turning to lower-priority items waiting later in the week.
-   Stay ahead of governance work piling up across your team by viewing the **Team** tab, which shows lifecycle tasks, security tasks, requests, and other governance items assigned across team members. For example, identify which team members are behind on critical onboarding tasks before a managed AI asset stalls because nobody noticed a review was past due.
-   Claim or route work that has no owner on the **Unassigned** tab. For example, take ownership of an unrouted security task before a threat detected against a managed AI asset sits waiting for someone to claim it.
-   Track the items you've submitted for review on the **Submitted by you** tab. View the cases, issues, policy exceptions, and inquiries that you've created, along with their current status.
-   As an AI steward, review and approve a change request before it disrupts production. From the **Requests** sub-tab on the **Team** or **Assigned to you** tab, see the change requests and offboarding requests waiting for AI steward approval. For example, review the impact on related sub-systems before approving an asset owner's request to swap out the AI model backing an agent.
-   As an AI Asset Owner, access and act on risk and compliance lifecycle tasks. Tasks include impact assessments and control attestations. The Activity Center surfaces AI asset tasks, issues, policy exceptions, and AI cases for the asset owner.
-   Create a case, issue, policy exception, or inquiry without leaving Activity Center. For more information, see [Managing AI tasks and approvals in Activity Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/aict-managing-tasks-and-approvals.md).

On the **Recommendations** page, you can resolve a backlog of similar AI recommendations by filtering the full list of AI-generated recommendations by category, priority, confidence, or outcome. For example, filter by the **Improve inventory signal** outcome to work through several assets that are missing descriptions in one pass. For more information about how recommendations are generated, prioritized, and resolved, see [Recommendations and AI insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/aict-recommendations-ai-insights.md).

