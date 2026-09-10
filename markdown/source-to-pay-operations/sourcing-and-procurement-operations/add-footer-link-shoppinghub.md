---
title: Add a footer link in Shopping Hub
description: You can add a link to the footer of Shopping Hub, similar to the existing Don't see what you need? link.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/add-footer-link-shoppinghub.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-08-31"
reading_time_minutes: 3
breadcrumb: [Configure, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Add a footer link in Shopping Hub

You can add a link to the footer of Shopping Hub, similar to the existing Don't see what you need? link.

## Before you begin

Role required: sn\_shop.shopping\_hub\_admin or sn\_shop.procurement\_administrator

## Procedure

1.  In the navigation filter, enter `sys_ux_page_property_list.do`.

2.  On the UX Page Properties, select the existing configuration for the **Don't see what you need** button.

    \[Omitted image "sh-new-button-properties.png"\] Alt text: UX Page Properties list showing the configuration for the Don't see what you need button.

3.  On the UX Page Property page, add a new link object in the Value section.

    \[Omitted image "sh-ux-page-property.png"\] Alt text: UX Page Property page with Value section highlighted.

4.  Add a new link object after the final entry to add the new link, following the structure shown below:

    ```
    {
                        "id": 6,
                        "type": "external",  // or "internal" if it's a ServiceNow page
                        "target": "_blank",  // or "_self" if opening in same window
                        "opensWindow": true,  // or false for internal links
                        "label": {
                            "translatable": true,
                            "message": "Your New Link Text"
                        },
    ```

5.  Select **Update**.


## Result

The newly added link is displayed in the Shopping Hub footer.

## What to do next

The `chrome_footer` page property is part of the Now Experience Framework page configuration for Shopping Hub. For more information about UI Builder, which manages other page configuration for Shopping Hub, see [UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder-overview.md).

**Parent Topic:**[Configuring Sourcing and Procurement Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/configuring-spo.md)

**Related topics**  


[Sourcing and Procurement Operations product tile]()

[Sourcing and Procurement Operations Product Hub]()

[Install Sourcing and Procurement Operations]()

[Sourcing and Procurement Operations Configuration Console]()

[Configure Sourcing and Procurement Operations]()

[Setting up primary data for ShoppingHub]()

[Configure punchout for third-party site purchases]()

[Configuring work prioritization]()

[Add a button in Shopping Hub]()

[Customize your top suppliers on Shopping Hub]()

[Configure conditions for merging purchase requisitions]()

[Service portal configuration for ShoppingHub]()

[Install ShoppingHub Mobile]()

[Advanced Work Assignment for Source-to-Pay Operations]()

[Install Universal Request for Sourcing and Procurement Operations]()

