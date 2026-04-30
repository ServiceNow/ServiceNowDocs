---
title: SaaS detection report
description: Use the SaaS detection report to discover and manage all SaaS applications accessed via a browser and configured within the ServiceNow Agent Client Collector for Visibility - Content \(ACC-VC\) product. The SaaS applications that can be managed through this report can be paid or free ones.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [References, Software Asset Management, IT Asset Management]
---

# SaaS detection report

Use the SaaS detection report to discover and manage all SaaS applications accessed via a browser and configured within the ServiceNow® Agent Client Collector for Visibility - Content \(ACC-VC\) product. The SaaS applications that can be managed through this report can be paid or free ones.

**Important:** To view the SaaS detection report, you must do the following:

-   Request and install the latest version of the Software Asset Management -SaaS License Management application from the [ServiceNow Store](https://store.servicenow.com/). For more information, see [Request SaaS License Management](../task/request-saas-license-management.md).
-   Install the Agent Client Collector for Visibility - Content \(ACC-VC\) product version 1.3.0 or later.

This report helps you manage your shadow IT spend more effectively by viewing all the users who access these applications, the usage of these applications, and how long each application has been used.

**Note:** By default, the SaaS detection report displays data from the past 90 days.

To view this report, navigate to **Software Asset Workspace** &gt; **License usage** &gt; **Reports**.

The SaaS detection report includes domain-separated data when Domain Support - Domain Extensions Installer \(com.glide.domain.msp\_extensions.installer\) and Performance Analytics - Domain Support \(com.snc.pa.domain\_support\) are activated.

<table id="table_a2h_lbt_qzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Product

</td><td>

The name of the SaaS application that is being discovered.

</td></tr><tr><td>

Publisher

</td><td>

Publisher of the SaaS application.Publisher is a reference to the Software Publishers \[samp\_sw\_publisher\] table.

</td></tr><tr><td>

Is monitored

</td><td>

Indicates whether ACC-VC is monitoring the product or not.-   If the product is monitored by the ACC-VC application, the Is monitored column value shows as true.
-   If the product isn't monitored by the ACC-VC application, the Is monitored column value shows as false.

</td></tr><tr><td>

Is managed

</td><td>

Indicates whether the product is managed or unmanaged. -   If a software model exists for a product, the Is managed column value shows as true.
-   If a software model doesn't exist for a product, the Is managed column value shows as false.

</td></tr><tr><td>

URL\(s\)

</td><td>

URL or multiple URLs for your SaaS application.

</td></tr><tr><td>

Total users

</td><td>

Total number of users who have accessed the product.Select the value in this column to view more information about the users in the User Usage Data table.

</td></tr><tr><td>

Last accessed time

</td><td>

The time when the product was last accessed by a user.

</td></tr><tr><td>

Total accessed time

</td><td>

Total duration for which the product has been accessed by its users.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Discovered user|User referenced from the Discovered Users \[samp\_discovered\_user\] table.|
|User|User accessing the application.|
|Device|Device or CI from which the user accessed the application.|
|Cost center|Allotted cost center of the user in an organization.|
|Department|Department of the user in an organization.|
|Total accessed time|Total duration for which the application has been accessed by a user.|
|Last accessed time|Last time when the application was accessed by a user.|

**Parent Topic:**[Software Asset Management references](references.md)

