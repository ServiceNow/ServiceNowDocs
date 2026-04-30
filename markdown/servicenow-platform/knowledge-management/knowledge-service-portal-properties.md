---
title: Knowledge Management Service Portal properties
description: Knowledge Management Service Portal properties determine how information is displayed on the Knowledge portal. You must have the admin role to set configuration properties.
locale: en-US
release: yokohama
product: Knowledge Management
classification: knowledge-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Knowledge Management reference, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Knowledge Management Service Portal properties

Knowledge Management Service Portal properties determine how information is displayed on the Knowledge portal. You must have the admin role to set configuration properties.

The following system properties are set to direct users to the Knowledge Management Service Portal homepage, and to specify the URL suffix for the homepage.

<table id="table_jzs_2kx_kt"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**sn\_km\_portal.glide.knowman.serviceportal.enable\_redirect**

</td><td>

Directs users to the desired Knowledge homepage. -   Type: true\|false
-   Default value: false

 Set to **true** to redirect users navigating to v2 or v3 pages to the Knowledge Management Service Portal homepage.

 **Note:** This property is not honored for the following use cases:

-   Contextual search in the Incident form
-   Connect
-   Global search

</td></tr><tr><td>

**sn\_km\_portal.glide.knowman.serviceportal.portal\_url**

</td><td>

The URL suffix for the Knowledge Management Service Portal. The default is **kb**.

</td></tr></tbody>
</table>The Knowledge Management Service Portal supports the [Knowledge Management V3 properties](r_KnowledgeProperties.md#). Configuring widget instance options on the portal pages can override these properties.

**Note:**

Starting with the Washington DC release, the Knowledge Management v3 homepage \(com.snc.knowledge3\) is being prepared for deprecation in the future Y release. It is replaced by the Knowledge Management Service Portal \(com.snc.knowledge\_serviceportal\), which is active by default for customers on Madrid and later releases. For more information about the new experience, see [Knowledge Management Service Portal homepage features](../concept/knowledge-service-portal-pages.md).

