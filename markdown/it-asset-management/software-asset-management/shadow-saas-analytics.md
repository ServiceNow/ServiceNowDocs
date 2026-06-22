---
title: SaaS detection report
description: Use the SaaS detection report to discover and manage all SaaS applications accessed via a browser and configured within the ServiceNow Agent Client Collector for Visibility - Content \(ACC-VC\) product. The SaaS applications that can be managed through this report can be paid or free ones.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-asset-management/software-asset-management/shadow-saas-analytics.html
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

-   Request and install the latest version of the Software Asset Management -SaaS License Management application from the [ServiceNow Store](https://store.servicenow.com/). For more information, see [Request SaaS License Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/saas-license-management/request-saas-license-management.md).
-   Install the Agent Client Collector for Visibility - Content \(ACC-VC\) product version 1.9.0 or later. For more information, see [Agent Client Collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/agent-client-collector/acc-landing-page.md).

You can use this report to manage shadow IT spend by viewing all the users who access these applications and their usage patterns. You can also see how long each application has been in use.

**Note:**

-   The data in the SaaS detection report reflects ACC-VC’s retention period, which is 30 days by default. The default value can be modified as needed.
-   SaaS URL data in the SaaS detection report are read-only and can't be edited directly from the report.

View this report by navigating to **Software Asset Workspace** &gt; **License usage** &gt; **Reports**. Additionally, you can view URL details on the URL Discovery Insights dashboard in the Discovery Admin Workspace. For further information, see [URL Discovery Insights dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/discovery/url-disco-insights.md).

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

Indicates whether ACC-VC is monitoring the product or not.-   If the product is monitored by the ACC-VC application, the Is monitored value is true.
-   If the product isn't monitored by the ACC-VC application, the Is monitored value is false.

</td></tr><tr><td>

Managed status

</td><td>

Indicates whether the product is managed or unmanaged. -   If a software model exists for a product, the status is Managed.
-   If a software model doesn't exist for a product, the status is Unmanaged.

</td></tr><tr><td>

URL\(s\)

</td><td>

URL or multiple URLs for your SaaS application.

</td></tr><tr><td>

Total users

</td><td>

Total number of users who have accessed the product.

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
|User ID|User ID of the person who is accessing the application.|
|Device|Device or CI that is used to access the application.|
|Date|Last date when the application was accessed.|
|Total usage time|Total duration for which the application has been accessed by a user.|
|Domain|Domain URL for the application.|

**Parent Topic:**[Software Asset Management references](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/software-asset-management/references.md)

