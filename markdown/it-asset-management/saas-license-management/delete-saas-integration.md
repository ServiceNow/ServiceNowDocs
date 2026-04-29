---
title: Delete an integration profile
description: If your company stops using a SaaS application or SSO provider, you can delete the integration profile.
locale: en-US
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

An SSO integration is created using a directory integration. When you delete an SSO integration profile, the directory integration \(including directory jobs, directory users, and directory groups\) is not deleted. Before deleting a directory integration, make sure it is not being used by additional connections, such as [Microsoft Azure AD integration for new hire onboarding](https://www.servicenow.com/docs/access?context=azure-active-directory-integration-for-new-hire-onboarding&version=australia&pubname=australia-employee-service-management&ft:locale=en-US). The sn\_remote\_dir\_sync.admin role is required to delete directory integrations.

**Parent Topic:**[SaaS License Management](sam-subscription-management.md)

**Related topics**  


[Request SaaS License Management](../task/request-saas-license-management.md)

[SaaS License Management setup for large companies](saas-setup-large-companies.md)

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

[Subscription identifiers for SaaS and SSO applications](subscription-identifiers.md#)

[Subscription exclusions for SaaS and SSO applications](subscription-exclusions.md#)

