---
title: Service catalog integration with the Customer and Consumer Service Portals
description: Users with the customer administrator role \(sn\_customerservice.customer\_admin\) can associate a portal with a service catalog.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [CSM integration with Request Management, CSM integration with IT Service Management overview, Integrating with IT Service Management, Integrating Customer Service Management with other applications, Customer Service Management]
---

# Service catalog integration with the Customer and Consumer Service Portals

Users with the customer administrator role \(sn\_customerservice.customer\_admin\) can associate a portal with a service catalog.

The following catalog pages and widgets are provided as part of the Customer Service with Request Management integration.

For more information, see [Associate a portal with a catalog](https://www.servicenow.com/docs/access?context=associate-portal-catalog&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

## CSM Catalog page

This is the display page for catalog items on the Customer and Consumer Service Portals. This page serves as the landing page for any service catalog item exposed on a CSM portal. All request items exposed on the CSM portals are either service catalog items or service catalog record producers. Navigate to **Service Portal** &gt; **Pages** to view this page.

-   Page ID: csm\_sc\_cat\_item
-   Update name: sp\_page\_7ea80b123bb31300bfe04d72f3efc4b7
-   Available to roles: snc\_internal, snc\_external

## CSM Catalog Item widget

This widget handles the redirection logic on submission of the catalog item and embeds the default catalog item widget. This widget listens to event **$sp.sc\_cat\_item.submitted**. On submission of a catalog item, it handles the portal redirection logic based on the page\_id and the catalog portal URL. When there is no parent set in the Requests \(sc\_request\) table, the URL is redirected to the default service portal ticket page. If a record producer has a redirect URL, this widget uses the redirect URL from the record producer instead of redirecting to the ticket page.

-   Widget ID: csm-sc-cat-item
-   Update name: sp\_widget\_ec837c713bbb1300bfe04d72f3efc4d1
-   Available to roles: snc\_internal, snc\_external

## Page route map

It is important to set up a page route map for any new Service Portals to handle the redirection to the Case ticket page. The redirection is based on the logic described in the CSM Catalog Item widget.

-   CSM Catalog item page route map: for the Customer Service Portal, this page route map routes the URL redirect from the sc\_cat\_item page to the csm\_sc\_cat\_item page.
-   CSP Catalog item page route map: for the Consumer Service Portal, this page route map routes the URL redirect from the sc\_cat\_item page to the csm\_sc\_cat\_item page.

## Portal settings for catalog items

Once the catalog items are defined, visibility of the **Submit**/**Add to Cart** button can be controlled by navigating to **Service Catalog** &gt; **Catalog Definitions** &gt; **Maintain Items**, selecting the desired item, and enabling or disabling the fields in the Portal Settings form section.

<table id="table_lz1_yhm_cmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Request method

</td><td>

Select Order, Request, or Submit as the type of catalog item.

</td></tr><tr><td>

Hide ‘Add to Cart'

</td><td>

Enable if the **Add to Cart** button should be disabled for the catalog item. **Note:** The **Add to Cart** button is not currently supported on the Customer Service Portal or the Consumer Service Portal.

</td></tr><tr><td>

Hide Quantity

</td><td>

Enable if the **Quantity** of the catalog item should be hidden.

</td></tr><tr><td>

Hide Delivery Time

</td><td>

Enable if the **Delivery Time** of the catalog item should be hidden.

</td></tr><tr><td>

Hide ‘Add to Wish List’

</td><td>

Enable if the **Add to Wish List** button for the catalog item should be hidden.

</td></tr><tr><td>

Hide Attachment

</td><td>

Enable if the attachment of the catalog item should be hidden.

</td></tr></tbody>
</table>