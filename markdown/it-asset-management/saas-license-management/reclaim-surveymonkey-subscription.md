---
title: Reclaim SurveyMonkey user subscriptions in Software Asset Management classic
description: Reclaim unused SurveyMonkey subscriptions to reduce your total software costs.
locale: en-US
release: australia
product: SaaS License Management
classification: saas-license-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reclaim user subscriptions in Software Asset Management classic, Reclaiming user subscriptions, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Reclaim SurveyMonkey user subscriptions in Software Asset Management classic

Reclaim unused SurveyMonkey subscriptions to reduce your total software costs.

## Before you begin

SurveyMonkey Role required: admin

ServiceNow Role required: sam\_user

## About this task

The SaaS License Management SurveyMonkey integration does not support reclamation through the ServiceNow AI Platform. When Software Asset Management creates a removal candidate for your SurveyMonkey integration, you can reclaim the user subscription by removing the associated user directly from your SurveyMonkey team. After you remove the user from your team, you must update the state of the removal candidate to **Closed Skipped** so that the user subscription is removed from the Software Subscriptions \[samp\_sw\_subscription\] table.

## Procedure

1.  Identify removal candidates for your SurveyMonkey integration.

    1.  From your ServiceNow instance, navigate to **Software Asset** &gt; **SaaS License** &gt; **Direct Integration Profiles**.

    2.  Select your SurveyMonkey integration profile from the Integration Profiles list.

    3.  On the **Software Models** tab of the Integration Profile form, select the software model that is associated with the integration profile.

    4.  On the Software Model form, select the **Reclamation Candidates** related tab to view the list of available removal candidates.

    5.  Take note of the user principal name for each removal candidate that you want to reclaim the user subscription for.

        Save this information for later use.

2.  Remove the associated users from your SurveyMonkey team.

    Based on the list of removal candidates that you identified in [step 1](reclaim-surveymonkey-subscription.md#identify-removal-candidate), you can reclaim user subscriptions by reassigning or deleting the associated users from your SurveyMonkey team.

    1.  From a web browser, open [SurveyMonkey](https://www.surveymonkey.com/).

    2.  Log in using your admin credentials.

    3.  On the left navigation menu, select **Manage Users**.

        The Manage Users page opens, where you can view the complete list of users in your SurveyMonkey team.

    4.  Click the ellipsis icon \(…\) for the user that you want to remove from your team.

        You can identify which user you want to remove based on the associated username. The username corresponds directly to the user principal name of each removal candidate that you identified in [step 1](reclaim-surveymonkey-subscription.md#identify-removal-candidate).

    5.  When prompted, select either **Reassign Account** or **Delete Account**.

        Select **Reassign Account** to move the user to another SurveyMonkey team. Select **Delete Account** to deactivate the user completely.

    6.  Repeat steps d and e for each user that you want to remove.

3.  Return to your ServiceNow instance to update the state of each removal candidate to **Closed Skipped**.

    1.  From your ServiceNow instance, navigate to **SaaS License** &gt; **Administration** &gt; **Direct Integration Profiles**.

    2.  Select your SurveyMonkey integration profile from the Integration Profiles list.

    3.  On the **Software Models** tab of the Integration Profile form, select the software model that is associated with the integration profile.

    4.  On the Software Model form, select the **Reclamation Candidates** related tab.

    5.  From the list of available removal candidates, select the removal candidate number \(RCCxxxxxxx\) for a user that you removed from your SurveyMonkey team in [step 2](reclaim-surveymonkey-subscription.md#remove-user).

    6.  On the Removal Candidate form, update the state of the removal candidate by clicking **Closed Skipped**.

        Software Asset Management removes the user subscription from the Software Subscriptions \[samp\_sw\_subscription\] table and automatically returns you to the Software Model form.

    7.  Repeat steps d through f for each user that you removed from your SurveyMonkey team.


**Parent Topic:**[Reclaim user subscriptions in Software Asset Management classic](reclaim-user-subscription-saas-classic.md)

