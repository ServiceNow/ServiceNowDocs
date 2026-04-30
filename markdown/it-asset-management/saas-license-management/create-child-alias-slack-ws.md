---
title: Create a child alias to set up multiple Slack workspace integration profiles
description: Create a child alias to set up multiple Slack workspace integration profiles.
locale: en-US
release: yokohama
product: SaaS License Management
classification: saas-license-management
topic_type: task
last_updated: "2026-03-04"
reading_time_minutes: 4
breadcrumb: [SaaS License Management, Software Asset Management, IT Asset Management]
---

# Create a child alias to set up multiple Slack workspace integration profiles

Create a child alias to set up multiple Slack workspace integration profiles.

## Before you begin

Role required: admin

## Procedure

1.  Create a Slack workspace integration profile.

    For more information about creating an integration profile, see [Integrating with Slack](../concept/integrate-with-slack.md#).

2.  Open the connection &amp; credential record set on the integration profile.

3.  Open the parent alias record \(sn\_slack\_ah\_v2.Slack\_Enterprise\).

4.  Select the **Child Aliases** tab.

5.  Select **New**.

    **Tip:** If the **New** button isn't visible, change the scope to the respective application of the child alias by navigating to the **Application scope** and reloading the Connection &amp; Credential Aliases page.

6.  On the new child alias form that opens up, provide a name for the child alias.

7.  Select **Submit**.

8.  Open the child alias record that you created and select the **Create New Connection &amp; Credential** related link.

9.  In the Create Connection and Credential dialog box, fill in or verify the following fields.

    |Field|Value|
    |-----|-----|
    |Name|Name of the Slack workspace connection.|
    |OAuth Client ID|Client ID that is assigned to your Slack workspace application. Enter the same client ID that you copied in [Create a Slack workspace application](../concept/integrate-with-slack.md#).|
    |OAuth Client Secret|Client secret that is assigned to your Slack workspace application. Enter the same client secret that you copied in [Create a Slack workspace application](../concept/integrate-with-slack.md#).|
    |OAuth Redirect URL|Redirect URL for your Slack workspace application. This field populates automatically.|

10. Select **Configure and Get OAuth Token**.

11. In the Authorize App dialog box, select **Allow**.

    The OAuth access token becomes available for authorizing your Slack workspace connection.

12. Repeat steps 5 to 11 to create child aliases for additional workspace connections.

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

[Create a child alias to set up multiple Cisco Webex integration profiles](create-child-alias-webex.md)

[Create a child alias to set up multiple Confluence Cloud integration profiles](create-child-alias-confluence.md)

[Create a child alias to set up multiple Jira integration profiles](create-child-alias-jira.md)

[Associate a user with subscription records](map-user-data.md)

[Disconnect SSO apps](disconnect-azure-ad-apps.md)

[Delete an integration profile](../concept/delete-saas-integration.md)

[Subscription identifiers for SaaS and SSO applications](../concept/subscription-identifiers.md#)

