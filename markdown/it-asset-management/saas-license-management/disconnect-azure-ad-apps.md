---
title: Disconnect SSO apps
description: Disconnect an SSO application to stop viewing subscription information for the app, or before creating a direct integration for the app.
locale: en-US
release: xanadu
product: SaaS License Management
classification: saas-license-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [SaaS License Management, Software Asset Management, IT Asset Management]
---

# Disconnect SSO apps

Disconnect an SSO application to stop viewing subscription information for the app, or before creating a direct integration for the app.

## Before you begin

Role required: sam\_integrator

## About this task

SaaS License Management offers direct integrations with select applications. Direct integrations provide the most robust usage data. For a list of available direct integrations, see [Integrate with SaaS applications](../concept/create-integration-profile.md). If you have a connected SSO app and want to replace it with a direct integration, disconnect the app before creating the direct integration to avoid creating duplicate subscription records for the app.

When an app is disconnected, all SSO subscriptions for the app are deleted and any open reclamation candidates are set to Closed Skipped.

## Procedure

1.  Navigate to **All** &gt; **SaaS License** &gt; **SSO Applications**.

2.  Click the application you want to disconnect.

3.  Click **Disconnect**.

    **Tip:** You can also disconnect multiple apps at once from the **SSO Applications** list. Select the apps using the check box on the left side of the list. At the bottom of the list, click the **Actions on selected rows** drop down menu and then click **Disconnect**.


**Parent Topic:**[SaaS License Management](../concept/sam-subscription-management.md)

**Related topics**  


[Request SaaS License Management](request-saas-license-management.md)

[SaaS Overview dashboard](../concept/saas-overview-dashboard.md)

[Playbook for SaaS integrations](../concept/playbook-saas-integrations.md)

[Integrate with SaaS applications](../concept/create-integration-profile.md)

[Integrate with SSO providers](../concept/saas-sso-integration.md)

[Create a child alias to set up multiple integration profiles](create-child-alias-saas.md)

[Viewing your SaaS and SSO subscriptions](../concept/usage-summary-saas.md)

[SaaS License Connections](../concept/saas-license-connections.md)

[Review a software reclamation rule](add-reclamation-rule-sub.md)

[Reclaiming user subscriptions](../concept/reclaiming-user-subscriptions-saas.md)

[Delete an integration profile](../concept/delete-saas-integration.md)

[Subscription identifiers for SaaS and SSO applications](../concept/subscription-identifiers.md#)

