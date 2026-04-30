---
title: Reclaim monday.com user subscriptions in Software Asset Management classic
description: Reclaim unused monday.com subscriptions to reduce your total software costs.
locale: en-US
release: zurich
product: SaaS License Management
classification: saas-license-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Reclaim user subscriptions in Software Asset Management classic, Reclaiming user subscriptions, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Reclaim monday.com user subscriptions in Software Asset Management classic

Reclaim unused monday.com subscriptions to reduce your total software costs.

## Before you begin

monday.com Role required: admin

ServiceNow Role required: sam\_user

## About this task

The SaaS License Management monday.com integration doesn’t support reclamation through the ServiceNow AI Platform. When Software Asset Management creates a removal candidate for your monday.com integration, you can reclaim the user subscription by deactivating the associated user on your monday.com account. After you deactivate the user, you must update the state of the removal candidate to **Closed Skipped** so that the user subscription is removed from the Software Subscriptions \[samp\_sw\_subscription\] table.

## Procedure

1.  Identify removal candidates for your monday.com integration.

    1.  From your ServiceNow instance, navigate to **All** &gt; **Software Asset** &gt; **SaaS License** &gt; **Direct Integration Profiles**.

    2.  Select your monday.com integration profile from the Integration Profiles list.

    3.  On the **Software Models** tab of the Integration Profile form, select the software model that is associated with the integration profile.

    4.  On the Software Model form, select the **Reclamation Candidates** related tab to view the list of available removal candidates.

    5.  Take note of the user principal name for each removal candidate that you want to reclaim the user subscription for.

        Save this information for later use.

2.  Deactivate the associated users on your monday.com account.

    Based on the list of removal candidates that you identified in [step 1](reclaim-monday-subscription.md#identify-removal-candidate), you can reclaim user subscriptions by deactivating the associated users on your monday.com account.

    1.  From a web browser, go to [monday.com](https://monday.com/).

    2.  Log in using your admin credentials.

    3.  At the bottom of the left navigation menu, select your profile icon and then select **Admin**.

        The Admin section opens.

    4.  In the Admin section, select **Users**.

        The **Users** tab of the Users subsection opens. This tab displays the complete list of users on your monday.com account.

    5.  From the list of users, select the ellipsis icon \(…\) for the user that you want to deactivate.

        You can identify which user you want to deactivate based on the associated user name or email address. The user name or email address corresponds directly to the user principal name of each removal candidate that you identified in [step 1](reclaim-monday-subscription.md#identify-removal-candidate).

    6.  When prompted, select **Deactivate user**.

    7.  Repeat steps e and f for each user that you want to deactivate.

3.  Return to your ServiceNow instance to update the state of each removal candidate to **Closed Skipped**.

    1.  From your ServiceNow instance, navigate to **SaaS License** &gt; **Administration** &gt; **Direct Integration Profiles**.

    2.  Select your monday.com integration profile from the Integration Profiles list.

    3.  On the **Software Models** tab of the Integration Profile form, select the software model that is associated with the integration profile.

    4.  On the Software Model form, select the **Reclamation Candidates** related tab.

    5.  From the list of available removal candidates, select the removal candidate number \(RCCxxxxxxx\) for a user that you deactivated in [step 2](reclaim-monday-subscription.md#remove-user).

    6.  On the Removal Candidate form, update the state of the removal candidate by selecting **Closed Skipped**.

    7.  Close the **Removal Candidate** tab.

4.  Verify the user deletion from the monday.com portal.

    1.  Run the **Refresh Monday.com subscriptions** scheduled job.

    2.  Verify the user deletion in the Software Subscriptions \[samp\_sw\_subscription\] table.


**Parent Topic:**[Reclaim user subscriptions in Software Asset Management classic](reclaim-user-subscription-saas-classic.md)

