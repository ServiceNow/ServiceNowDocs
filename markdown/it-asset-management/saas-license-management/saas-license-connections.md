---
title: SaaS License Connections
description: Creating a custom integration helps you connect the Software Asset Management application with a SaaS application that doesn't have an existing integration in SaaS License Management.
locale: en-US
release: xanadu
product: SaaS License Management
classification: saas-license-management
topic_type: concept
last_updated: "2025-09-17"
reading_time_minutes: 4
breadcrumb: [SaaS License Management, Software Asset Management, IT Asset Management]
---

# SaaS License Connections

Creating a custom integration helps you connect the Software Asset Management application with a SaaS application that doesn't have an existing integration in SaaS License Management.

The low-code framework uses ServiceNow® Integration Hub and ServiceNow® Flow Designer to connect with a SaaS provider’s API endpoints. You can perform the following actions:

-   Download a list of all users, view meaningful usage data, and optimize your SaaS spend by reclaiming unused subscriptions.
-   Manage your custom SaaS connections along with the base system SaaS connections using Software Asset Management software models and reporting.

## Custom integrations

Install Integration Hub Starter, Standard, Professional, or Enterprise to create a custom integration. For more information about Integration Hub, see [Request IntegrationHub](https://www.servicenow.com/docs/access?context=request-ih-overview&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).

There’s no charge to install Integration Hub plugins on a non-production instance. You can build a custom integration on a non-production instance that has Integration Hub installed, then bring it into your production environment using an update set. For more information about update sets, see [System update sets](https://www.servicenow.com/docs/access?context=system-update-sets&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US). This way, you can validate your custom integrations before putting them in production and you're not charged for an Integration Hub subscription.

**Important:** You can create custom integrations for subscription-based models using User Subscription as the license metric, and for consumption-based models using SaaS Consumption as the license metric.

Some SaaS applications have existing Integration Hub spokes that you can use to create your custom integration. If there's an existing spoke for the SaaS application that you're integrating with, skip the step to create a custom spoke. If you use an existing spoke, you can use some of its data stream actions. Find out what actions are included with the spoke before creating your own actions. For a list of applications that have Integration Hub spokes, see [IntegrationHub available spokes](https://www.servicenow.com/docs/access?context=spokes-list&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).

Building a custom integration with SaaS License Connections requires you to track many different values. Use the [SaaS License Connections Worksheet](https://support.servicenow.com/kb_view.do?sysparm_article=KB0793266) while researching the SaaS API and building your data stream actions to make sure that you have all the information you need.

1.  [Create a custom spoke](../task/create-saas-spoke.md)  
To set up a custom integration in SaaS License Management, create a spoke to connect with a SaaS application.
2.  [Create a custom integration profile](../task/create-integration-custom.md)  
Create a custom integration profile to track software subscriptions and optimize stale licenses for any SaaS application.
3.  [Create a data stream action to get users](../task/create-data-stream-action-slc.md)  
Create a data stream action to get a list of user subscriptions from the SaaS application.
4.  [Create a subflow to get users](../task/create-subflow-get-users.md#)  
Create a subflow to add a list of users to the Software Subscription table.
5.  [Create a data stream action to get user activity](../task/create-data-stream-get-activity.md)  
Create a data stream action to get user activity from a SaaS application.
6.  [Create a subflow to get user activity](../task/create-sublow-get-activity.md)  
Create a subflow to update the Software Subscription table with each user's most recent activity in the SaaS application.
7.  [Create an action to remove a user](../task/create-data-stream-remove-user.md)  
Create an action to deactivate or delete a user account in the SaaS application.
8.  [Create a subflow to reclaim a user](../task/create-subflow-reclaim-user.md)  
Create a subflow to reclaim a user subscription.
9.  [Create a subflow to get license consumption](../task/create-subflow-get-license-consumption.md)  
Create a subflow to add license consumption data to the Subscription Consumption Summaries \[sam\_saas\_consumption\_summary\] table.
10. [Publish a custom integration profile](../task/publish-integration-custom.md)  
Publish a custom integration profile to complete the custom integration.
11. [Create a store app for a custom integration](../task/create-slc-store-app.md)  
Publish your custom integration application on the ServiceNow Store to make it available for others to use.

**Parent Topic:**[SaaS License Management](sam-subscription-management.md)

**Related topics**  


[Request SaaS License Management](../task/request-saas-license-management.md)

[SaaS Overview dashboard](saas-overview-dashboard.md)

[Playbook for SaaS integrations](playbook-saas-integrations.md)

[Integrate with SaaS applications](create-integration-profile.md)

[Integrate with SSO providers](saas-sso-integration.md)

[Create a child alias to set up multiple integration profiles](../task/create-child-alias-saas.md)

[Viewing your SaaS and SSO subscriptions](usage-summary-saas.md)

[Review a software reclamation rule](../task/add-reclamation-rule-sub.md)

[Reclaiming user subscriptions](reclaiming-user-subscriptions-saas.md)

[Disconnect SSO apps](../task/disconnect-azure-ad-apps.md)

[Delete an integration profile](delete-saas-integration.md)

[Subscription identifiers for SaaS and SSO applications](subscription-identifiers.md#)

