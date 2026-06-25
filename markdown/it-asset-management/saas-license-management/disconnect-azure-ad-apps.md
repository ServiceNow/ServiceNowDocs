---
title: Disconnect SSO apps
description: Disconnect an SSO application to stop viewing subscription information for the app, or before creating a direct integration for the app.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/saas-license-management/disconnect-azure-ad-apps.html
release: australia
product: SaaS License Management
classification: saas-license-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [SaaS License Management, Software Asset Management, IT Asset Management]
---

# Disconnect SSO apps

Disconnect an SSO application to stop viewing subscription information for the app, or before creating a direct integration for the app.

## Before you begin

Role required: sam\_integrator

## About this task

SaaS License Management offers direct integrations with select applications. Direct integrations provide the most robust usage data. For a list of available direct integrations, see [Integrate with SaaS applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/saas-license-management/create-integration-profile.md). If you have a connected SSO app and want to replace it with a direct integration, disconnect the app before creating the direct integration to avoid creating duplicate subscription records for the app.

When an app is disconnected, all SSO subscriptions for the app are deleted and any open reclamation candidates are set to Closed Skipped.

## Procedure

1.  Navigate to **All** &gt; **SaaS License** &gt; **SSO Applications**.

2.  Click the application you want to disconnect.

3.  Click **Disconnect**.

    **Tip:** You can also disconnect multiple apps at once from the **SSO Applications** list. Select the apps using the check box on the left side of the list. At the bottom of the list, click the **Actions on selected rows** drop down menu and then click **Disconnect**.


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

[Delete an integration profile]()

[Subscription identifiers for SaaS and SSO applications]()

[Subscription exclusions for SaaS and SSO applications]()

