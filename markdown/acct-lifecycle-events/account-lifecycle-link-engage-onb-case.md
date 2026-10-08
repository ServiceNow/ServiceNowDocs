---
title: Link an engagement to an onboarding case
description: Link an engagement to an additional onboarding case on the same account to track all onboarding work for the engagement in one place.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/acct-lifecycle-events/account-lifecycle-link-engage-onb-case.html
release: brazil
topic_type: task
last_updated: "2026-09-30"
reading_time_minutes: 1
keywords: [link onboarding case, engagement onboarding links, engagement, onboarding case]
breadcrumb: [Engagement onboarding links, Manage engagements, Customer success, Use, Customer Success Management]
---

# Link an engagement to an onboarding case

Link an engagement to an additional onboarding case on the same account to track all onboarding work for the engagement in one place.

## Before you begin

-   The engagement and the onboarding case must already exist and belong to the same account.
-   Role required: sn\_acct\_lc.agent

## About this task

Use engagement onboarding links when one engagement covers more than one onboarding case. You can start from either record. For background, see [Engagement onboarding links](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/acct-lifecycle-events/account-lifecycle-engage-onb-links.md).

**Note:** Users with the `sn_acct_lc.customer_success_viewer` role can view links but can't create them.

## Procedure

1.  Open the record to start from.

    -   To start from an engagement, open the engagement record. See [Engagement home page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/acct-lifecycle-events/account-lifecycle-view-engage.md) for details
    -   To start from an onboarding case, open the onboarding case in the Account Onboarding Workspace view.
2.  Find the **Engagement Onboarding Links** related list.

    In the contextual side panel, select the **Related Items** tab and expand **Engagement Onboarding Links**.

3.  Select **Create**.

4.  On the form, select the other record to link.

    The record that you started from is already filled in and is read-only.

    -   If you started from an engagement, select the onboarding case in the **Onboarding Case** field.
    -   If you started from an onboarding case, select the engagement in the **Engagement** field.
    The list shows only active records on the same account that aren't already linked to the record you started from.

5.  Save the record.

    The link appears in the **Engagement Onboarding Links** related list on both the engagement and the onboarding case.


**Parent Topic:**[Engagement onboarding links](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/acct-lifecycle-events/account-lifecycle-engage-onb-links.md)

