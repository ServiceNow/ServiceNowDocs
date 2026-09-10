---
title: Enable a shopper to purchase on behalf of another user
description: Configure the Shopping Hub to enable a shopper to purchase on behalf of another user.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/config-shoppinghub-purchase-behalf.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-08-07"
reading_time_minutes: 1
breadcrumb: [ShoppingHub configuration, Set up master data, Configure, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Enable a shopper to purchase on behalf of another user

Configure the Shopping Hub to enable a shopper to purchase on behalf of another user.

## Before you begin

Role required: sn\_shop.procurement\_administrator

## Procedure

1.  Navigate to **All** &gt; **ShoppingHub** &gt; **Administration** &gt; **ShoppingHub Configuration**.

2.  Select **New**.

    \[Omitted image "sh-config-behalf.png"\] Alt text: ShoppingHub Configuration form with "Purchase on behalf of" selected as configuration type.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the configuration|
    |Configuration type|Select **Purchase on behalf of** from the list to enable purchasing on behalf of another user.|
    |Active|Check box that indicates whether the configuration is active.|
    |Group of shoppers|The group of shoppers who are authorized to purchase on behalf of other users.|
    |Group\(s\) to be shopped on behalf of|The group of users for whom purchases can be made on their behalf.|
    |Individual shoppers|Individual users who are authorized to purchase on behalf of other users.|
    |Individual\(s\) to be shopped on behalf of|The individual users for whom purchases can be made on their behalf.|
    |Cost centers of shoppers|The cost centers of shoppers who are authorized to purchase on behalf of users in the same cost centers.|
    |Cost centers to be shopped on behalf of|The cost centers of the users for whom purchases can be made on their behalf.|
    |Legal entities of shoppers|The legal entities of shoppers who are authorized to purchase on behalf of users in the same legal entities.|
    |Legal entities to be shopped on behalf of|The legal entities of the users for whom purchases can be made on their behalf.|
    |Countries of shoppers|The countries of shoppers who are authorized to purchase on behalf of users in the same countries.|
    |Countries to be shopped on behalf of|The countries of the users for whom purchases can be made on their behalf.|

    **Note:** The cost center, legal entity, and country fields can be used on their own or together with the group and individual fields. A match on any configured field is sufficient to authorize the purchase-on-behalf-of relationship.

4.  Select **Submit**.


**Parent Topic:**[ShoppingHub configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/shoppinghub-configurations.md)

