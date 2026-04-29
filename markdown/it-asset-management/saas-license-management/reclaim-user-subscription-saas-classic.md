---
title: Reclaim user subscriptions in Software Asset Management classic
description: Reclaim unused SaaS and SSO subscriptions in the Software Asset Management classic application.
locale: en-US
release: australia
product: SaaS License Management
classification: saas-license-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Reclaiming user subscriptions, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Reclaim user subscriptions in Software Asset Management classic

Reclaim unused SaaS and SSO subscriptions in the Software Asset Management classic application.

## Before you begin

Role required: sam\_user

**Important:** The SaaS License Management SurveyMonkey integration does not support reclamation through the ServiceNow AI Platform. To reclaim a SurveyMonkey user subscription, you must reassign or delete the user from your SurveyMonkey team directly using the SurveyMonkey admin portal. After the user is removed from your team, you must update the state of the corresponding removal candidate to **Closed Skipped** so that the user subscription is removed from the Software Subscriptions \[samp\_sw\_subscription\] table. See [Reclaim SurveyMonkey user subscriptions in Software Asset Management classic](reclaim-surveymonkey-subscription.md) for detailed instructions.

**Important:** The SaaS License Management monday.com integration does not support reclamation through the ServiceNow AI Platform. To reclaim a monday.com user subscription, you must deactivate the user on your monday.com account. After the user is deactivated, you must update the state of the corresponding removal candidate to **Closed Skipped** so that the user subscription is removed from the Software Subscriptions \[samp\_sw\_subscription\] table. See [Reclaim monday.com user subscriptions in Software Asset Management classic](reclaim-monday-subscription.md) for detailed instructions.

**Important:** The SaaS License Management Roadmunk integration does not support reclamation through the ServiceNow AI Platform. To reclaim a Roadmunk user subscription, you must deactivate the user on your Roadmunk account. After the user is deactivated, you must update the state of the corresponding removal candidate to **Closed Skipped** so that the user subscription is removed from the Software Subscriptions \[samp\_sw\_subscription\] table. See [Reclaim Roadmunk user subscriptions in Software Asset Management classic](reclaim-roadmunk-subscription.md) for detailed instructions.

## Procedure

1.  Navigate to **All** &gt; **Software Asset** &gt; **Removal Candidates** &gt; **Reclamation Candidates**.

2.  To reclaim a user subscription that was not automatically identified by a software reclamation rule, create a software removal candidate.

    See [Add a software removal candidate in Software Asset Management classic](t_AddAReclCandidate.md) for detailed instructions on how to create a software removal candidate in the Software Asset Management classic application.

3.  Reclaim user subscriptions.

    -   To reclaim all user subscriptions, click **Reclaim All**.

        **Note:** Use caution when reclaiming all user subscriptions. Some users may still need their subscriptions even if they have no activity.

    -   To reclaim a set of user subscriptions, specify your Search filter criteria and then click **Reclaim All**. For example, you can reclaim all user subscriptions for Adobe InDesign by selecting **Product** from the Search list and then entering `*InDesign`.
    -   To reclaim an individual user subscription, select a removal candidate and then click **Reclaim** on the Removal Candidate form.


## Result

After you reclaim a user subscription, the subscription record is deleted from the Software Subscriptions \[samp\_sw\_subscription\] table. The reclamation candidate state is set to **Closed Complete**. If the reclamation fails, the state is set to **Attention Required**. An error message is displayed at the top of the screen with additional details on how to resolve the error.

-   **[Reclaim SurveyMonkey user subscriptions in Software Asset Management classic](reclaim-surveymonkey-subscription.md)**  
Reclaim unused SurveyMonkey subscriptions to reduce your total software costs.
-   **[Reclaim monday.com user subscriptions in Software Asset Management classic](reclaim-monday-subscription.md)**  
Reclaim unused monday.com subscriptions to reduce your total software costs.
-   **[Reclaim Roadmunk user subscriptions in Software Asset Management classic](reclaim-roadmunk-subscription.md)**  
Reclaim unused Roadmunk subscriptions to reduce your total software costs.

**Parent Topic:**[Reclaiming user subscriptions](../concept/reclaiming-user-subscriptions-saas.md)

