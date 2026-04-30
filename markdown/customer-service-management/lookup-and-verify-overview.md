---
title: Lookup and verify
description: The lookup and verify feature enables customer service agents to quickly look up contacts or consumers using information such as the name, phone number, or record number.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [CSM Configurable Workspace features, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Lookup and verify

The lookup and verify feature enables customer service agents to quickly look up contacts or consumers using information such as the name, phone number, or record number.

This feature simplifies the process of looking up and verifying contact or consumer information. Agents can use it as follows:

-   If an interaction record is already populated with contact or consumer information from a chat or phone call, the agent can review the information and confirm that it is correct.
-   If no customer or consumer information is available, the agent can search for this information, select and confirm the information. and populate the interaction record.

**Note:** If this information has already been verified, such as through a customer portal login or authentication by Virtual Agent or by an IVR, the **Verified** check box on the interaction record is checked.

Agents can access the search window on the interaction record as follows:

-   CSM Configurable Workspace: By clicking the Verify Contact icon \(![Verify contact icon.](../image/config-ws-lookup-verify-contact.png)\) or the Verify Consumer icon \(![Verify consumer icon.](../image/config-ws-lookup-verify-consumer.png)\) in the contextual side panel.
-   CSM Agent Workspace: By clicking the **Lookup Contact** and **Lookup Consumer** buttons.

Agents can perform a type-ahead search across multiple configurable fields such as name, phone number, email address, and record number. From the search results list, agents can select a result to display detailed information for the contact or consumer in a verification card. Once verified, the system adds the information to the interaction record and checks the **Verified** check box.

## Plugins

The lookup and verify feature is included with the Customer Service \(com.sn\_customerservice\) plugin. This plugin provides the configuration for contact and consumer lookup as well as **Lookup Contact** and **Lookup Consumer** UI actions that can be added to the interaction record in CSM Configurable Workspace.

**Note:** These actions are not enabled by default. The workspace admin can enable these actions as part of the lookup and verify feature configuration.

## Contact and consumer configurations

Two lookup and verify configurations are provided with the feature, one for contacts and one for consumers. Navigate to **Workspace Experience** &gt; **Lookup and Verify** &gt; **Configuration** to access the Lookup and Verify Configurations list.

**Note:** To see the contact and consumer lookup and verify configurations, you must activate the CSM Lookup and Verify plugin \(com.snc.sn\_csm\_lookup\_verify\).

For each configuration, the workspace administrator can:

-   Enable the configuration and display the related UI action on the interaction record.
-   Enter the minimum number of characters to start the type-ahead search.
-   Enter the maximum number of search results returned.
-   Select the primary and secondary fields to include in the search results.
-   Select the fields to display on the verification card.
-   View the lookup tables.

**Note:** Customers can contact ServiceNow to make changes to the search fields.

## Using Lookup and verify in CSM workspaces

Agents can use the lookup and verify feature in CSM workspaces.

-   CSM Configurable Workspace: agents search for contact or consumer information using the contextual side panel.
-   CSM Agent Workspace: agents search for contact or consumer information using the Verify Contact or Verify Consumer pop-up windows on the interaction form.

The search field provides type ahead search that displays results in a list and narrows the results as more characters are entered. Selecting a result from the list displays more detailed information about the contact or consumer in a verification card.

The search feature searches multiple configured fields such as name, account, phone number, and record number.

-   For phone numbers and record numbers, it uses an "exact match" search.
-   For other fields, it uses a "starts with" search.

## Verification cards

After selecting a search result, detailed information about the contact or consumer is displayed in a verification card. From this card, the customer service agent can review and confirm the information by clicking **Verified**.

## Tables

The lookup and verify feature uses the following tables:

-   Lookup and Verify Configurations \(sn\_lookup\_verify\_config\)
-   Lookup Tables \(sn\_lookup\_verify\_search\_on\_table\)

**Related topics**  


[Look up and verify a contact or consumer](../task/lookup-verify-contact-consumer.md)

