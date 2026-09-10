---
title: Set up a delegate for your assessments
description: Name another user to act on your Smart Assessments on your behalf for a set period.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/smart-assessment-engine/set-up-delegation-for-assessments.html
release: australia
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: task
last_updated: "2026-09-03"
reading_time_minutes: 1
breadcrumb: [Delegation, Respond to assessments, Manage, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Set up a delegate for your assessments

Name another user to act on your Smart Assessments on your behalf for a set period.

## Before you begin

User delegation must be enabled on the template category of the assessments you want to delegate. For more information, see [Create an assessment template category](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/sae-asmnt-template-category-create.md).

The delegate must also have the Smart Assessment role that the action requires. For example, to submit an assessment, the delegate must have the Assessment actor \[sn\_smart\_asmt.actor\] role.

Role required: sn\_smart\_asmt.actor to be a delegate of the owner. To be a delegate of the requestor, you need the sn\_smart\_asmt.assessment\_reader role instead.

## About this task

Delegation in the Smart Assessment Engine uses the standard ServiceNow platform delegate feature, which you configure from your user profile. For an overview, see [Delegation in Smart Assessment Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/delegation-in-sae.md).

## Procedure

1.  Open your user profile.

2.  Select **Delegates** tab.

3.  Select **New** to create a delegate.

4.  Add a delegate and select the user who will act on your behalf.

5.  Select the **Assignments** option.

    The Assignments option is what lets the delegate act on work assigned to you, including your Smart Assessments.

6.  Set the **Starts** and **Ends** dates for the delegation period.

7.  Save the delegate record.


## Result

During the delegation period, the delegate can act on your assessments in categories where delegation is enabled. A delegate of the owner can respond and submit. A delegate of the requestor can cancel and reassign an assessment.

