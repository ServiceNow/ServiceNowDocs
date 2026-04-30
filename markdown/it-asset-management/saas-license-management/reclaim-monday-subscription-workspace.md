---
title: Reclaim monday.com user subscriptions in the Software Asset Workspace
description: Reclaim unused monday.com subscriptions to reduce your total software costs.
locale: en-US
release: zurich
product: SaaS License Management
classification: saas-license-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Reclaim user subscriptions in the Software Asset Workspace, Reclaiming user subscriptions, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Reclaim monday.com user subscriptions in the Software Asset Workspace

Reclaim unused monday.com subscriptions to reduce your total software costs.

## Before you begin

To reclaim user subscriptions in the Software Asset Workspace, you must request and activate the Software Asset Workspace \(sn\_sam\_workspace\) store application. See [Request Software Asset Management](t_RequSoftwareAssetMgmt.md) for more details on requesting and activating the Software Asset Workspace \(sn\_sam\_workspace\) store application.

monday.com Role required: admin

ServiceNow Role required: sam\_user

## About this task

The SaaS License Management monday.com integration doesn’t support reclamation through the ServiceNow AI Platform. When Software Asset Management creates a removal candidate for your monday.com integration, you can reclaim the user subscription by deactivating the associated user on your monday.com account. After you deactivate the user, you must update the state of the removal candidate to **Closed Skipped** so that the user subscription is removed from the Software Subscriptions \[samp\_sw\_subscription\] table.

## Procedure

1.  Identify removal candidates for your monday.com integration.

    1.  From your ServiceNow instance, navigate to **Software Asset** &gt; **Software Asset Workspace**.

        The Software Asset Workspace launches in a new tab.

    2.  From the side navigation menu of the Software Asset Workspace, select **License usage**.

        The License usage view opens.

    3.  On the **Publishers** tab of the License usage view, select **monday.com Ltd.** from the list of available publishers.

        The monday.com Ltd. publisher overview opens.

    4.  Select the **Removal Candidates** related list to view the list of available removal candidates.

    5.  Take note of the removal candidates that you want to reclaim the user subscription for.

        Save this information for later use.

2.  Deactivate the associated users on your monday.com account.

    Based on the list of removal candidates that you identified in [step 1](reclaim-monday-subscription-workspace.md#identify-removal-candidate), you can reclaim user subscriptions by deactivating the associated users on your monday.com account.

    1.  From a web browser, go to [monday.com](https://monday.com/).

    2.  Log in using your admin credentials.

    3.  At the bottom of the side navigation menu, select your profile icon and then select **Admin**.

        The Admin section opens.

    4.  In the Admin section, select **Users**.

        The **Users** tab of the Users subsection opens. This tab displays the complete list of users on your monday.com account.

    5.  From the list of users, select the ellipsis icon \(…\) for the user that you want to deactivate.

    6.  When prompted, select **Deactivate user**.

    7.  Repeat steps e and f for each user that you want to deactivate.

3.  Return to your ServiceNow instance to update the state of each removal candidate to **Closed Skipped**.

    1.  From your ServiceNow instance, navigate to **Software Asset** &gt; **Software Asset Workspace**.

        The Software Asset Workspace launches in a new tab.

    2.  From the side navigation menu of the Software Asset Workspace, select **License usage**.

        The License usage view opens.

    3.  On the **Publishers** tab of the License usage view, select **monday.com Ltd.** from the list of available publishers.

        The monday.com Ltd. publisher overview opens.

    4.  Select the **Removal Candidates** related list.

    5.  From the list of available removal candidates, select the removal candidate number \(RCCxxxxxxx\) for a user that you deactivated in [step 2](reclaim-monday-subscription-workspace.md#remove-user).

    6.  On the Removal Candidate form, update the state of the removal candidate by selecting **Closed Skipped**.

    7.  Close the **Removal Candidate** tab.

4.  Verify the user deletion from the monday.com portal.

    1.  Run the **Refresh Monday.com subscriptions** scheduled job.

    2.  Verify the user deletion in the Software Subscriptions \[samp\_sw\_subscription\] table.


**Parent Topic:**[Reclaim user subscriptions in the Software Asset Workspace](reclaim-user-subscription-saas-workspace.md)

