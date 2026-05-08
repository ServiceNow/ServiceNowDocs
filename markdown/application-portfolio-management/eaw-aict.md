---
title: AI Control Tower integration with Enterprise Architecture
description: View and manage the AI systems associated with a business application from the Enterprise Architecture Workspace to understand AI risk and governance status as part of your broader application portfolio.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-14"
reading_time_minutes: 8
keywords: [AI governance, business applications, enterprise architecture, AI systems, portfolio management, AI steward, risk classification, lifecycle management, enterprise architecture workspace]
breadcrumb: [Exploring the application portfolio, Exploring Portfolio list view, Exploring Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# AI Control Tower integration with Enterprise Architecture

View and manage the AI systems associated with a business application from the Enterprise Architecture Workspace to understand AI risk and governance status as part of your broader application portfolio.

## Key benefits of AI Control Tower integration with Enterprise Architecture

The integration between the AI Control Tower and business applications is built around four core themes:

-   Unified AI governance: Connect AI oversight to your technology portfolio as an integrated capability. AI governance decisions can be made with full awareness of the business applications they affect.
-   Business context for AI: AI governance without business context is incomplete. AI stewards can see the applications, owners, and business impact tied to every AI system they govern — enabling better-informed decisions on approval, risk classification, and accountability.
-   Portfolio-wide AI visibility: Enterprise architects get AI adoption and governance status surfaced directly in their existing workflows — no context switching required. An enterprise architect responsible for hundreds of business applications can see exactly which ones are using AI, and whether that AI has been approved.

## Why AI systems are connected with business applications

Enterprise Architecture manages business applications by tracking their costs, business value, functional fitness, and risk. AI systems embedded in or supporting those applications introduce a new category of risk — one that requires dedicated governance beyond what traditional Enterprise Architecture covers. Without visibility into which AI systems are associated with each business application, an enterprise architect cannot form a complete picture of that application's risk profile, conformance, or operational dependencies.

At the same time, AI Control Tower governs AI systems through their full lifecycle — from onboarding and risk assessment through build, test, and deployment. However, AI governance is most effective when AI systems are understood in their business context: which applications depend on them, which business processes they support, and what the organizational impact would be if they were changed or decommissioned. That context lives in the Enterprise Architecture Workspace.

The integration between the Enterprise Architecture and AI Control Tower addresses both gaps. Enterprise architects can assess AI risk at the application level. AI stewards can ground governance decisions in business impact. Together, they give your organization a unified view of AI activity that spans both the application portfolio and the AI asset inventory.

The connection between AI systems and business applications enables you to:

-   Track total cost of ownership: Track AI systems related budgets at a business application level
-   Track ownership and accountability: Track AI system ownership through the business application it serves
-   Track AI system impact: Track the business impact the AI system is creating by connecting the AI system's technical outputs to the business functions it supports

## Value by persona

|Persona|Before integration|After integration|
|-------|------------------|-----------------|
|Enterprise architect|I manage 500 business applications but have no idea which ones are using AI or whether that AI is approved.|I can see AI adoption across my application landscape and understand governance status from my existing workspace.|
|AI steward|I govern AI systems but don't understand their business context—who owns the applications using them, how critical they are.|I see exactly which business applications depend on each AI system and who's accountable.|

## Value for enterprise architects

The **AI systems** tab on a business application record lets enterprise architects answer questions that were previously difficult to address from Enterprise Architecture alone:

-   Which AI systems are running inside or alongside this business application?
-   Are any of those AI systems still not reviewed and pending AI Steward approval?
-   What is the governance and lifecycle status of each AI system this application depends on?
-   If this application is being rationalized or retired, which AI systems will be affected?
-   What is the AI adoption picture across my entire application portfolio, and where are the governance gaps?

Because the **AI systems** tab surfaces data directly from AI Control Tower, enterprise architects don't have to switch workspaces or contact the AI governance team to get these answers. The AI system's lifecycle phase, state, lifecycle status, and risk classification are all visible from the business application record.

## Value for AI stewards and AI asset owners

AI Control Tower tracks AI systems through four lifecycle stages: onboard, assess, build and test, and deploy. At each stage, governance decisions — such as risk classification, conformance review, and approval — benefit from knowing the business context of the AI system being evaluated.

Without this integration, an AI steward reviewing a submitted AI system sees only its technical attributes. They have no visibility into which business applications depend on the system, who owns those applications, or how critical those applications are to the organization.

By associating AI systems with business applications, AI Stewards and AI Asset Owners gain visibility into the business scope of each AI system before they begin governance activities. This reduces the risk of approving or escalating an AI system without understanding which business processes and applications it affects.

The business application associations on an AI system record also support audit readiness. During an AI risk assessment or conformance review, being able to show which business applications an AI system supports — and that those applications are active, non-retired, and within scope — is a key part of the evidence trail.

## Managed and unmanaged AI systems

AI systems in the **AI systems** tab appear under one of two sections:

-   **Managed**

    AI systems that an AI Steward has reviewed or is under review. Managed systems are actively governed and tracked through their lifecycle in AI Control Tower.

-   **Unmanaged**

    AI systems created in AI Control Tower that have not yet been submitted for AI Steward review and have not entered the governance lifecycle.


Both sections are visible on the business application record so that enterprise architects can see not only the AI systems that have cleared governance review, but also those still awaiting it. An application with several unmanaged AI systems warrants closer attention during portfolio assessments and rationalization exercises.

The tab displays the following information for each AI system:

|Column|Description|
|------|-----------|
|Display name|The name of the AI system.|
|Provider|The organization or vendor that provides the AI system.|
|Vendor|The technology vendor associated with the AI system.|
|Managed by|The role responsible for managing the AI system, such as AI Asset Owner.|
|Lifecycle phase|The current phase in the AI system lifecycle: New, Assess, Build and test, or Deploy.|
|State|The current state of the AI system record, such as Development.|
|Lifecycle status|The review or approval status, such as AI steward review.|
|Risk classification|The risk level assigned to the AI system during governance review.|

## How associations are created

An AI system is associated with a business application in one of two ways:

-   A user submits the **Request an AI Use Case** catalog item in the service portal and selects one or more business applications in the **Business Applications** field. This is the recommended intake path because it creates the AI system record in AI Control Tower and establishes the business application association in a single step.

    For information on how to create an AI use case, see Request an AI use case.

    For information on the **Request an AI use case** form fields, see Request an AI use case form.

-   A user with the APM user \(sn\_apm.apm\_user\) role manually adds an AI system from the **AI systems** tab on a business application record in the Enterprise Architecture Workspace. This is useful for associating AI systems that were not submitted through the service portal intake form. For information, see [Add an existing AI system to a business application](../../task/eaw-task/eaw-add-ai-system-to-ba.md).

Only active business applications are available for association. Business applications with a status of Retired or a lifecycle stage of End of Life are excluded automatically, so the associations on an AI system record reflect only applications that are currently in scope for portfolio management.

Removing an AI system association from a business application record does not delete the AI system record from AI Control Tower. The AI system continues through its governance lifecycle independently of its application associations.

## Viewing associated business application in AI Control Tower

The association between AI systems and business applications is bidirectional. To view linked business applications in AI Control Tower, navigate to **Workspaces** &gt; **AI Control Tower** &gt; **AI Assets** &gt; **AI systems** &gt; **Select an AI system** &gt; **Details** &gt; **Business applications**. This view is read-only in AI Control Tower; to add or remove associations, use the **Related assets** &gt; **Business applications** &gt; **AI systems** tab on the business application record in the Enterprise Architecture Workspace.

For enterprise architects who work primarily in the Enterprise Architecture Workspace and AI stewards who work primarily in AI Control Tower, this bidirectionality means each team sees the same associations from their own workspace without requiring the other team to maintain a separate record.![Business applications related list displayed for an AI system in the AI Control Tower workspace.](../../image/eaw-image/ai-system-aict-related-list.png)

## Required roles

To view the **AI systems** tab on a business application record, you must have the APM User role \(sn\_apm.apm\_user\) or higher. Users with the AI Steward \(sn\_aig.ai\_steward\) or AI Asset Owner \(sn\_aig.ai\_asset\_owner\) role can add or remove AI system associations.

**Parent Topic:**[Exploring the application portfolio](eaw-app-portfolio.md)

**Related topics**  


[bundle-platai.ai-control-tower-home-page]

[eaw-exploring-the-ai-portfolio.md](eaw-exploring-the-ai-portfolio.md)

[Remove an AI system from a business application](../../task/eaw-task/eaw-unassign-ai-system-from-ba.md)

[View AI system details from a business application](../../task/eaw-task/eaw-view-ai-system-in-aict-from-ba.md)

