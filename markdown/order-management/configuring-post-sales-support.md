---
title: Configure Customer Contracts and Entitlements
description: Use the Customer Contracts and Entitlements application to configure and display customer contracts and entitlements.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Configure Customer Contracts and Entitlements

Use the Customer Contracts and Entitlements application to configure and display customer contracts and entitlements.

## Activate Customer Contracts and Entitlements

As an admin, you can activate the following plugins to enable users to create and manage Customer Contracts and Entitlements. For more information, see [Activate a plugin](https://www.servicenow.com/docs/access?context=t_ActivateAPlugin&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

<table id="table_yct_wrv_4zb"><thead><tr><th>

Plugin

</th><th>

Description

</th><th>

Dependency

</th></tr></thead><tbody><tr><td>

Customer Contracts and Entitlements\[com.sn\_pss\_core\]

</td><td>

Provides foundational objects to manage Customer Contracts and Entitlements and APIs for integration.

</td><td>

-   Customer Service Install Base Management

\[com.snc.install\_base\]​

-   Product Catalog Management Core

\[com.sn.prd\_pm\]


</td></tr><tr><td>

Entitlements Verification\[com.sn\_ent\_verify\]

</td><td>

Provides APIs to verify entitlement.​

</td><td>

Customer Contracts and Entitlements \[com.sn\_pss\_core\]​

</td></tr><tr><td>

[Contracts and Entitlement Workflows​](configure-cont-ent-workflows-csm.md)\[com.sn\_contract\_ent\_wf\]

</td><td>

Provides workflows to manage changes on Customer Contracts and Entitlements.

</td><td>

-   Customer Contracts and Entitlements Foundation

\[com.sn\_pss\_core\]​

-   Lead to Cash Primitives

\[com.sn\_l2c\_core\]

-   Customer Life Cycle Management Workflows

\[com.sn\_l2c\_cust\_flows\]​


</td></tr></tbody>
</table>With the activation of Customer Contracts and Entitlements, the existing contracts are available for viewing only.

For more information on the installed roles and tables, see [Components installed with Customer Contracts and Entitlements](../reference/components-installed-pss.md).

## Request apps from the ServiceNow Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

