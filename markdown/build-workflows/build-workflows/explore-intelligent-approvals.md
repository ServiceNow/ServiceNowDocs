---
title: Explore intelligent approvals
description: Learn how intelligent approvals automate approval decisions by directly connecting to approval policy documentation.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2026-07-01"
reading_time_minutes: 4
keywords: [explore, intelligent approvals, approval policies, AI approvals]
---

# Explore intelligent approvals

Learn how intelligent approvals automate approval decisions by directly connecting to approval policy documentation.

## Intelligent approvals overview

Intelligent approvals is an AI-first capability that modernizes how organizations govern and execute policy decisions. Policy owners upload their approval policies directly without relying on developers to build approval workflows. AI continuously interprets these policies and evaluates incoming requests as they are made, automatically approving or rejecting routine cases that clearly meet policy criteria. Ambiguous or edge case requests fall back to humans for evaluation and approval.

This capability closes the gap between policy intent and approval execution. Policy documents are the single source of truth, eliminating the need for developers to translate business policies into code. When business conditions change, business users can update the policy document, and AI uses the latest policy to keep approvals accurate and up to date.

## Approval decisions

An active intelligent approval evaluates approval requests and generates approval decisions at runtime. The intelligent approval must be published before it can process approval requests. For each request, an intelligent approval returns one of these outcomes:

-   Auto-approve
-   Auto-reject
-   Can't decide

When an intelligent approval reaches an automatic approval or rejection decision, the system performs these actions.

-   The system creates an Approval \[sysapproval\_approver\] record with a state of **Approved** or **Rejected**.
-   The system adds a comment to the approval that explains how the decision was made.
-   The system updates any related approval records that are waiting for human approval to the state of **No Longer Required**.

When an intelligent approval can't decide, the request falls back to the existing approval workflow and is routed to a human for an approval decision. The human approval reviewer receives work notes on the parent record and approval request indicating that AI attempted evaluation but could not determine an outcome.

**Important:** Intelligent approvals uses generative AI to evaluate requests and generate approval decisions. AI-generated decisions are based on the content of your policy documents and may not account for all circumstances. Review AI decisions and maintain human oversight processes appropriate to your organization.

Intelligent approvals can potentially conflict with existing approval workflows. If an existing approval workflow has the same trigger conditions as an Intelligent approval, the existing approval workflow will create approval records assigned to humans. You can use the option **Potential overlapping approvals** to identify existing workflows that run on the same trigger conditions and records.

## Intelligent approvals users

|User|Description|
|----|-----------|
|Policy owner|Policy owners create and manage approval policies by uploading policy documents or referencing existing documents. They review AI-generated policy interpretations, refine intelligent approvals through chat experiences, and publish finalized intelligent approvals for immediate activation across all incoming requests.|
|Business user|Business users submit requests that are automatically evaluated against intelligent approvals. They receive faster approval decisions for routine requests that clearly meet policy criteria, while complex cases are routed to appropriate human approval users.|
|Approval user|Approval users handle requests that AI can't confidently evaluate based on existing approval policies. When AI can't make a decision, approval users receive work notes on the parent record and approval request indicating that AI attempted evaluation but could not determine an outcome. Approval users can also review audit trails of automatic approvals made by the system.|

## Intelligent approvals workflow

The following workflow shows how policy owners, business users, and approval users interact with intelligent approvals to streamline policy governance and approval execution.

1.  Policy owners upload an approval policy document.
2.  AI interprets the uploaded policy document, extracts trigger conditions and policy areas, and calculates a confidence score based on test scenarios.
3.  Policy owners review AI-generated intelligent approvals, preview how intelligent approvals will be applied, and identify potential conflicts with existing workflows.
4.  Policy owners can optionally refine the policy document based on AI suggested improvements, upload an updated policy, and when satisfied with the results, publish the intelligent approval.
5.  When approval requests are submitted, AI evaluates them against the intelligent approval and automatically approves or rejects requests that clearly meet criteria.
6.  When AI can't make a confident decision, the request falls back to the existing approval workflow. Human approval users receive work notes indicating AI attempted evaluation but could not reach a decision.
7.  All approval decisions, both automatic and human, are recorded as approval records. Work notes indicate whether the decision was made automatically based on an intelligent approval or by a human approval user.

## Intelligent approvals benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Eliminate developer dependency for policy implementation by uploading policy documents directly and letting AI interpret them.|Policy document upload and AI interpretation|Policy owner|
|Reduce approval processing time through real-time AI evaluation and automatic approval of routine requests.|Real-time policy evaluation and automated approvals|Business user|
|Maintain policy accuracy with immediate enforcement when business conditions change, without workflow rewrites.|Dynamic policy updates and activation|Policy owner|
|Improve decision consistency by using policy documents as the single source of truth for all approval decisions.|Centralized policy management and audit trails|Approver|
|Verify policy effectiveness through test results scoring and preview capabilities before activation.|Policy preview and test results scoring|Policy owner|

## Intelligent approvals homepage

\[Omitted image "intelligent-approval-homepage-update-path-01.png"\] Alt text: Sample Intelligent approval homepage

The Intelligent approvals homepage offers the following information and options.

-   Total number of decisions made
    -   Total auto approved
    -   Total auto rejected
    -   Total undecided
-   Option to create an intelligent approval
-   List of decisions made by each intelligent approval
    -   Approved
    -   Rejected
    -   Undecided
-   List of intelligent approvals by state
    -   Active
    -   Inactive

## What to explore next

To learn more about configuring and using intelligent approvals, see:

-   [Configure intelligent approvals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/configure-intelligent-approvals.md)
-   [Build intelligent approvals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/build-intelligent-approvals.md)
-   [Intelligent approvals reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/reference-intelligent-approvals.md)

