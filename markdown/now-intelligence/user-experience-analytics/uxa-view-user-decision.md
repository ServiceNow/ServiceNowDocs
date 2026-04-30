---
title: View users’ consent tracking selections
description: View and analyze details regarding users and their tracking selection preferences.
locale: en-US
release: zurich
product: User Experience Analytics
classification: user-experience-analytics
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [How users consent to tracking in User Experience Analytics, User privacy, tracking, and consent, Configure, User Experience Analytics, Platform Analytics]
---

# View users’ consent tracking selections

View and analyze details regarding users and their tracking selection preferences.

## Before you begin

Role required: analytics\_admin

## Procedure

1.  Navigate to **All**.

2.  In the navigator, enter `sys_analytics_user_consent_decision.list` to open the User Experience Analytics User Consent Decisions page.

3.  Review the data that applies to your users’ tracking selections.

    The table also includes the detection policy provider and the date of the migration from the deprecated table \[m2m\_user\_consent\_info\].

    **Note:** When a user either explicitly consents to or opts out of advanced tracking through the **Explicit Opt-In** or **Notice** modal window, or if they manually update their tracking preference, a corresponding record is created or updated in the sys\_analytics\_user\_consent\_decision table. This record is only created if it doesn't already exist. However, a record is not created if a user doesn't actively select an advanced tracking preference. This can happen, for instance, when a **No Consent Required** policy is assigned to a user and they don't manually adjust their tracking preference within the application.

    Users who fall under an **Explicit Opt-In** or **Notice** consent policy, they receive an annual opt-in or notice message based on the date set in the User Consent Decision record.

    See [How users consent to tracking in User Experience Analytics](user-exp-analytics-user-set.md) for information on how users manually update their preference.


**Parent Topic:**[How users consent to tracking in User Experience Analytics](user-exp-analytics-user-set.md)

