---
title: Customer 360 page for Agentic Contact Center for Banking
description: The Customer 360 page provides customer service representatives \(CSRs\) with an AI-enhanced, comprehensive view of a customer's profile, financial standing, account details, transaction history, and service cases.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Explore, Agentic Contact Center for Banking, Banking applications, Financial Services Operations \(FSO\)]
---

# Customer 360 page for Agentic Contact Center for Banking

The Customer 360 page provides customer service representatives \(CSRs\) with an AI-enhanced, comprehensive view of a customer's profile, financial standing, account details, transaction history, and service cases.

This page gives CSRs a unified view of a customer's relationship. CSRs can open it by selecting the customer's name from the Interaction page contact card, or navigate to it directly when reviewing a customer outside of a call.

The page opens in a separate tab. It supports both retail \(B2C\) consumer profiles and commercial \(B2B\) account profiles, with the page layout adapting dynamically to reflect the customer type.

**Note:** When viewing the page for an account's primary contact, a variant of the page displays the details of the associated account. No AI elements are displayed on this page.

![Customer 360 view showing account details, interaction history, and financial overview with donut charts.](../images/agentic-contact-center-banking-c360.png)

## Customer summary

The customer summary is an AI-generated summary that provides the CSR with a concise overview of the customer's relationship with the bank. The summary includes information such as:

-   How long the customer has been with the bank
-   A brief overview of the customer's active accounts
-   A summary of recent transactions
-   An assessment of the customer's financial standing, including any defaults, delinquencies, and transaction patterns

## Financial overview

The following summary metric cards display the customer's financial position:

-   **Total deposit**: The combined balance across the customer's deposit products, including savings accounts, checking accounts, and fixed-term deposits \(certificates of deposit\). Calculated as the sum of balances across deposit and investment accounts.
-   **Total available credit**: The remaining available balance across billing products, including credit cards, overdraft facilities, and lines of credit. Calculated as the sum of available balances across credit card accounts.
-   **Total money owed**: The total outstanding amount the customer owes the bank, including unpaid loan balances and outstanding credit card balances. Calculated as the sum of balances across line of credit and loan accounts.

When a metric applies but the value is zero, the card displays **$0**. When no relevant product exists for the customer \(for example, no credit card account is on record\) the card displays **No account available**.

## Accounts and transactions

The **Accounts** section displays a list of all active financial accounts held by the customer. When an account is selected, a card displays the product name, masked account number \(last four digits visible\), balance, and account status.

Recent transactions display for the selected customer account, showing description, posted date and time, amount, and transaction type \(debit or credit\). Transactions are sorted with the most recent first.

## Cases

The **Cases** section shows all cases associated with the customer. The list displays with case number, date and time, service definition, status, and assigned agent. Cases are sorted by date and time by default, with the most recent first.

CSRs can filter cases by case number, financial account, state, and case owner, and can sort cases by case number, date and time, case type, case status, and assigned agent. Selecting a case number opens the case record.

## Other page sections

The following table lists other sections in the Customer 360 page. Its contents vary depending on whether the customer is a retail consumer \(B2C\) or a commercial account \(B2B\).

<table id="table_pjl_c4r_q3c"><thead><tr><th>

Name

</th><th>

Customer type

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="2">

Customer details

</td><td>

Account

</td><td>

Displays the account name, primary contact, phone number, email address, industry, and doing-business-as name.

</td></tr><tr><td>

Consumer

</td><td>

Displays the consumer's name, address information, date of birth, nationality, phone number, and email.

</td></tr><tr><td>

Interaction history

</td><td>

Both

</td><td>

Lists recent interactions logged against the account or consumer, displayed with the most recent first.

</td></tr><tr><td>

Contacts

</td><td>

Account

</td><td>

Lists all authorized contacts associated with the account, showing each contact's name and email address. A corporate account can have multiple authorized contacts depending on the organization's size.

</td></tr><tr><td>

Household members

</td><td>

Consumer

</td><td>

Lists individuals linked to the retail consumer, such as family members or authorized representatives. If no household members have been added, the section displays a message indicating that none are on record.**Note:** This displays when the Customer Service Household plugin is installed.

</td></tr></tbody>
</table>## Contextual side panel

The contextual side panel appears on the right side of the page and provides access to supplementary tools and related record information. The following default CSM components are available in the panel:

-   Activity stream
-   Attachments
-   Templates
-   Recommended Actions
-   Related items

## Actions

The following table shows the available actions in the Customer 360 page.

|Name|Description|
|----|-----------|
|Ask Now Assist|Opens the Now Assist panel and initiates the Banking CSR customer insights AI agent. This agent uses the customer's profile and financial data to surface insights. See [Agentic Contact Center for Banking AI agents overview](../../fso-now-assist/concept/agentic-contact-center-for-banking-agents-overview.md) for more information.|
|Create case|Opens the **Create new case** window to create a case for the customer.|

**Parent Topic:**[Financial Services](../../fso-common/concept/fso-overview.md)

**Related topics**  


[Exploring Agentic Contact Center for Banking](exploring-agentic-contact-center-for-banking.md)

[Interaction page for Agentic Contact Center for Banking](interaction-workspace-for-agentic-contact-center-for-banking.md)

[CSM Configurable Workspace](https://www.servicenow.com/docs/access?context=csm-workspaces-configure&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)

