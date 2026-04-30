---
title: Add a new button in Shopping Hub
description: You can add a new button in Shopping Hub, similar to the existing Don’t see what you need? button.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Add a new button in Shopping Hub

You can add a new button in Shopping Hub, similar to the existing Don’t see what you need? button.

## Before you begin

Role required: sn\_shop.shopping\_hub\_admin or sn\_shop.procurement\_administrator

## Procedure

1.  In the navigation filter, enter `sys_ux_page_property_list.do`.

2.  On the UX Page Properties, select the existing configuration for the **Don't see what you need** button.

    ![UX Page Properties list showing the configuration for the Don't see what you need button.](../image/sh-new-button-properties.png)

3.  On the UX Page Property page, add a new link object in the Value section.

    ![UX Page Property page with Value section highlighted.](../image/sh-ux-page-property.png)

4.  Add a new link object after the final entry to add the new button, following the structure shown below:

    ```
    {
                        "id": 6,
                        "type": "external",  // or "internal" if it's a ServiceNow page
                        "target": "_blank",  // or "_self" if opening in same window
                        "opensWindow": true,  // or false for internal links
                        "label": {
                            "translatable": true,
                            "message": "Your New Button Text"
                        },
    ```

5.  Select **Update**.


## Result

The newly added button is displayed in Shopping Hub.

**Parent Topic:**[Configure Sourcing and Procurement Operations](../concept/configuring-spo.md)

**Related topics**  


[Install Sourcing and Procurement Operations](activate-finance-spend-central.md)

[Setting up primary data for ShoppingHub](../reference/set-up-master-data-shopping-hub.md)

[Configure punchout for third-party site purchases](configure-supplier-punchout.md)

[Configuring work prioritization](../concept/configuring-work-prioritization.md)

[Customize your top suppliers on Shopping Hub](customize-top-suppliers.md)

[Configure conditions for merging purchase requisitions](config-pr-merge.md)

[Service portal configuration for ShoppingHub](../concept/service-portal-configuration-for-shoppinghub.md)

[Install ShoppingHub Mobile](install-shoppinghub-mobile.md)

[Advanced Work Assignment for Source-to-Pay Operations](../concept/awa-spo.md)

