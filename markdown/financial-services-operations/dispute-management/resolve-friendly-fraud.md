---
title: Detect friendly fraud
description: Detect friendly fraud and determine the course of action required depending on the amount being disputed, the customer relationship, and the outcome of the detection logic. The Friendly fraud AI agent can be enabled as part of the Help resolve friendly fraud disputes agentic workflow. The agent recommends an action and helps draft the customer response.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/dispute-management/resolve-friendly-fraud.html
release: australia
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2026-07-02"
reading_time_minutes: 4
breadcrumb: [Investigation, Resolving disputes without network integration, Processing, Use, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Detect friendly fraud

Detect friendly fraud and determine the course of action required depending on the amount being disputed, the customer relationship, and the outcome of the detection logic. The Friendly fraud AI agent can be enabled as part of the Help resolve friendly fraud disputes agentic workflow. The agent recommends an action and helps draft the customer response.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent or sn\_bom\_credit\_card.dispute\_agent\_connector

## About this task

Friendly fraud occurs when a consumer makes a legitimate purchase but later disputes the transaction, claiming it was unauthorized or that they didn't receive the product or service. To detect friendly fraud accurately, a set of predefined rules is applied to disputed transactions.

By default, transactions are flagged for friendly fraud if they:

-   Took place with the same merchant.
-   Were conducted using Visa cards.
-   Were made on the same card account.
-   Occur within 120 to 365 days from each other.
-   Have no active fraud reports or disputes.
-   Have at least two matching core data elements \(User ID, IP address, shipping address, device ID/fingerprint\), with one being either IP address or device ID/fingerprint.

The dispute agent can decline requests, issue credits, or proceed with chargebacks, along with modifying communication templates for customer interaction.

Dispute agents can also use the Help resolve friendly fraud disputes agentic workflow to provide suggested actions and draft customer responses. This agentic workflow detects friendly fraud through automated checks, guides the dispute agent toward appropriate actions, and helps draft responses for customers.

When this agentic workflow is enabled, the Friendly fraud AI agent has access to:

-   **Tools**: The agent has access to various tools, including:
    -   Knowledge base \(KB\) articles
    -   Friendly fraud task details
    -   Previous cases of disputes
-   **Decision Making**: The dispute agent can follow a generated recommendation of the AI agent or make a different decision. If the dispute agent decides to deviate from the generated suggestion, they must provide a reason for their decision. The process includes declining requests, issuing credits, or proceeding with chargebacks, and communication templates for customer interaction.

For information on modifying the agentic workflow, see [Configure agentic workflows in Financial Services Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/configuring-agentic-workflows-in-fso.md).

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(\[Omitted image "inline-data-vis-96px-list.png"\] Alt text: lists icon\).

3.  In the **Lists** tab under **Card disputes service cases**, open the case list.

    -   For your assigned cases, select **Assigned to me**.
    -   For all dispute cases, select **All**.
4.  In the list, select which case you want to work on.

    If you want to work on a case that isn't assigned to you yet, you can assign it to yourself by selecting **Assign to me**.

5.  Select the **Playbook** tab.

6.  Select the transaction ID in the transaction level playbook of the **Processing** tab.

    The **Investigate** stage is initiated for the transaction.

7.  The **Detect friendly fraud** activity appears in the **Investigate** stage.

    If friendly fraud is not detected for the transaction, the activity is marked as complete. The form is set to read-only and an information banner indicates that friendly fraud was not detected for this transaction.

8.  The transaction details along with the **Evidence** are displayed.

    If the Friendly fraud AI agent is enabled, a notification appears in the ServiceNow Otto panel and an active chat is initiated. The AI agent provides a recommendation for the dispute along with a valid reason. It guides the dispute agent in the panel to select the appropriate action and provide the reasons for the selection.

9.  If the Friendly fraud AI agent is enabled, select the ServiceNow Otto icon \(\[Omitted image "icon-otto.png"\] Alt text: Otto icon.\) and open the active chat for the disputed transaction.

    In the chat, the AI agent generates a recommendation for the dispute with a valid reason. A new section appears with the AI-driven recommendation in the **Resolve friendly fraud** activity.

10. Perform one of the following actions:

    -   If you're working with the AI agent, in the chat, enter the number corresponding to your decision.
    -   If you're not working with the AI agent, select one of the following options directly on the form.
<table id="choicetable_z24_15n_52c"><thead><tr><th align="left" id="d110353e306">

Action

</th><th align="left" id="d110353e309">

Result

</th></tr></thead><tbody><tr><td id="d110353e315">

**Decline dispute transaction**

</td><td>

1.  Provide the reason for the decline and select **Mark Complete.**
2.  The next activity **Customer communication** is displayed. See [Manage customer communication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/resolve-fraud-customer-communication.md).


</td></tr><tr><td id="d110353e345">

**Issue credit and write-off**

</td><td>

1.  Provide the **Resolution reason**.
2.  Select **Mark complete**.

The **Issue credit** activity is displayed.

3.  Provide the final credit and select **Close task**. The task is marked as **Closed Complete.**
.

</td></tr><tr><td id="d110353e381">

**Proceed with dispute**

</td><td>

The **Report fraud** activity is displayed. Follow the further steps to resolve the fraud. For more information, see [Report fraud to a card network](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/report-fraud-to-card-network.md).

</td></tr></tbody>
</table>11. If you're working with the AI agent, continue interacting with it as needed to resolve the case.

    You can continue working in the playbook activities as you interact with the AI agent. For information about resolving customer communication for friendly fraud, see [Manage customer communication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/resolve-fraud-customer-communication.md).


## Result

Based on the resolution option selected, either directly on the form or through the Friendly fraud AI agent chat, the friendly fraud is resolved. The case proceeds to the next activity.

**Parent Topic:**[Investigating a dispute](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/investigate-a-dispute.md)

