---
title: SaaS License Management setup for large companies
description: Set up SaaS License Management for large companies to confirm that you can view all SaaS usage data in your ServiceNow instance.
locale: en-US
release: australia
product: SaaS License Management
classification: saas-license-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [SaaS License Management, Software Asset Management, IT Asset Management]
---

# SaaS License Management setup for large companies

Set up SaaS License Management for large companies to confirm that you can view all SaaS usage data in your ServiceNow instance.

Some large companies must update the **com.snc.pa.dc.max\_row\_count\_indicator\_source** system property before creating integration profiles. If either of the following conditions is true for your company, an admin must update this property.

-   If there are more than 50,000 user subscriptions for the [SaaS applications](create-integration-profile.md), excluding the subscriptions for [Adobe Cloud](adobe-cloud-integration.md) and [Microsoft 365](integrate-with-microsoft.md).
-   If there are more than 50,000 user subscriptions for Adobe Cloud and Microsoft 365 combined.

Update the **com.snc.pa.dc.max\_row\_count\_indicator\_source** system property to be the greater value between your subscriptions for the two groups. For example, if you have 60,000 user subscriptions for [SaaS applications](create-integration-profile.md) combined and 25,000 user subscriptions for [Adobe Cloud](adobe-cloud-integration.md) and [Microsoft 365](integrate-with-microsoft.md) combined, update the property to be `60,000`.

**Note:** For more information about how to use the **com.snc.pa.dc.max\_row\_count\_indicator\_source** property, see [Data collector properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/pa-properties.md).

**Parent Topic:**[SaaS License Management](sam-subscription-management.md)

**Related topics**  


[Request SaaS License Management](../task/request-saas-license-management.md)

[SaaS Overview dashboard](saas-overview-dashboard.md)

[Integrate with SaaS applications](create-integration-profile.md)

[Integrate with SSO providers](saas-sso-integration.md)

[Playbook for SaaS integrations](playbook-saas-integrations.md)

[Viewing your SaaS and SSO subscriptions](usage-summary-saas.md)

[Review a software reclamation rule](../task/add-reclamation-rule-sub.md)

[Reclaiming user subscriptions](reclaiming-user-subscriptions-saas.md)

[Create a child alias to set up multiple integration profiles](../reuse/create-child-alias-saas.md)

[Create a child alias to set up multiple Cisco Webex integration profiles](../task/create-child-alias-webex.md)

[Create a child alias to set up multiple Confluence Cloud integration profiles](../task/create-child-alias-confluence.md)

[Create a child alias to set up multiple Jira integration profiles](../task/create-child-alias-jira.md)

[Associate a user with subscription records](../task/map-user-data.md)

[Disconnect SSO apps](../task/disconnect-azure-ad-apps.md)

[Delete an integration profile](delete-saas-integration.md)

[Subscription identifiers for SaaS and SSO applications](subscription-identifiers.md#)

[Subscription exclusions for SaaS and SSO applications](subscription-exclusions.md#)

