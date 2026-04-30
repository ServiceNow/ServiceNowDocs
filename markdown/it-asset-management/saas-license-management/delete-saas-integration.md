---
title: Delete an integration profile
description: If your company stops using a SaaS application or SSO provider, you can delete the integration profile.
locale: en-US
release: xanadu
product: SaaS License Management
classification: saas-license-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [SaaS License Management, Software Asset Management, IT Asset Management]
---

# Delete an integration profile

If your company stops using a SaaS application or SSO provider, you can delete the integration profile.

To delete an integration profile, navigate to the integration profile record and click **Delete**. The sam\_integrator role is required to delete integration profiles.

## Direct integrations

When you delete a direct integration profile, all subscriptions, scheduled jobs, and consumption summaries for the integration are also deleted. Open reclamation candidates are updated to Closed Skipped. Reclamation rules are not deleted.

## SSO integrations

When you delete an SSO integration profile, all SSO applications, subscriptions, and scheduled jobs for the integration are also deleted. Open reclamation candidates are updated to Closed Skipped. Reclamation rules are not deleted.

An SSO integration is created using a directory integration. When you delete an SSO integration profile, the directory integration \(including directory jobs, directory users, and directory groups\) is not deleted. Before deleting a directory integration, make sure it is not being used by additional connections, such as [Microsoft Azure AD integration for new hire onboarding](https://www.servicenow.com/docs/access?context=azure-active-directory-integration-for-new-hire-onboarding&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US). The sn\_remote\_dir\_sync.admin role is required to delete directory integrations.

**Parent Topic:**[SaaS License Management](sam-subscription-management.md)

**Related topics**  


[Request SaaS License Management](../task/request-saas-license-management.md)

[SaaS Overview dashboard](saas-overview-dashboard.md)

[Playbook for SaaS integrations](playbook-saas-integrations.md)

[Integrate with SaaS applications](create-integration-profile.md)

[Integrate with SSO providers](saas-sso-integration.md)

[Create a child alias to set up multiple integration profiles](../task/create-child-alias-saas.md)

[Viewing your SaaS and SSO subscriptions](usage-summary-saas.md)

[SaaS License Connections](saas-license-connections.md)

[Review a software reclamation rule](../task/add-reclamation-rule-sub.md)

[Reclaiming user subscriptions](reclaiming-user-subscriptions-saas.md)

[Disconnect SSO apps](../task/disconnect-azure-ad-apps.md)

[Subscription identifiers for SaaS and SSO applications](subscription-identifiers.md#)

