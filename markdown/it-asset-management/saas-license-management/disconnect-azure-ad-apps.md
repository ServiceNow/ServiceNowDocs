---
title: Disconnect SSO apps
description: Disconnect an SSO application to stop viewing subscription information for the app, or before creating a direct integration for the app.
locale: en-US
release: zurich
product: SaaS License Management
classification: saas-license-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
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

[SaaS License Management setup for large companies](../concept/saas-setup-large-companies.md)

[SaaS Overview dashboard](../concept/saas-overview-dashboard.md)

[Integrate with SaaS applications](../concept/create-integration-profile.md)

[Integrate with SSO providers](../concept/saas-sso-integration.md)

[Playbook for SaaS integrations](../concept/playbook-saas-integrations.md)

[Viewing your SaaS and SSO subscriptions](../concept/usage-summary-saas.md)

[Review a software reclamation rule](add-reclamation-rule-sub.md)

[Reclaiming user subscriptions](../concept/reclaiming-user-subscriptions-saas.md)

[Create a child alias to set up multiple integration profiles](../reuse/create-child-alias-saas.md)

[Create a child alias to set up multiple Cisco Webex integration profiles](create-child-alias-webex.md)

[Create a child alias to set up multiple Confluence Cloud integration profiles](create-child-alias-confluence.md)

[Create a child alias to set up multiple Jira integration profiles](create-child-alias-jira.md)

[Create a child alias to set up multiple Slack workspace integration profiles](create-child-alias-slack-ws.md)

[Associate a user with subscription records](map-user-data.md)

[Delete an integration profile](../concept/delete-saas-integration.md)

[Subscription identifiers for SaaS and SSO applications](../concept/subscription-identifiers.md#)

[Subscription exclusions for SaaS and SSO applications](../concept/subscription-exclusions.md#)

