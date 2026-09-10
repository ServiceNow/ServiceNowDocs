---
title: Resolve friendly fraud disputes
description: Resolve friendly fraud disputes by reviewing evidence, selecting an appropriate action, and communicating with customers. You can use the Help resolve friendly fraud disputes agentic workflow to receive AI-generated recommendations and draft responses.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/dispute-management/resolve-friendly-fraud.html
release: australia
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2026-07-02"
reading_time_minutes: 3
keywords: [friendly fraud, dispute resolution, AI agent, agentic workflow]
breadcrumb: [Investigate, Processing a Visa dispute, Managing disputes integrated with Visa, Processing, Use, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Resolve friendly fraud disputes

Resolve friendly fraud disputes by reviewing evidence, selecting an appropriate action, and communicating with customers. You can use the Help resolve friendly fraud disputes agentic workflow to receive AI-generated recommendations and draft responses.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent or sn\_bom\_credit\_card.dispute\_agent\_connector

## About this task

Friendly fraud occurs when a consumer makes a legitimate purchase but later disputes the transaction, claiming it was unauthorized or that they did not receive the product or service. A set of predefined rules is applied to disputed transactions to detect friendly fraud.

By default, transactions are flagged for friendly fraud if they:

-   Took place with the same merchant.
-   Were conducted using Visa cards.
-   Were made on the same card account.
-   Occur within 120 to 365 days from each other.
-   Have no active fraud reports or disputes.
-   Have at least two matching core data elements \(User ID, IP address, shipping address, device ID/fingerprint\), with one being either IP address or device ID/fingerprint.

You can decline requests, issue credits, or proceed with chargebacks. You can also modify communication templates for customer interaction.

When you enable the Help resolve friendly fraud disputes agentic workflow, the Friendly fraud AI agent provides recommendations and helps draft customer responses. The AI agent provides recommendations to assist your decision-making. AI-generated suggestions may not always be accurate. Review all recommendations carefully and apply your professional judgment before taking action.

The Friendly fraud AI agent has access to the following information:

-   Knowledge base articles
-   Friendly fraud task details
-   Previous dispute cases

You can follow the AI agent's recommendation or make a different decision. If you deviate from the generated suggestion, provide a reason for your decision.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(\[Omitted image "inline-data-vis-96px-list.png"\] Alt text: lists icon\).

3.  In the **Lists** tab under **Card disputes service cases**, open the case list.

    -   For your assigned cases, select **Assigned to me**.
    -   For all dispute cases, select **All**.
4.  In the list, select which case you want to work on.

    If you want to work on a case that isn't assigned to you yet, you can assign it to yourself by selecting **Assign to me**.

5.  Select the **Playbook** tab.

6.  In the **Processing** tab, select the transaction ID in the transaction level playbook.

    The **Investigate** stage is initiated for the transaction.

7.  In the **Investigate** stage, locate the **Detect friendly fraud** activity.

    If friendly fraud is not detected for the transaction, the activity is marked as complete and the form is set to read-only. An information banner indicates that friendly fraud was not detected for this transaction.

8.  Review the transaction details and evidence.

    If the Friendly fraud AI agent is enabled, a notification appears in the ServiceNow Otto panel and an active chat is initiated. The AI agent provides a recommendation for the dispute with a valid reason and guides you to select the appropriate action.

9.  Select one of the following resolution options.

    If you are working with the AI agent, enter the number corresponding to your decision in the chat. Otherwise, select an option directly on the form.

<table id="choicetable_z24_15n_52c"><thead><tr><th align="left" id="d110311e259">

Action

</th><th align="left" id="d110311e262">

Result

</th></tr></thead><tbody><tr><td id="d110311e268">

**Decline dispute transaction**

</td><td>

1.  Provide the reason for the decline and select **Mark Complete**.
2.  The **Customer communication** activity is displayed. See [Resolve fraud customer communication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/resolve-fraud-customer-communication.md).


</td></tr><tr><td id="d110311e299">

**Issue credit and write-off**

</td><td>

1.  Provide the **Resolution reason**.
2.  Select **Mark complete**. The **Issue credit** activity is displayed.
3.  Provide the final credit and select **Close task**. The task is marked as **Closed Complete**.


</td></tr><tr><td id="d110311e335">

**Proceed with dispute**

</td><td>

The **Report fraud** activity is displayed. See [Report fraud to card network](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/report-fraud-to-card-network.md).

</td></tr></tbody>
</table>10. If you are working with the AI agent, continue interacting with it as needed to resolve the case.

    You can continue working in the playbook activities as you interact with the AI agent.


## Result

Based on your selected resolution option, the friendly fraud dispute is resolved and the case proceeds to the next activity.

**Parent Topic:**[Investigate stage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/investigate-stage.md)

