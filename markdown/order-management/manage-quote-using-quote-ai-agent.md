---
title: Manage quotes using the Quote AI Agent
description: Use the Quote AI Agent to create a quote, modify an existing quote, or review a quote that the agent generated automatically from a trigger condition.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/manage-quote-using-quote-ai-agent.html
release: australia
topic_type: task
last_updated: "2026-07-07"
reading_time_minutes: 3
breadcrumb: [Use, Now Assist for CPQ, Sales Customer Relationship Management]
---

# Manage quotes using the Quote AI Agent

Use the Quote AI Agent to create a quote, modify an existing quote, or review a quote that the agent generated automatically from a trigger condition.

## Before you begin

Role required: sales\_agent

## About this task

The Quote AI Agent supports three operations on quotes. Choose the operation that matches your goal.

-   **Create**—Ask the agent to build a new quote for an opportunity. The agent retrieves the opportunity line items, builds the quote, and presents it for your review. If a primary quote already exists, the agent uses it. If no primary quote exists, the agent creates one.
-   **Modify**—Ask the agent to update an existing open quote. The agent interprets your request, applies the changes, and checks that all discounts and pricing conform to company policies.
-   **Trigger-generated**—Review a draft quote that the agent created automatically when a trigger condition was met on an opportunity, for example when the opportunity stage is set to **Propose** or when a task or note contains a recognized keyword. The agent notifies you through Microsoft Teams and Now Assist for CPQ when the draft is ready.

If a change requires approval, the agent notifies you and starts the approval workflow. If the agent can't find enough information to continue, it sends you a message asking for the missing details.

## Procedure

1.  Open the starting point for your operation.

    |Operation|Starting point|
    |---------|--------------|
    |**Create a quote**|Open the opportunity for which you want to create a quote.|
    |**Modify a quote**|Open the quote you want to modify, or open the linked opportunity.|
    |**Review a trigger-generated quote**|Open the notification from the Quote AI Agent in Microsoft Teams or Now Assist for CPQ, then open the opportunity linked in the notification.|

2.  Open the Now Assist for CPQ chat panel.

3.  Enter your request or respond to the agent, depending on your operation.

<table><thead><tr><th align="left" id="d79223e138">

Operation

</th><th align="left" id="d79223e141">

What to do

</th></tr></thead><tbody><tr><td id="d79223e147">

**Create a quote**

</td><td>

Enter your request in the chat, including the opportunity number and any pricing instructions.

 Example requests:

 -   `Create a quote for Opportunity OPT001 with a 10% discount on Visibility.`
-   `Help me create a quote for Opportunity 123.`
-   `Create a quote for Opportunity OPT001 and generate an email with the document.`


</td></tr><tr><td id="d79223e177">

**Modify a quote**

</td><td>

Enter your modification request in the chat, including the quote number and the change you want to make.

 Example requests:

 -   `For this quote, apply a 10% discount to all products.`
-   `Remove the Visibility line item from quote QT001.`
-   `Update the quantity for Standard on quote QT001 to 50.`
-   `Change the price list on this quote to the EMEA price list.`


</td></tr><tr><td id="d79223e211">

**Review a trigger-generated quote**

</td><td>

Review the draft quote that the agent created, including the products, quantities, and pricing. The agent populates the quote from the opportunity line items and may suggest related or recommended products based on the opportunity data.

 If the agent has sent a message asking for missing information, reply in the chat with the details requested. This applies when no opportunity line items exist and no product information is available in the opportunity notes or tasks.

</td></tr></tbody>
</table>4.  Review the summary that the agent presents.

    For a new or trigger-generated quote, the agent shows line items, pricing, and any discounts applied. For a modification, the agent identifies the relevant quote line items by product name and shows you the proposed changes before applying them. If the agent needs more information, it sends you a message before continuing.

5.  Confirm the details or provide additional instructions.

    -   To add products, tell the agent which products to include.
    -   To remove products, tell the agent which products to exclude.
    -   To apply or change a discount, specify the discount amount or percentage and the products it applies to.
    -   To change pricing, ask the agent to update the price list or individual line item prices.
    -   To accept or apply the changes as shown, confirm your approval in the chat.
6.  If the agent notifies you that a discount or pricing change requires approval, wait for the approval workflow to complete before continuing.

7.  Ask the agent to generate the quote document and draft the client email.

    Example: `Generate the quote document and prepare an email for the customer.`

    This step applies when creating a new quote or finalizing a trigger-generated quote. Skip this step if you're only updating an existing quote and don't need to send a new document.

8.  Review the draft email and send it to the customer.


## Result

The quote is created, updated, or finalized and attached to the opportunity. The agent updates the opportunity work notes with a summary of the actions taken and notifies you through Microsoft Teams and Now Assist for CPQ.

