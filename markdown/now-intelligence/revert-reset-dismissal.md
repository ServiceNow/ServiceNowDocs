---
title: Revert baseline reset or signal dismissal
description: Review previous decisions to reset the KPI Signals baseline or dismiss a signal. Revert the decision if necessary.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/now-intelligence/revert-reset-dismissal.html
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use, KPI Signals, Platform Analytics experience, Platform Analytics]
---

# Revert baseline reset or signal dismissal

Review previous decisions to reset the KPI Signals baseline or dismiss a signal. Revert the decision if necessary.

## Before you begin

You must have access to KPI Details.

Role required: You must be a responsible user for the KPI, or have the admin, pa\_admin, or pa\_kpi\_signal\_admin role.

## Procedure

1.  From KPI Details, open the KPI Signals panel.

2.  Switch to the **Past** tab.

    \[Omitted image "kpi-signals-past.png"\] Alt text: KPI Signals panel in KPI Details, focused on the Past tab

3.  To focus on a baseline reset or a signal dismissal, click the card for that decision.

    You can also point to the callout for a signal to see the reason for its dismissal or for the baseline reset.\[Omitted image "kpi-signals-past-focus.png"\] Alt text: KPI Signals focusing on a past baseline reset

    **Note:** You cannot revert an anti-signal.

4.  If you determine that an earlier decision to dismiss a signal or reset a baseline was incorrect, click **Revert**.

5.  Review the list of all decisions that you would revert.

    When you revert a signal dismissal or baseline reset, you also revert all later decisions.\[Omitted image "kpi-signals-reverted-decisions.png"\] Alt text: List of decisions that would be reverted

6.  If you decide to proceed with reverting the decisions, click **Confirm**.


## What to do next

Now make a new decision for the oldest signal whose decision you reverted. Then work your way through any subsequent signals.

**Parent Topic:**[Using KPI Signals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/using-kpi-signals.md)

