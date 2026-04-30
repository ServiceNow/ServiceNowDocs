---
title: Reclaim Roadmunk user subscriptions in Software Asset Management classic
description: Reclaim unused Roadmunk subscriptions to reduce your total software costs.
locale: en-US
release: yokohama
product: SaaS License Management
classification: saas-license-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Reclaim user subscriptions in Software Asset Management classic, Reclaiming user subscriptions, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Reclaim Roadmunk user subscriptions in Software Asset Management classic

Reclaim unused Roadmunk subscriptions to reduce your total software costs.

## Before you begin

Roadmunk Role required: Account Admin

ServiceNow Role required: sam\_user

## About this task

The SaaS License Management Roadmunk integration does not support reclamation through the ServiceNow AI Platform. When Software Asset Management creates a removal candidate for your Roadmunk integration, you can reclaim the user subscription by deactivating the associated user on your Roadmunk account. After you deactivate the user, you must update the state of the removal candidate to **Closed Skipped** so that the user subscription is removed from the Software Subscriptions \[samp\_sw\_subscription\] table.

## Procedure

1.  Identify removal candidates for your Roadmunk integration.

    1.  From your ServiceNow instance, navigate to **All** &gt; **Software Asset** &gt; **SaaS License** &gt; **Direct Integration Profiles**.

    2.  Select your Roadmunk integration profile from the Integration Profiles list.

    3.  On the **Software Models** tab of the Integration Profile form, select the software model that is associated with the integration profile.

    4.  On the Software Model form, select the **Reclamation Candidates** related tab to view the list of available removal candidates.

    5.  Take note of the user principal name for each removal candidate that you want to reclaim the user subscription for.

        Save this information for later use.

2.  Deactivate the associated users on your Roadmunk account.

    Based on the list of removal candidates that you identified in [step 1](reclaim-roadmunk-subscription.md#identify-removal-candidate), you can reclaim user subscriptions by deactivating the associated users on your Roadmunk account.

    1.  From a web browser, open [Roadmunk](https://roadmunk.com/).

    2.  Log in using your Account Admin credentials.

        The Roadmunk dashboard opens.

    3.  On the left navigation menu of the Roadmunk dashboard, click your profile icon and then select **Account Settings**.

        Your account settings open.

    4.  On the page header of your account settings, select the **Users** tab.

        This tab displays the complete lists of users on your Roadmunk account, including collaborators, reviewers, and inactive users.

    5.  Click the **Active** toggle button for every user that you want to deactivate.

        You can determine which users you want to deactivate based on the email address that is associated with each user. The email address corresponds directly to the user principal name of each removal candidate that you identified in [step 1](reclaim-roadmunk-subscription.md#identify-removal-candidate).

    6.  Click **Save**.

    The users are deactivated and added to the list of inactive users.

    **Note:** By default, the Roadmunk Download Subscriptions subflow within the ServiceNow SaaS License Management Roadmunk integration downloads all users in your Roadmunk account, including both active and inactive users. To download only the active users in your account, you must download your Roadmunk User Report and then attach it to the Roadmunk integration profile on your ServiceNow instance. See step 7 of [Create a Roadmunk integration profile](../concept/integrate-with-roadmunk.md#) for detailed instructions.

3.  Delete deactivated users from your Roadmunk account.

    If a deactivated user is no longer part of your organization or team, you can delete the user from your Roadmunk account.

    **Warning:** Users are deleted permanently. Proceed with caution, as users cannot be restored once deleted.

    1.  On the same **Users** tab of your Roadmunk account settings, select **INACTIVE USERS**.

        The list of inactive users opens.

    2.  Click the Remove icon \(![Remove icon.](../image/remove-icon.png)\) for the user that you want to delete.

        The removal confirmation dialog box opens.

    3.  On the dialog box, click **Delete**.

        The user is deleted from your account and all roadmaps are unassigned from the user.

        **Note:** The user is not notified about being deleted from your account. Any comments that either mention or are made by the user are updated to indicate that the user has been deleted. All roadmaps that are owned by the user are retained in your account and can be managed by any Account Admin. You can view these roadmaps at any time in the All Roadmaps list on the Roadmaps homepage. If the user is invited back to Roadmunk under the same email address, you must manually reassign these roadmaps to the user.

    4.  Repeat steps b and c for each user that you want to delete.

4.  Return to your ServiceNow instance to update the state of each removal candidate to **Closed Skipped**.

    1.  From your ServiceNow instance, navigate to **SaaS License** &gt; **Administration** &gt; **Direct Integration Profiles**.

    2.  Select your Roadmunk integration profile from the Integration Profiles list.

    3.  On the **Software Models** tab of the Integration Profile form, select the software model that is associated with the integration profile.

    4.  On the Software Model form, select the **Reclamation Candidates** related tab.

    5.  From the list of available removal candidates, select the removal candidate number \(RCCxxxxxxx\) for a user that you deactivated in [step 2](reclaim-roadmunk-subscription.md#remove-user).

    6.  On the Removal Candidate form, update the state of the removal candidate by clicking **Closed Skipped**.

        Software Asset Management removes the user subscription from the Software Subscriptions \[samp\_sw\_subscription\] table and automatically returns you to the Software Model form.

    7.  Repeat steps d through f for each user that you deactivated on your Roadmunk account.


**Parent Topic:**[Reclaim user subscriptions in Software Asset Management classic](reclaim-user-subscription-saas-classic.md)

