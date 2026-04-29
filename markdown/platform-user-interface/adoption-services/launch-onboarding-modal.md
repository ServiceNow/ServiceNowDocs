---
title: Launch an Onboarding Modal
description: Launch an Onboarding Modal you have created in your instance.
locale: en-US
release: australia
product: Adoption Services
classification: adoption-services
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Onboarding modals, Adoption services, Configure user experiences]
---

# Launch an Onboarding Modal

Launch an Onboarding Modal you have created in your instance.

## Before you begin

Role required: admin

## Procedure

1.  To launch an Onboarding modal once created, do the following:

2.  Create a client script in UIB.

3.  Under code snippet enter `api.emit('SN_HELP#GUIDANCE_START_REQUESTED',{guidanceId:"ID"});`

4.  Replace the ID with the sys\_ID of the modal guidance to be opened.

5.  Save the page.

6.  Select **Body** in the left panel of the UIB page.

7.  In the right panel, select the **Events** tab.

8.  Under **Dispatched Events** select **Add**.

9.  In the event name, add `SN_HELP#GUIDANCE_START_REQUESTED` and give the label with a name.

10. Select **Save**.


**Parent Topic:**[Configure](../concept/configure-onboarding-modals.md)

