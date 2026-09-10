---
title: Party Relationship Center
description: The Party Relationship Center \(PRC\) provides a single, unified view of all entities connected to a party, including billing accounts, sold products, related parties, and active cases.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-media-technology/c360-prc-overview.html
release: australia
topic_type: concept
last_updated: "2026-09-01"
reading_time_minutes: 3
keywords: [party relationship centre, PRC, node map, customer hierarchy, relationship graph]
breadcrumb: [Explore, Telecommunications Customer 360, Telecommunications, Media, and Technology \(TMT\)]
---

# Party Relationship Center

The Party Relationship Center \(PRC\) provides a single, unified view of all entities connected to a party, including billing accounts, sold products, related parties, and active cases.

**Note:** To view the party relationship center, you must have the`sn_genai_platform` plugin installed.

An interactive graph of all entities connected to a party is displayed in the CSM/FSM Configurable Workspace. It is fully configurable and administrators can controlAdministrators can control which entities appear in the graph, what information is displayed on each node, and how relationships are visualized. A contextual side panel shows detailed information about any selected entity and eliminates the need to navigate across multiple screens or applications.

Log in as a user with the sn\_telecom\_c360.user or the sn\_telecom\_c360.admin role and select the Party Relationship Center icon on the [Telecommunications Customer 360 home page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/c360-home-page.md). The map is displayed when a graph configuration exists for the selected consumer or account.

Each node in the map displays a header, subheader, highlighted value, and contextual side panel properties. You can configure these values per node type. The node map supports horizontal and vertical orientation. Selecting any node opens a contextual side panel that displays the configured properties for that entity. You can also navigate directly to a node's underlying record by selecting the open-record button in the side panel.

Use the **Search** option to filter the node map by typing a value that matches the header or subheader configured for a node type. Matching nodes are highlighted in the graph.

## Consumer party relationship map

When the customer is a consumer, the map displays the consumer and up to five levels of related entities. Products can link directly to the consumer or through a billing account.

-   **Tier 1: Consumer**

    The primary consumer. Displays the consumer's name, phone, and address. Table: `sn_customerservice_consumer`.

-   **Tier 2: Consumer relationships**

    Consumers related to the primary consumer, including consumer-to-consumer relationships and household-to-consumer relationships. Tables: `sn_customerservice_consumer_relationship`, `household_member_relationship`.

-   **Tier 3: Billing account**

    The billing account connected to the consumer through the billing account related party relationship. The consumer who owns the billing account is the bill-to consumer. Table: `sn_crt_billing_account`.

-   **Tier 4: Sold products**

    Products linked to the billing account. Each consumer's role on a product is shown: Owner, Authorized, User, or Dependent. Each product card displays the Sold To consumer and the Billed Through billing account. Tables: `sn_prd_invt_product_inventory`, `sn_prd_invt_product_related_party`.

-   **Tier 5: Transactions**

    Active cases, incidents, and work orders linked to each product. Each card displays the record number, short description, and table name. Tables: `sn_customerservice_case`, `incident`, `sn_csm_work_order`.


## Account party relationship map

When the customer is an account, the map displays the parent account and up to five levels of related entities for each child account.

-   **Tier 1: Parent account and child accounts**

    The parent account and its child accounts, linked through `sn_customerservice_account_relationship`. Each child account displays as its own section in the map.

-   **Tier 2: Billing account**

    The billing account for each account. The billing account displays alongside the account hierarchy. Contacts with billing-level responsibilities are identified through the billing account related party relationship. Table: `sn_crt_billing_account`.

-   **Tier 3: Contacts**

    Contacts linked to the account through the contact relationship. Each contact's responsibility is shown: Account Manager, Billing Contact, Technical Contact, or Support Contact. Table: `customer_contact`.

-   **Tier 4: Sites and sold products**

    Products sold to the account at a specific site \(`cmn_location`\). Multiple sites per account display as separate sections. Each product card displays the Sold To account and the Billed Through billing account. Tables: `sn_prd_invt_product_inventory`, `sn_prd_invt_product_related_party`.

-   **Tier 5: Transactions**

    Active cases, incidents, and work orders linked to each product. For telecom products, TMForum CFS/RFS/Resource decomposition can be expanded. Tables: `sn_customerservice_case`, `incident`, `sn_csm_work_order`.


**Related topics**  


[Configure the Party Relationship Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/c360-configure-prc.md)

