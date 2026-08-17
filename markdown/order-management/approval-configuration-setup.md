---
title: Approval configuration setup
description: Configure deal registration approval rules, trigger conditions, approver groups, and reminders to implement your organization's approval workflow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/approval-configuration-setup.html
release: australia
topic_type: reference
last_updated: "2026-08-17"
reading_time_minutes: 2
breadcrumb: [Deal Registration approvals, Deal Registration, Configure Partner Relationship Management, Configure, Sales Customer Relationship Management]
---

# Approval configuration setup

Configure deal registration approval rules, trigger conditions, approver groups, and reminders to implement your organization's approval workflow.

## Role Required

Deal Reg Admin \(sn\_prm\_dr.deal\_reg\_admin\), this role inherits the Approval Rule Admin role, who can configure deal registration approvals. For more information on Advanced Approval Management, see [Advanced Approval Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/explore-advanced-approval-for-sales.md).

## Configuration setup

Deal registration approval configuration uses the standard [Advanced Approval Framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/explore-advanced-approval-for-sales.md) application.

1.  Create Approval Config: Register the deal entity with the Advanced Approval Framework \(performed once per organization\).
2.  Define Trigger Conditions: Create conditions that determine when approval is needed \(for example, deal size less than $1 million\).
3.  Create Approval Rules: For each trigger condition, define who receives approval requests and in what sequence.
4.  Set up Approval Groups \(Optional\): Define groups of users who can be approvers to simplify rule management.
5.  Configure Approvers: Specify which users or user groups are approvers in each approval rule.
6.  Set Reminders \(Optional\): Configure automatic reminders to approvers about pending approval requests.
7.  Assign Approver role: Manually assign the Approver role to all users who approve deals.
8.  Test the workflow: Create test deals and verify that the approval workflow works as expected.

## Configuration example

Scenario: Your organization requires approval for all deals under $1 million. Approvals should go to the relationship manager for the partner, then to a designated deal reviewer.

Configuration includes:

-   Trigger Condition: Deal amount is less than $1,000,000.
-   Approval Rule: When trigger is met, send approval requests to relationship managers, then to deal reviewers.
-   Approval Group \(Optional\): Define "Relationship Managers" and "Deal Reviewers" groups to simplify management.
-   Approval Steps:
    -   Step 1: Relationship manager approval \(user must approve\).
    -   Step 2: Deal reviewer approval \(sequential, after step 1 is approved\).
-   Reminders: Send approvers a daily reminder about pending approvals.
-   Approver Role: Manually assign Approver role to all relationship managers and deal reviewers.

**Note:**

Before users can access and work on approval requests, the Deal Registration Admin must manually assign the Approver \(sn\_adv\_appr\_mgmt.approval\_request\_approver\) role to each user designated in the approval rules.

## Demo data and templates

You must configure your own approval rules and trigger conditions based on your organization's requirements. Demo data for approval configuration is not included in this release.

**Parent Topic:**[Deal Registration approvals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/deal-registration-approvals-overview.md)

