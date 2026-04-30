---
title: Setting up a remote table integration
description: This use case illustrates how an agent at a financial institution can access individual consumer, bank account, and transactional data that resides in a third-party external system. This integration methodology can apply across industries, such as integrating to a policy administration system in insurance.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Integration use cases, Developer resources, Financial Services Operations \(FSO\)]
---

# Setting up a remote table integration

This use case illustrates how an agent at a financial institution can access individual consumer, bank account, and transactional data that resides in a third-party external system. This integration methodology can apply across industries, such as integrating to a policy administration system in insurance.

## Scenario

A consumer of the financial institution calls in to get more information about a recent transaction on their savings account. The agent at the financial institution creates an interaction record while on the phone with the consumer. The agent wants to review recent transactional activity, so they populate the consumer's details within the Consumer field and save.

The Consumer field is referencing a remote table, which means the consumer’s record is being retrieved from the financial institution’s CRM tool without being stored in ServiceNow.

Once the agent selects the consumer in the Consumer field, they can see all of their related savings accounts in a separate field, labeled Deposit Account. This field is referencing account information from an external system. The list of bank accounts is filtered to the consumer’s using a reference qualifier.

Once the agent opens the consumer’s record, they can see the related bank accounts and related transactions that reside in the external system. The agent can easily find the transaction the consumer is calling about and move forward in the resolution process.

The agent creates a case from the interaction record through a UI action. The remote data from the interaction is retrieved and pre-populated on the case form.

## Objectives

This use case achieves the following:

-   Look up an individual Customer \(Consumer\) from an interaction which is stored in an external system
-   Filter the list of available deposit accounts on the interaction record based on the consumer selected
-   After opening the Consumer detail page, provide a related list titled 'Bank accounts', which pulls in any Bank accounts stored in an external system for that Consumer record
-   After selecting a 'Bank account' record, provide a related list titled 'Transactions', which pulls in any Transactions stored in an external system for that Bank account
-   Leverage a UI policy to create a financial services case from the interaction record and pre-populate the consumer and bank account information populated by the agent on the interaction record

## High-level setup procedure

The following table shows the steps to set up a remote table integration and display the data in the user interface.

<table id="table_hyc_crj_mcc"><thead><tr><th>

Step

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Activate the remote tables plugin

</td><td>

The remote tables plugin must be enabled for the ServiceNow instance to support remote tables. For more information, see [Activate the remote tables plugin](https://www.servicenow.com/docs/access?context=activate-remote-tables-plugin&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

Inspect the source data

</td><td>

Based on the approach you plan to take, you should determine what external data is shown in the system. The endpoints and queried source data will vary depending on your individual architectural layout.

</td></tr><tr><td>

Create the required remote tables

</td><td>

Create the required remote tables so you can see the proper data retrieved from the external source.A remote table needs an external primary key to relate its temporary data to the data stored in the external source.

You should identify the data elements you want to pull from the external sources and display in your workspace. For example, when pulling Consumer information, in addition to the external primary key, you may want to include full name, country code, city, and so on.

</td></tr><tr><td>

Create outbound REST messages

</td><td>

Set up the outbound REST message requests to perform proper GET calls to the external system where the information is stored. Navigate to **All** &gt; **System Web Services** &gt; **Outbound** &gt; **REST Messages** to do so.

</td></tr><tr><td>

Create consumer remote table definition

</td><td>

Create the proper definitions where you define the script and tell ServiceNow what actions to perform when invoking each REST API call.In this step, you’ll align the values you want to display in your remote table to the values that are specified in your external system.

You also must map the sys\_id field to the designated external primary key in the external system.

</td></tr><tr><td>

Create entity relationships through remote tables

</td><td>

When making other remote tables, create relationships between them by mapping the unique external primary key to the sys\_id field of your remote table.For example, to relate a bank account or insurance policy to its consumer, the external primary key must be mapped to the sys\_id field in the Consumer remote table definition.

Configure the Related Lists for the consumer to view the related records. This can be done by opening the context menu of consumer record, then navigating to **Configure** &gt; **Related Lists**.

</td></tr><tr><td>

Update fields on the interaction record to reference remote tables

</td><td>

This step gives an agent the ability to search for the remote data when needed.Create custom fields that reference your remote tables in an interaction. This can be done by opening the context menu of the interaction record, then navigating to **Configure** &gt; **Form Layout**.

</td></tr><tr><td>

Add reference qualifiers on fields

</td><td>

This step enables filtering of the list so it only shows, for example, accounts or policies within the external system that are related to the selected consumer.For more information, see [Reference qualifiers](https://www.servicenow.com/docs/access?context=c_ReferenceQualifiers&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

Create a UI action to populate remote data

</td><td>

Create a UI action to populate remote data from the interaction into the case, or the respective objects in your workflow.For more information, see [Create a UI action](https://www.servicenow.com/docs/access?context=t_EditingAUIAction&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

Utilize the FSO Lookup client action

</td><td>

The Lookup UXF Client action, included in the Financial Services Remote Tables plugin, is essential for setting up the FSO Lookup Client action.This action integrates the Action Payload Definition and is used within a field decorator as a UXF Client action.

It’s available as part of the Remote table lookup application but requires integration with a field decorator or a declarative action.

For more information on the FSO Look Up Client action, see [FSO Look Up Client action](../../../../product/fso-common/reference/fso-look-up-client-action.md).

</td></tr><tr><td>

Display remote transactions for locally stored financial account

</td><td>

You can choose to keep information that changes frequently in remote tables \(such as transactions\) while storing other data that doesn't change in local tables.For instance, you can display transactions for a persisted bank account as a related list where all transactional data remains in an external system. For more information, see [Create defined related lists](https://www.servicenow.com/docs/access?context=t_CreateDefinedRelatedLists&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

When creating the relationship, specify the remote table as the **Queries from table** value. Use a function in the **Query with** field to define the relationship between the transactions and account.

</td></tr></tbody>
</table>For more information on the implementation walkthrough, see the FSO Remote Table setup guide.

