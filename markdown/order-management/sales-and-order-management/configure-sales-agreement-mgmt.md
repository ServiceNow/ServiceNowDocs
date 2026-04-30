---
title: Configure Sales Agreement Management
description: Use the Sales Agreement Management application to create sales agreements between a buyer and a seller for future transactions.
locale: en-US
release: yokohama
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Sales Customer Relationship Management applications, Sales Customer Relationship Management]
---

# Configure Sales Agreement Management

Use the Sales Agreement Management application to create sales agreements between a buyer and a seller for future transactions.

## Activate Sales Agreement Management

As an admin, you can activate the following plugins to enable users to create and manage sales agreements. For more information, see [Activate a plugin](https://www.servicenow.com/docs/access?context=t_ActivateAPlugin&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

<table id="table_dz4_d2c_wbc"><thead><tr><th>

Plugin

</th><th>

Description

</th><th>

Dependency

</th></tr></thead><tbody><tr><td>

Sales Agreement Data Model \[com.sn\_sales\_agmt\_core\]

</td><td>

This plugin provides foundational objects to manage sales agreements.

</td><td>

-   Product Catalog Management Core\[com.sn\_prd\_pm\]​
-   Price Management \[com.sn\_csm\_pricing\]

</td></tr><tr><td>

Sales Agreement Management \[com.sn\_sales\_agmt\_wf\]

</td><td>

This plugin provides workflow to create and manage sales agreements.

</td><td>

-   Sales Agreement Data Model \[com.sn\_sales\_agmt\_core\]
-   Lead to Cash Core \[com.sn\_l2c\_core\]​
-   Quote Management Application \[com.sn\_l2c\_quote\_mgmt\]

**Note:** You need to install the Quote Management Application plugin separately.


</td></tr></tbody>
</table>For more information on the installed roles and tables, see [Components installed with Sales Agreement Management](../reference/components-installed-sales-agreement.md). To view sales agreements from an account, you must manually configure the sales agreement related list on the Account form.

## Request apps from the ServiceNow Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

