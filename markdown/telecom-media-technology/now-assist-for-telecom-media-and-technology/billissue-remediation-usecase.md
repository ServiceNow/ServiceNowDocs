---
title: Now Assist for Telecommunications, Media and Technology \(TMT\) AI agent collection Help remediate bill issues agentic workflow
description: Use the Help remediate bill issues agentic workflow to handle the billing inquiry case requests and recommend better plans based on the customer usage.
locale: en-US
release: australia
product: Now Assist for Telecom, Media and Technology
classification: now-assist-for-telecom-media-and-technology
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Customer Service Problem Management, Use agentic workflows, Now Assist for TMT, Telecommunications, Media, and Technology \(TMT\)]
---

# Now Assist for Telecommunications, Media and Technology \(TMT\) AI agent collection Help remediate bill issues agentic workflow

Use the Help remediate bill issues agentic workflow to handle the billing inquiry case requests and recommend better plans based on the customer usage.

## Help remediate bill issues agentic workflow overview

The Help remediate bill issue agentic workflow uses a team of AI agents that support the resolution of customer issues. It can handle task requests to retrieve the account details, current invoices, and past invoices. It analyzes the data to identify reasons for high bill usage and recommends better plans based on customer usage patterns.

Role required: sn\_tmt\_agentic\_ai.telco\_billing\_inquiry\_case\_agent

To modify the Help remediate bill issues agentic workflow, Duplicate an agentic workflow, and adjust the settings according to your requirements.

**Important:** In the Edit trigger form, make sure that the **Active** button is turned on to enable the AI agent to trigger autonomously.

## Role masking

Required role: sn\_tmt\_agentic\_ai.telco\_billing\_inquiry\_case\_agent

Agentic workflows and their AI agents use role masking to determine which users can access them. Ones installed with Now Assist applications have specific roles that come included with the application. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. For the instructions to change the security controls, see Define security controls for an agentic workflow.

## Help remediate bill issues agentic workflow

To access the use case:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Help remediate bill issues**.

To create a new use case, see Create an agentic workflow.

## Application dependency

The Help remediate bill issues agentic workflow has the following dependencies:

-   Case Management for Invoice operations \(com.sn\_csm\_invoice\)
-   Product offering recommendations

To configure the spoke selector, see [Configure the spoke selector for external systems](../task/configure-spoke-selector-for-external-systems.md).

## Testing the agentic workflow

To access the use case testing page:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Testing**.
2.  On the Overview page, select **Test use cases**.

To test the agentic workflow, see Manually test the execution of an agentic workflow.

## AI agents used in the Help remediate bill issues agentic workflow

The following AI agents are used to execute the instructions for the agentic workflow.

To create an AI agent, see Create an AI agent.

<table id="table_kw1_skx_r2c"><thead><tr><th>

AI agent

</th><th>

AI agent role

</th></tr></thead><tbody><tr><td>

Billing account information collector AI agent

</td><td>

This AI agent is designed to handle billing inquiries by following a structured approach.

 It retrieves the billing inquiry case details and obtains the billing account details using the account number.

 The agent is intended for use by ServiceNow agents for getting the billing account number.

</td></tr><tr><td>

Recommended plans AI agent

</td><td>

This AI agent is designed to facilitate the generation and confirmation of service plan recommendations through a structured approach.

 It follows these instructions: 1.  Generates a recommended plan.
2.  Shows the recommended plan to the user for confirmation.
3.  Verifies whether an email is associated with the customer account.
4.  Triggers the email notification agent to send the recommended plan details to the user.

</td></tr><tr><td>

Billing invoice data collector AI agent

</td><td>

This AI agent collects the billing invoice data like account details, invoice history, and invoice details.

</td></tr></tbody>
</table>