---
title: Defining Security Control Lists
description: Use this feature to add or remove observables in bulk.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [About Security Control Lists in TISC, Administer, Threat Intelligence Security Center, Security Operations]
---

# Defining Security Control Lists

Use this feature to add or remove observables in bulk.

## Before you begin

Role required: sn\_sec\_tisc.admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center** &gt; **Administration**.

2.  Go to **Security Control Lists**.

    For example, adding observables to allow list then go to Allow list option.

3.  Select **Allow List**.

4.  Select the Observables type such as IP Address, File and so on to add to the allow list.

5.  Click **Add**.

    The **Select Observables For Allow list** is displayed.

6.  Select all those observables that are required to be added to the allow list.

7.  Click **Add to Allow List**.

    The selected observables are added.

8.  Similarly, select **Add to Deny list** to add the observables to the removed list.

9.  Select **Add to Watch list** to add the observables to the watch list.

    **Note:** You can directly add the observables to allow list, deny list, or watch list directly from the Observables form view page, which are available above the form banner.

10. To verify, navigate to **Threat Intel Library**.

11. Select the observable type that was added to the allow list.

    The observable is indicated as added to allow list.

    **Note:** Allow list and deny list are mutually exclusive and the system will automatically ensure that an observable in allow list is not part of deny list and vice-versa.


