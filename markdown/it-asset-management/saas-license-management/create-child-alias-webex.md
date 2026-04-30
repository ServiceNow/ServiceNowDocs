---
title: Create a child alias to set up multiple Cisco Webex integration profiles
description: Create a child alias to set up multiple Cisco Webex integration profiles.
locale: en-US
release: yokohama
product: SaaS License Management
classification: saas-license-management
topic_type: task
last_updated: "2025-06-23"
reading_time_minutes: 3
breadcrumb: [SaaS License Management, Software Asset Management, IT Asset Management]
---

# Create a child alias to set up multiple Cisco Webex integration profiles

Create a child alias to set up multiple Cisco Webex integration profiles.

## Before you begin

Role required: admin

## Procedure

1.  Create a Cisco Webex integration profile.

    For more information about creating an integration profile, see [Integrating with Cisco Webex](../concept/integrate-with-webex-apps.md#).

2.  Open the connection &amp; credential record set on the integration profile.

3.  Open the parent alias record \(sn\_cisco\_teams\_spk.CiscoWebexTeams\).

4.  Set the configuration template to the appropriate template based on the selected process in the profile.

    |Process selected on the profile|Configuration template|
    |-------------------------------|----------------------|
    |Both **Download activity** and **Reclaim subscriptions** check boxes are selected|Webex Subscription Activity and Reclaim|
    |Only **Download activity** check box is selected|Webex Subscription and Activity|
    |Only **Reclaim subscriptions** check box is selected|Webex Subscription and Reclaim|
    |Both **Download activity** and **Reclaim subscriptions** check boxes aren’t selected|Webex Subscription|

5.  Save the parent alias record.

6.  Select the **Child Aliases** tab.

7.  Select **New**.

    **Tip:** If the **New** button isn't visible, change the scope to the respective application of the alias from the application scope.

8.  Reload the Connection &amp; Credential Aliases page.

9.  On the new child alias form that opens up, provide a name of your choice for the alias.

10. Select **Submit**.

11. Open the child alias record that you created, select **Create New Connection &amp; Credential**.

12. Configure the connection and credential in the same way that you have done for the parent integration.

13. After the connection is configured, return to the integration profile and then select the newly created child alias on the **Connection &amp; Credential** field.

14. Select **Save** and publish the integration profile.


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

[Create a child alias to set up multiple Confluence Cloud integration profiles](create-child-alias-confluence.md)

[Create a child alias to set up multiple Jira integration profiles](create-child-alias-jira.md)

[Create a child alias to set up multiple Slack workspace integration profiles](create-child-alias-slack-ws.md)

[Associate a user with subscription records](map-user-data.md)

[Disconnect SSO apps](disconnect-azure-ad-apps.md)

[Delete an integration profile](../concept/delete-saas-integration.md)

[Subscription identifiers for SaaS and SSO applications](../concept/subscription-identifiers.md#)

