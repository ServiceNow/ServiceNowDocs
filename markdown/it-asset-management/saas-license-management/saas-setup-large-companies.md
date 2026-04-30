---
title: SaaS License Management setup for large companies
description: Set up SaaS License Management for large companies to confirm that you can view all SaaS usage data in your ServiceNow instance.
locale: en-US
release: xanadu
product: SaaS License Management
classification: saas-license-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Request SaaS License Management, SaaS License Management, Software Asset Management, IT Asset Management]
---

# SaaS License Management setup for large companies

Set up SaaS License Management for large companies to confirm that you can view all SaaS usage data in your ServiceNow instance.

Some large companies must update the **com.snc.pa.dc.max\_row\_count\_indicator\_source** system property before creating integration profiles. If either of the following conditions is true for your company, an admin must update this property.

-   If there are more than 50,000 user subscriptions for the [SaaS applications](create-integration-profile.md), excluding the subscriptions for [Adobe Cloud](adobe-cloud-integration.md) and [Microsoft 365](integrate-with-microsoft.md#).
-   If there are more than 50,000 user subscriptions for Adobe Cloud and Microsoft 365 combined.

Update the **com.snc.pa.dc.max\_row\_count\_indicator\_source** system property to be the greater value between your subscriptions for the two groups. For example, if you have 60,000 user subscriptions for [SaaS applications](create-integration-profile.md) combined and 25,000 user subscriptions for [Adobe Cloud](adobe-cloud-integration.md) and [Microsoft 365](integrate-with-microsoft.md#) combined, update the property to be `60,000`.

**Note:** For more information about how to use the **com.snc.pa.dc.max\_row\_count\_indicator\_source** property, see [Data collector properties](https://www.servicenow.com/docs/access?context=pa-properties&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US).

**Parent Topic:**[Request SaaS License Management](../task/request-saas-license-management.md)

