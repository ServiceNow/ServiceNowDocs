---
title: SaaS License Management setup for large companies
description: Set up SaaS License Management for large companies to confirm that you can view all SaaS usage data in your ServiceNow instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/saas-license-management/saas-setup-large-companies.html
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

-   If there are more than 50,000 user subscriptions for the [SaaS applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/saas-license-management/create-integration-profile.md), excluding the subscriptions for [Adobe Cloud](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/adobe-cloud-integration.md) and [Microsoft 365](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/integrate-with-microsoft.md).
-   If there are more than 50,000 user subscriptions for Adobe Cloud and Microsoft 365 combined.

Update the **com.snc.pa.dc.max\_row\_count\_indicator\_source** system property to be the greater value between your subscriptions for the two groups. For example, if you have 60,000 user subscriptions for [SaaS applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/saas-license-management/create-integration-profile.md) combined and 25,000 user subscriptions for [Adobe Cloud](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/adobe-cloud-integration.md) and [Microsoft 365](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/integrate-with-microsoft.md) combined, update the property to be `60,000`.

**Note:** For more information about how to use the **com.snc.pa.dc.max\_row\_count\_indicator\_source** property, see [Data collector properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/pa-properties.md).

**Parent Topic:**[SaaS License Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/saas-license-management/sam-subscription-management.md)

**Related topics**  


[Request SaaS License Management]()

[SaaS Overview dashboard]()

[Integrate with SaaS applications]()

[Integrate with SSO providers]()

[Playbook for SaaS integrations]()

[Viewing your SaaS and SSO subscriptions]()

[Review a software reclamation rule]()

[Reclaiming user subscriptions]()

[Create a child alias to set up multiple integration profiles]()

[Create a child alias to set up multiple Cisco Webex integration profiles]()

[Create a child alias to set up multiple Confluence Cloud integration profiles]()

[Create a child alias to set up multiple Jira integration profiles]()

[Associate a user with subscription records]()

[Disconnect SSO apps]()

[Delete an integration profile]()

[Subscription identifiers for SaaS and SSO applications]()

[Subscription exclusions for SaaS and SSO applications]()

