---
title: Purchase a Boomi plan
description: Purchase a Boomi plan with fabric credits to add connections and transactions to your Boomi account.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/integrate-applications/purchase-boomi-plan.html
release: australia
topic_type: task
last_updated: "2026-10-23"
reading_time_minutes: 2
keywords: [Boomi, purchase, fabric credits, Partner Passport Portal]
breadcrumb: [Boomi partner application, Partner Passport Portal, Workflow Data Fabric]
---

# Purchase a Boomi plan

Purchase a Boomi plan with fabric credits to add connections and transactions to your Boomi account.

## Before you begin

Complete the setup steps. For more information, see [Set up Boomi access in Partner Passport Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/set-up-boomi-access.md).

Role required: sn\_wdf\_token.wdf\_admin

## About this task

When you confirm a purchase, the fabric credit amount is blocked immediately, and it can't be refunded or canceled. This helps prevent the same credits from being used for another purchase. Each purchase is for one plan. To purchase more, make another purchase.

The deduction and the corresponding balance update take up to 48 hours to appear in the portal.

You can purchase a plan again at any time. Purchasing the plan that you have again adds transactions but not connections. Purchasing a higher plan adds transactions and raises your connection limit to that plan's limit.

## Procedure

1.  Navigate to **All** &gt; **Workflow Data Fabric Usage** &gt; **Partner Passport**.

2.  On the **Partner Applications** tab, on the Boomi card, select **Get started**.

    If you've already purchased a plan, select **Manage plan** instead.

3.  In the **Purchase** step, select a plan.

    The **Summary** panel shows your credit balance, the plan you selected, its credit cost, and your balance after the purchase.

    \[Omitted image "partner-portal-purchase.png"\] Alt text: Choose your plan screen showing Boomi Starter and Boomi Growth plan options with a Summary panel displaying credit balance and cost

4.  Select the check box to confirm that you understand the fabric credits can't be refunded or canceled.

5.  Select **Confirm purchase**.

    If your balance doesn't cover the plan cost, **Confirm purchase** isn't available, and the **Summary** panel shows the amount that you're short.

    A dialog confirms the purchase and shows the plan, the credits used, and the credits remaining.

    \[Omitted image "partner-portal-purchase-confirm.png"\] Alt text: Plan purchased confirmation dialog showing the Boomi Growth plan details, credits consumed, and credits remaining

6.  Select **Done**.

    The **Purchase** step shows that the purchase is confirmed and that the plan is provisioned within 48 hours, with a link to the Boomi capacity update article. The order summary shows the plan purchased, the fabric credits spent and remaining, and the order date.

7.  Select **Mark as complete**.

    The portal opens on the **Partner Applications** tab, and **Available credits** shows your new balance.


## Result

The purchase is recorded in the [purchase log](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/view-partner-passport-portal-purchase-logs.md) immediately. The purchase log is the source of truth for all transactions. Your available credit balance may take up to 48 hours to reflect the deduction.

Boomi adds the plan's capacity to your account and sends an email when it's added. The plan's 365-day validity starts on that date. For details on capacity updates, validity, and expiration, see the [Boomi capacity update article \[KB3225968\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=kb3225968).

**Parent Topic:**[Boomi partner application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/manage-boomi-plans.md)

