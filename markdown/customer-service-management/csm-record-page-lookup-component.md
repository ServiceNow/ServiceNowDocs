---
title: Lookup component
description: Use the lookup component on interaction record pages in CSM Configurable Workspace to look up, link, and verify a contact or consumer on an interaction record.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Front-line case page, CSM Configurable Workspace record pages, Set up CSM Configurable Workspace, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Lookup component

Use the lookup component on interaction record pages in CSM Configurable Workspace to look up, link, and verify a contact or consumer on an interaction record.

![Lookup and verify contact card includes the contact name plus selectable fields for account name, email address, and phone numbers](../image/lookup-and-verify-component.png "Lookup and verify contact card")

The lookup component is available on the following interaction record pages:

-   [CSM centered chat interaction record page](csm-centered-chat-interaction-page.md)
-   [CSM voice interaction record page](csm-native-voice-record-page.md)
-   Email interaction record page

**Note:** For some of these interaction record pages, the Lookup component replaces the Lookup &amp; Verify component that was formerly available in the contextual side panel.

For more information about the component usage and configuration, see [Lookup](https://developer.servicenow.com/dev.do#!/reference/next-experience/zurich/now-components/record%20lookup/overview) in the [Next Experience Components documentation](https://developer.servicenow.com/dev.do#!/reference/next-experience/components?&query=&order_by=nameAsc&limit=120&offset=0&categories[]=uib_component&categories[]=uib_macroponent-component&categories[]=uib_facades).

## Using the lookup component

Customer service agents can use the lookup component to search for and select a customer, either a contact or consumer, and link that customer to the interaction record.

Linking a customer displays the customer information in a contact or consumer card on the interaction record. After linking a customer to the record, agents can verify the customer.

<table id="table_wwj_ks2_yfc"><thead><tr><th>

Task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Search for a contact or consumer

</td><td>

Enter information in the **Search** field on the lookup card such as a name, email address, phone number, or record number. The lookup card displays a list of search results based on the search term.![The lookup card displays a list of cards with results that match the entered search term, such as contacts with the first name of George](../image/lookup-and-verify-search-consumer.png "Lookup and verify search")

</td></tr><tr><td>

Link a contact or consumer to the interaction record

</td><td>

Select the Link icon \(![link icon looks like two interconnected chain links](../image/lookup-and-verify-link-contact.png)\) on a customer card from the list of search results to link the selected customer with the interaction record.

</td></tr><tr><td>

Verify a contact or consumer

</td><td>

Verify the customer by selecting **Verify** on the lookup card. The system displays the Verified tag in the card header.If the customer is already verified, the system hides the **Verify** button.

**Note:** If an agent creates a customer record from the lookup component, the system creates and verifies the customer at the same time.

</td></tr><tr><td>

Create a contact or consumer

</td><td>

Create a customer record by selecting the Create new \(![Create new icon is a plus sign inside a circle](../image/lookup-and-verify-add-customer.png)\) icon in the lookup card header.The system displays a new contact or consumer record. Enter information in the relevant fields and select **Save**.

**Note:** If an agent creates a customer record from the lookup component, the system creates and verifies the customer at the same time.

</td></tr><tr><td>

Edit a contact or consumer

</td><td>

Make changes to the linked customer information by selecting the More actions \(![More actions icon is three vertically stacked dots](../image/lookup-and-verify-more-actions-menu.png)\) menu on the lookup card and then selecting **Edit**.The system displays the contact or consumer record fields. Make changes to the desired fields and then select **Save**.

The system saves the changes to the contact or consumer information and updates the same fields on the interaction record.

</td></tr><tr><td>

Unlink a contact or consumer

</td><td>

Select the More actions \(![More actions icon is three vertically stacked dots](../image/lookup-and-verify-more-actions-menu.png)\) menu on the lookup card and then select **Unlink** to remove a contact or consumer from an interaction record.

</td></tr><tr><td>

Collapse or expand the lookup card

</td><td>

Select the up and down arrows on the lookup card to expand and collapse the card. When expanded, agents can see the customer details. When collapsed, agents can see more content below the card.

</td></tr></tbody>
</table>## Contact lookup card

The contact lookup card includes the following information:

-   Name
-   Mobile phone
-   Business phone
-   Email
-   Street
-   City
-   State/Province
-   Account

## Consumer lookup card

The consumer lookup card includes the following information:

-   Name
-   Business phone
-   Mobile phone
-   Home phone
-   Email
-   Street
-   City
-   State/Province

