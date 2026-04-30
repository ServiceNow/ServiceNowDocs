---
title: Enabling guest users to submit a catalog item on the Customer Service Portal
description: Configure customer service portal to enable guest users to access and submit catalog item.
locale: en-US
release: yokohama
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configure the Customer and Consumer Service Portals, Set up self-service, Configuring Customer Service Management, Customer Service Management]
---

# Enabling guest users to submit a catalog item on the Customer Service Portal

Configure customer service portal to enable guest users to access and submit catalog item.

Guest users or logged out users can’t access catalog items by default. You must change the accesses for the catalog items and its related services to make a catalog item available for guest users.

## Changes required to enable guest user access

Make the following items public to enable logged out users to request catalog items:

<table id="table_om3_cgn_w2c"><thead><tr><th>

Item

</th><th>

Required changes

</th></tr></thead><tbody><tr><td>

Portal pages and widgets

</td><td>

Enable public access for those portal pages and widgets that are used to display the following:-   list of catalog items
-   catalog item form
-   Home page or browse catalog page to which the users are redirected to after submitting the catalog item

For details, see [Enable public access on a service portal page](enable-publicaccess-on-page-csm-portal.md) and [Enable public access on widgets](enable-publicaccess-on-widgets-csm-portal.md).

</td></tr><tr><td>

Catalog categories

</td><td>

Enable public access for those catalog categories that enables the guest users to browse the list of items on the widget.For details, see [Enable public access for categories for the catalog items](make-catalogitem-categories-public-csm-portal.md).

It is optional to make these items public

</td></tr><tr><td>

Catalog items

</td><td>

Enable public access for the catalog items and their forms that must be displayed to the guest users.For details, see [Enable public access for a catalog item](make-item-public-csm-portal.md).

**Note:** Configure the catalog item script to display post submission confirmation message and redirection to an appropriate page. For details, see [Configure catalog item script to display confirmation message and redirect the guest user](configure-catalogitem-script-toredirect.md).

</td></tr><tr><td>

Catalog item variables and variable sets

</td><td>

Enable public access for the catalog item variables and variable sets that should be displayed on the submit form for guests.For details, see [Enable public access for a catalog item variable and variable set](make-catalogitem-variable-public-csm-portal.md).

</td></tr><tr><td>

Catalog item APIs

</td><td>

Enable public access for the catalog item APIs to allow submitting the form.For details, see [Enable public access on REST APIs](enable-publicaccess-for-restapis-csm-portal.md).

**Note:** Introduce rate limits on the public REST APIs to avoid excessive use or abuse of publicly available catalog items. For details, see [Apply a rate limit on REST APIs](apply-ratelimit-for-restapis-csm-portal.md).

</td></tr></tbody>
</table>