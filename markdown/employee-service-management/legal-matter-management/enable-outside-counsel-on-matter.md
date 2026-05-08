---
title: Enable the option to engage with outside counsel for a matter
description: Enable legal fulfiller to submit requests for outside counsel engagements for a matter.
locale: en-US
release: australia
product: Legal Matter Management
classification: legal-matter-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure Legal Matter Management with outside counsel, Configure, Legal Matter Management, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Enable the option to engage with outside counsel for a matter

Enable legal fulfiller to submit requests for outside counsel engagements for a matter.

## Before you begin

-   Ensure you have installed and activated Legal Tracker spoke. For more information, see Legal Tracker.

    **Important:** After setting up the spoke, give the Legal Tracker Spoke user \[sn\_legal\_trckr\_spk.user\] role to users accessing Legal Tracker

-   Ensure you have selected Practice Areas intake forms where the record type is either of the following:
    -   Matter
    -   Request and Matter
-   Ensure you have added details for the outside counsels and approval route. For more information, see [Add outside counsel details](lmm-lt-setup-outside-counsels.md) and [Add approval route details](lmm-lt-setup-approval-route.md).

Role required: sn\_lg\_ops.legal\_config

## About this task

While working on matters, you may want to engage with outside counsel to get additional services. You can submit a request to engage with the outside counsel. To view the **Add outside counsel for Legal Tracker** option in a legal matter, you must enable Outside Counsel on Matter for the Practice Areas.

## Procedure

1.  Navigate to **All** &gt; **Legal Administration** &gt; **Practice Areas**.

2.  Select a record from the list of Practice Areas.

3.  Select the intake form from the **Intake Forms** tab.

4.  In the information message at the top of the page about the current application, select **here** to be able to edit the form.

5.  Select the Unlock Options icon ![Unlock Options icon.](../../legal-request-management/image/lock.png) in the **Options** field in the Record Producer section.

6.  Enter `Enable` in the **Select target record** field.

7.  Select **Enable Outside Counsel on Matter** from the list.

8.  Select **Update**.


## Result

The **Add Outside Counsel for Legal Tracker** button is available in the **Outside Counsel** tab of a matter. Users with the matter fulfiller role and access to update matters can submit Outside Counsel Engagement for Legal Tracker. This option is applicable only for matter and not for requests.

**Parent Topic:**[Configure Legal Matter Management to engage with outside counsel using Legal Tracker](../concept/configurations-for-legal-tracker-integration.md)

