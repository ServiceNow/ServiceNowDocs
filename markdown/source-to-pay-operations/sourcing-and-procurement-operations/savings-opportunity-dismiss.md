---
title: Dismiss a savings opportunity
description: Reject a savings opportunity that you do not intend to pursue, recording who dismissed it, when, and why so it stays on record for auditing.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/sourcing-and-procurement-operations/savings-opportunity-dismiss.html
release: zurich
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-05-15"
reading_time_minutes: 2
keywords: [Savings Opportunities, Dismiss, Dismissed reason, sn\_spend\_gen\_ai\_savings\_opportunities]
breadcrumb: [Action or dismiss an opportunity, Using Spend and Savings Management, Use Sourcing and Procurement Operations, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Dismiss a savings opportunity

Reject a savings opportunity that you do not intend to pursue, recording who dismissed it, when, and why so it stays on record for auditing.

## Before you begin

The **Dismiss** option is available only to the user assigned as Spend category manager on the Spend categories table for the opportunity's spend category. A manager assigned to a parent spend category can dismiss opportunities for any of its child categories. The option is hidden for users who do not meet this condition.

Role required: sn\_spend\_mgmt.category\_manager\_admin

## Procedure

1.  From the **Workspaces** tab, select **Source-to-Pay Workspace**.

2.  Select the **Category management** tab.

3.  Do one of the following:

    -   In the Potential savings opportunities section, in the opportunity card you want to dismiss, select the three dots menu, and then select **Dismiss**.

        \[Omitted image "spend-dismiss-learn-more-card.png"\] Alt text: Three dots menu on an opportunity card showing the Dismiss and Learn more options.

    -   In the Potential savings opportunities section, select **View all**. Then, in the Potential Savings Opportunities page, select **Dismiss** for the opportunity you want to dismiss.

        \[Omitted image "spend-dismiss-learn-more.png"\] Alt text: Potential Savings Opportunities page showing the Learn more option on an opportunity card.

4.  In the **Share feedback** modal, select one or more reasons from the checklist.

    At least one reason is required. The available options are:

    -   **Not relevant to my role**
    -   **Already completed**
    -   **Timing isn't right**
    -   **Incorrect analysis**
    -   **Other**
    Optionally, add a comment in the **Add a comment** field to provide more context. You can also chat with Now Assist from this modal to propose changes to the opportunity before dismissing it.

    \[Omitted image "spend-dismiss-output.png"\] Alt text: Share feedback modal showing dismissal reason options.

5.  Select **Submit**.

    The opportunity **Status** moves to **Dismissed**. The **Dismissed reason**, **Dismissed by**, and **Dismissed date** fields are populated. The card is removed from the **Potential Savings Opportunities** page and the **Category Management** tab.

    **Note:** If the dismissal does not process, verify that the sn\_spend\_mgmt.category\_manager\_admin role is assigned and that the opportunity is not in progress.


## Result

The opportunity remains on the Savings Opportunities table with **Status** of **Dismissed** and the dismissal audit fields filled in. The record is not deleted. The dismissal reason is captured as structured agent feedback; subsequent discovery runs consume that feedback to deprioritize patterns that have been rejected and to refine the scoring of future opportunities. When new data materially changes the savings estimate on a dismissed opportunity, the agentic workflow can regenerate it for re-evaluation.

## What to do next

**Note:** If the opportunity still appears on the **Potential Savings Opportunities** page after dismissal, refresh the page. If the issue persists, verify that the **Status** field on the record is set to **Dismissed**.

To reopen a dismissed opportunity, set **Status** back to **Open** in the Savings Opportunities table. The UI policy reverses and hides the dismissal fields, but the previously entered values are retained on the record.

The **Learn more** Now Assist trigger remains available on dismissed records because the trigger's condition only suppresses it for `status = closed`.

**Parent Topic:**[Action or dismiss a savings opportunity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/action-or-dismiss-savings-opportunity.md)

