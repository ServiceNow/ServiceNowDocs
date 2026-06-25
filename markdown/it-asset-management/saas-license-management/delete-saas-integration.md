---
title: Delete an integration profile
description: If your company stops using a SaaS application or SSO provider, you can delete the integration profile.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/saas-license-management/delete-saas-integration.html
release: australia
product: SaaS License Management
classification: saas-license-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [SaaS License Management, Software Asset Management, IT Asset Management]
---

# Delete an integration profile

If your company stops using a SaaS application or SSO provider, you can delete the integration profile.

To delete an integration profile, navigate to the integration profile record and click **Delete**. The sam\_integrator role is required to delete integration profiles.

## Direct integrations

When you delete a direct integration profile, all subscriptions, scheduled jobs, and consumption summaries for the integration are also deleted. Open reclamation candidates are updated to Closed Skipped. Reclamation rules are not deleted.

## SSO integrations

When you delete an SSO integration profile, all SSO applications, subscriptions, and scheduled jobs for the integration are also deleted. Open reclamation candidates are updated to Closed Skipped. Reclamation rules are not deleted.

An SSO integration is created using a directory integration. When you delete an SSO integration profile, the directory integration \(including directory jobs, directory users, and directory groups\) is not deleted. Before deleting a directory integration, make sure it is not being used by additional connections, such as [Microsoft Azure AD integration for new hire onboarding](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/azure-active-directory-integration-for-new-hire-onboarding.md). The sn\_remote\_dir\_sync.admin role is required to delete directory integrations.

**Parent Topic:**[SaaS License Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/saas-license-management/sam-subscription-management.md)

**Related topics**  


[Request SaaS License Management]()

[SaaS License Management setup for large companies]()

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

[Subscription identifiers for SaaS and SSO applications]()

[Subscription exclusions for SaaS and SSO applications]()

