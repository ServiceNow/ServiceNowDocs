---
title: Reclaim SurveyMonkey user subscriptions in the Software Asset Workspace
description: Reclaim unused SurveyMonkey subscriptions to reduce your total software costs.
locale: en-US
release: zurich
product: SaaS License Management
classification: saas-license-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Reclaim user subscriptions in the Software Asset Workspace, Reclaiming user subscriptions, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Reclaim SurveyMonkey user subscriptions in the Software Asset Workspace

Reclaim unused SurveyMonkey subscriptions to reduce your total software costs.

## Before you begin

To reclaim user subscriptions in the Software Asset Workspace, you must request and activate the Software Asset Workspace \(sn\_sam\_workspace\) store application. See [Request Software Asset Management](t_RequSoftwareAssetMgmt.md) for more details on requesting and activating the Software Asset Workspace \(sn\_sam\_workspace\) store application.

SurveyMonkey Role required: admin

ServiceNow Role required: sam\_user

## About this task

The SaaS License Management SurveyMonkey integration doesn’t support reclamation through the ServiceNow AI Platform. When Software Asset Management creates a removal candidate for your SurveyMonkey integration, you can reclaim the user subscription by removing the associated user directly from your SurveyMonkey team. After you remove the user from your team, you must update the state of the removal candidate to **Closed Skipped** so that the user subscription is removed from the Software Subscriptions \[samp\_sw\_subscription\] table.

## Procedure

1.  Identify removal candidates for your SurveyMonkey integration.

    1.  From your ServiceNow instance, navigate to **Software Asset** &gt; **Software Asset Workspace** &gt; **License usage**.

    2.  On the **Publishers** tab of the License usage view, select **SurveyMonkey** from the list of available publishers.

        The SurveyMonkey publisher overview opens.

    3.  Select the **Removal Candidates** related list to view the list of available removal candidates.

    4.  Take note of the removal candidates for which you want to reclaim the user subscription.

        Save this information for later use.

2.  Remove the associated users from your SurveyMonkey team.

    Based on the list of removal candidates that you identified in [step 1](reclaim-surveymonkey-subscription-workspace.md#identify-removal-candidate), you can reclaim user subscriptions by reassigning or deleting the associated users from your SurveyMonkey team.

    1.  From a web browser, open [SurveyMonkey](https://www.surveymonkey.com/).

    2.  Log in using your admin credentials.

    3.  On the side navigation menu, select **Manage Users**.

        The Manage Users page opens, where you can view the complete list of users in your SurveyMonkey team.

    4.  Select the ellipsis icon \(…\) for the user that you want to remove from your team.

    5.  When prompted, select either **Reassign Account** or **Delete Account**.

        Select **Reassign Account** to move the user to another SurveyMonkey team. Select **Delete Account** to deactivate the user completely.

    6.  Repeat steps d and e for each user that you want to remove.

3.  Return to your ServiceNow instance to update the state of each removal candidate to **Closed Skipped**.

    1.  From your ServiceNow instance, navigate to **Software Asset** &gt; **Software Asset Workspace** &gt; **License usage**.

    2.  On the **Publishers** tab of the License usage view, select **SurveyMonkey** from the list of available publishers.

        The SurveyMonkey publisher overview opens.

    3.  Select the **Removal Candidates** related list.

    4.  From the list of available removal candidates, select the removal candidate number \(RCCxxxxxxx\) for a user that you removed from your SurveyMonkey team in [step 2](reclaim-surveymonkey-subscription-workspace.md#remove-user).

    5.  On the Removal Candidate form, update the state of the removal candidate by selecting **Closed Skipped**.

        Software Asset Management removes the user subscription from the Software Subscriptions \[samp\_sw\_subscription\] table.

    6.  Close the Removal Candidate form.

    7.  Repeat steps e through g for each user that you removed from your SurveyMonkey team.


**Parent Topic:**[Reclaim user subscriptions in the Software Asset Workspace](reclaim-user-subscription-saas-workspace.md)

