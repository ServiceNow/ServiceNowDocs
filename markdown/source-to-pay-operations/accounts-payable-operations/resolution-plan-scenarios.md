---
title: Resolution plan scenarios
description: The Recommend invoice owner AI agent handles different scenarios when resolving Missing or invalid business owner exceptions. For each scenario, the AI agent recommends a resolution plan based on historically processed invoices and supplier information.
locale: en-US
release: yokohama
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: reference
last_updated: "2025-11-11"
reading_time_minutes: 1
keywords: [AI agent, Now Assist]
breadcrumb: [Recommend invoice owner AI agent, Using AI agents in Now Assist for Accounts Payable Operations, Now Assist for Accounts Payable Operations \(APO\), Accounts Payable Operations, Finance and Supply Chain]
---

# Resolution plan scenarios

The Recommend invoice owner AI agent handles different scenarios when resolving Missing or invalid business owner exceptions. For each scenario, the AI agent recommends a resolution plan based on historically processed invoices and supplier information.

For information on using the Recommend invoice owner AI agent, see [Use Recommend invoice owner AI agent](../task/use-recommend-invoice-owner-ai-agent.md).

<table id="table_l45_wws_ghc"><thead><tr><th>

No

</th><th>

Scenario

</th><th>

Resolution plan

</th></tr></thead><tbody><tr><td>

1

</td><td>

No historically processed invoices exist in the system

</td><td>

The Recommend invoice owner AI agent suggests reaching out to the existing supplier contact. If the accounts payable specialist opts to reach out to supplier contact, a task is created and assigned to the supplier contact.

</td></tr><tr><td>

2

</td><td id="single">

Single historical owner found in the system

</td><td>

The Recommend invoice owner AI agent prompts whether to assign the historical business owner. On confirmation, the AI agent updates the business owner on the invoice and changes the exception status to Review complete.

However, if the [automatic assignment property](../concept/configuring-bo-prediction-settings.md#automatic) is set to true, the business owner is assigned and no confirmation is needed.

</td></tr><tr><td>

3

</td><td id="multiple">

Multiple historical owners found in the system

</td><td>

The Recommend invoice owner AI agent uses the score calculated by the [Relevant invoice finder skill](../concept/exploring-now-assist-apo.md#invoice-finder). If the scores of all business owners is less than the threshold, the agent suggests creating a task for the last known business owner.

 On confirmation, the AI agent creates and assigns the exception task to the last known business owner.

 If the scores of all business owners is above the threshold, the AI agent follows the [single historical owner process](resolution-plan-scenarios.md#single) after selecting the business owner:

-   If a business owner has the highest score, the AI agent selects that owner.
-   If multiple business owners tie for the highest score, the AI agent selects the most recent owner.

</td></tr></tbody>
</table>