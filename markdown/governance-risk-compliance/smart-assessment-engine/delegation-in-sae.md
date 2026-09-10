---
title: Delegation in Smart Assessment Engine
description: Delegation lets another user act on your assessments on your behalf for a set period, so work doesn't stall when a responder or requestor is unavailable.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/smart-assessment-engine/delegation-in-sae.html
release: australia
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: concept
last_updated: "2026-09-03"
reading_time_minutes: 2
breadcrumb: [Respond to assessments, Manage, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Delegation in Smart Assessment Engine

Delegation lets another user act on your assessments on your behalf for a set period, so work doesn't stall when a responder or requestor is unavailable.

## Delegation overview

In an assessment, some actions can be done only by specific people: only the owner can submit, and only the requestor or an assessment admin can cancel or reassign. If that person is unavailable, their part of the workflow stalls. Delegation addresses this by letting a user name another user to act on their behalf for a defined time period.

**Note:** This feature is available starting with Australia Patch 2.

Delegation in the Smart Assessment Engine uses the standard ServiceNow platform delegate feature. A user adds a delegate on their user profile, selects the **Assignments** option, and sets a start and end date. During that period, the delegate can act on the user's Smart Assessments. For the steps, see [Set up a delegate for your assessments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/set-up-delegation-for-assessments.md).

**Important:** This delegation is different from the granular, section-level delegation used in collaboration, where an owner assigns contributors to specific sections. For section-level access, see [Collaboration in assessments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/collaboration-in-assessments.md).

## Enabling delegation for a category

Delegation is turned off by default and is enabled for each template category. An assessment administrator can enable it, for more information see [Create an assessment template category](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/sae-asmnt-template-category-create.md).

Enabling delegation at the category level isn't enough on its own. Each user must also add a delegate and select the **Assignments** option on their own user profile before delegation works on their assessments. For the user-level steps, see [Set up a delegate for your assessments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/set-up-delegation-for-assessments.md).

## Delegate actions by role

A delegate inherits the ability to act in place of the user who delegated to them, based on that user's role in the assessment:

-   A delegate of the **owner** can respond to and submit the assessment.
-   A delegate of the **requestor** can cancel and reassign the assessment, and edit its due date while it's in the open state.
-   A delegate of an **assessment contributor** or **section contributor** can respond to questions within that contributor's scope.

**Note:** Delegation extends what a user can do on specific assessments; it doesn't grant roles. A delegate must independently have the Smart Assessment role that the action requires. For example, to submit an assessment on someone's behalf, the delegate must also have the Assessment actor \[sn\_smart\_asmt.actor\] role.

## Delegation visibility

Delegation is transparent. During the delegation period, the assessments that a user can act on for others appear in the delegate's assignment list, and the delegate works on them as usual. Actions the delegate takes, such as submitting or canceling, are recorded against the delegate.

