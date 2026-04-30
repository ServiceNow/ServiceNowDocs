---
title: Close or cancel an account onboarding case
description: You can close or cancel an account boarding case and all the related activities.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Set up playbook, Account onboarding, Configure, Customer Success Management]
---

# Close or cancel an account onboarding case

You can close or cancel an account boarding case and all the related activities.

## Before you begin

Role required: sn\_acct\_lc.agent

## Procedure

1.  Navigate to **Workspace** &gt; **CSM/FSM Configurable Workspace** and select the **List** icon.

2.  Navigate to the **Customer Success** &gt; **All Onboarding Cases** and open the onboarding case you want to cancel.

3.  Select the **Record details** to view the account onboarding case form.

4.  To cancel the account onboarding case, follow these steps:

    -   Change the State to **Canceled**. A pop-up message asking to confirm the cancellation is displayed. Select **Yes** to confirm. The Resolution code is automatically updated to `Voided/Canceled`.
    -   Verify that all the required fields are filled out and select **Save**. The account onboarding case is canceled.
5.  To close the account onboarding case, follow these steps:

    -   Change the State to **Closed**.
    -   Select the Resolution code from the drop-down list:
        -   Successful - No issues
        -   Successful - With issues
        -   Unsuccessful - Unable to complete
        -   Voided/Canceled
    -   Confirm that the rest of the required fields are filled out and select **Save**. The account onboarding case is canceled.

        **Note:** Before you close an account onboarding case, you must close or cancel or the related account onboarding case tasks. If an associated child task is still open, a warning message is displayed. You must first close or cancel the child tasks and then proceed with closing the account onboarding case.


**Parent Topic:**[Set up the account onboarding playbook](../concept/account-lifecycle-use-playbook.md)

