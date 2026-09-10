---
title: Deal registration approvals and tasks
description: Deal registration approvals enable multi-step, configurable approval chains for deal records, while deal registration tasks let you manage work directly on deals without external task systems.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/order-management/deal-registration-approvals-and-tasks-overview.html
release: zurich
topic_type: concept
last_updated: "2026-07-20"
reading_time_minutes: 3
keywords: [deal registration, approval workflow, deal tasks, partner relationship management]
breadcrumb: [Deal Registration, Partner Relationship Management, Configure, Sales Customer Relationship Management]
---

# Deal registration approvals and tasks

Deal registration approvals enable multi-step, configurable approval chains for deal records, while deal registration tasks let you manage work directly on deals without external task systems.

## Approvals and tasks overview

Deal registration approvals and tasks are two related features that streamline deal management in Partner Relationship Management \(PRM\). Approvals verify that deals go through required approval chains before moving forward. Tasks let you track and manage work related to specific deals without leaving the deal record.

## Deal registration approvals

Deal registration approvals use the Advanced Approval Management \(AAM\) framework to create multi-step, configurable approval chains. Unlike the previous single-step approval flow, this framework lets you define when approvals are required and who must approve at each step.

The approval process has two layers: configuration and runtime. During configuration, an administrator sets up approval configurations, trigger conditions \(when approvals are needed\), approval rules \(who approves\), and approval chains \(the sequence of approvers\). At runtime, users submit deals for approval, and the system routes approval requests to the appropriate approvers based on the configuration.

When you submit a deal for approval, you see a preview showing which approvers receive the request and in what order. After approval by all required approvers, the deal moves to the approved state.

## Deal registration tasks

Previously, teams could not manage tasks directly on deal records. Any work related to a deal had to be tracked outside the deal registration system. This made it difficult to see all deal-related work in one place and raised the risk of missing service-level agreements \(SLAs\).

Deal registration tasks solve this by providing a dedicated task table that extends the ServiceNow platform task table. This table appears as a related list on deal records, so you can create, view, and manage tasks without leaving the deal.

You can create deal registration tasks when a deal is in any state except Draft, Closed, or Cancelled. This means tasks are available during all active approval and business phases.

## How approvals and tasks work together

Approvals and tasks complement each other in the deal lifecycle. As a deal moves through approval states \(Pending Approval, In Review, Approved\), you can create and track related tasks on the same record. This keeps all deal work—approvals and supporting tasks—visible in one place.

## Key concepts

-   **Approval trigger condition**

    A rule that defines when a deal requires approval \(for example, when the estimated deal size is less than one million dollars\).

-   **Approval rule**

    Specifies who the approvers are \(for example, the enterprise relationship manager\) and how they approve.

-   **Approval chain**

    Controls the sequential order in which approvers receive and act on approval requests.

-   **Deal registration task**

    A task record linked to a specific deal, used to track work that supports the deal lifecycle.

-   **Fulfiller role**

    A role automatically assigned to users without deal access when they are assigned a deal registration task, so they can see only that specific deal.


## Who uses these features

-   **Deal registration agents**

    Submit deals for approval and create tasks to track supporting work.

-   **Approvers \(Enterprise Relationship Managers\)**

    Review deal details and approve or reject deals with comments.

-   **Enterprise Relationship Managers**

    Manage deals and tasks for the channel partners in their portfolio.

-   **B2B and B2C agents**

    View and create tasks only for deals in their assigned deal type.

-   **PRM administrators**

    Configure approval rules, trigger conditions, and approval chains.


## When to use approvals and tasks

Use deal registration approvals when your organization requires authorization before deals can move forward—for example, when deal sizes exceed certain thresholds or require specific stakeholder sign-off.

Use deal registration tasks to coordinate any work that supports a deal, such as legal review, pricing adjustments, or follow-up communications. Tasks keep all deal-related work visible in one place and help teams track SLAs.

-   **[Deal Registration approvals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/deal-registration-approvals-overview.md)**  
Enable deal agents to submit deals for approval through a configurable approval workflow built on the Advanced Approval Management for Sales framework.

**Parent Topic:**[Deal Registration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/deal-registration-management.md)

