---
title: Add an existing AI system to a business application
description: Associate an existing AI Control Tower AI system with a business application from the Enterprise Architecture Workspace.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-04-16"
reading_time_minutes: 1
keywords: [AI system, business application, associate, AI Control Tower, enterprise architecture workspace, portfolio management, governance]
breadcrumb: [Working with an application portfolio, Working with Portfolio list view, Managing Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Add an existing AI system to a business application

Associate an existing AI Control Tower AI system with a business application from the Enterprise Architecture Workspace.

## Before you begin

Role required:

-   To add an existing AI system to a business application: sn\_apm.apm\_user
-   To view the AI system details in the AI Control Tower: sn\_aig.ai\_steward or sn\_aig.ai\_asset\_owner

## About this task

This task adds an existing AI system from AI Control Tower to a business application record.

You can also add a business application to a new AI System. For information, see [Request an AI use case form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/ai-risk-management/request-ai-system-form.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Architecture Workspace**.

2.  Open the Portfolio List view by selecting the Portfolio icon \(![Portfolio icon](../../image/portfolio-icon.png)\).

3.  Select the expand row icon \(![Expand Row icon](../../image/ExpandIcon.png)\) next to **Application Portfolio**.

4.  Select **Business Applications**.

5.  Select the business application that you want to add existing AI systems to.

6.  Select the **AI systems**.

7.  In the **Managed** or **Unmanaged** section, select **Add**.

    The **Add AI system** pop-up window appears.

    **Note:**

    -   **Managed** AI systems are AI systems that an AI Steward has reviewed or is under review. Managed systems are actively governed and tracked through their lifecycle in AI Control Tower.
    -   **Unmanaged** AI systems are AI systems created in AI Control Tower that have not yet been submitted for AI Steward review and have not entered the governance lifecycle.
8.  In the search field, type the name of the AI system and select it from the results.

    AI systems already associated with this business application do not appear in the search results.

9.  Select **Add**.

    The AI system appears in the **AI systems** tab.

    ![AI systems tab highlighted in the business applications related list.](../../image/eaw-image/ai-system-ba.png)

    The association also appears under **Workspaces** &gt; **AI Control Tower** &gt; **AI Assets** &gt; **AI systems** &gt; **Select an AI system** &gt; **Details** &gt; **Business applications**.


**Parent Topic:**[Working with an application portfolio](../../concept/eaw-concept/eaw-work-with-application-portfolio.md)

**Related topics**  


[AI Control Tower integration with Enterprise Architecture](../../concept/eaw-concept/eaw-aict.md)

[AI Control Tower Home](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/ai-control-tower-home-page.md)

