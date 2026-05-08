---
title: SaaS License Connections
description: Creating a custom integration helps you connect the Software Asset Management application with a SaaS application that doesn't have an existing integration in SaaS License Management.
locale: en-US
release: australia
product: SaaS License Management
classification: saas-license-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [SaaS License Management, Software Asset Management, IT Asset Management]
---

# SaaS License Connections

Creating a custom integration helps you connect the Software Asset Management application with a SaaS application that doesn't have an existing integration in SaaS License Management.

The low-code framework uses ServiceNow® Integration Hub and ServiceNow® Flow Designer to connect with a SaaS provider’s API endpoints. You can perform the following actions:

-   Download a list of all users, view meaningful usage data, and optimize your SaaS spend by reclaiming unused subscriptions.
-   Manage your custom SaaS connections along with the base system SaaS connections using Software Asset Management software models and reporting.

## Custom integrations

Install Integration Hub Starter, Standard, Professional, or Enterprise to create a custom integration. For more information about Integration Hub, see Request IntegrationHub.

There’s no charge to install Integration Hub plugins on a non-production instance. You can build a custom integration on a non-production instance that has Integration Hub installed, then bring it into your production environment using an update set. For more information about update sets, see System update sets. This way, you can validate your custom integrations before putting them in production and you're not charged for an Integration Hub subscription.

**Important:** You can create custom integrations for subscription-based models using User Subscription as the license metric, and for consumption-based models using SaaS Consumption as the license metric.

Some SaaS applications have existing Integration Hub spokes that you can use to create your custom integration. If there's an existing spoke for the SaaS application that you're integrating with, skip the step to create a custom spoke. If you use an existing spoke, you can use some of its data stream actions. Find out what actions are included with the spoke before creating your own actions. For a list of applications that have Integration Hub spokes, see IntegrationHub available spokes.

Building a custom integration with SaaS License Connections requires you to track many different values. Use the [SaaS License Connections Worksheet](https://support.servicenow.com/kb_view.do?sysparm_article=KB0793266) while researching the SaaS API and building your data stream actions to make sure that you have all the information you need.

