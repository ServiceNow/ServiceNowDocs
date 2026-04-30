---
title: Create a child alias to set up multiple integration profiles
description: Create a child alias to set up multiple integration profiles with unique connections and manage different configurations for each integration profile.
locale: en-US
release: xanadu
product: SaaS License Management
classification: saas-license-management
topic_type: task
last_updated: "2024-11-18"
reading_time_minutes: 3
breadcrumb: [SaaS License Management, Software Asset Management, IT Asset Management]
---

# Create a child alias to set up multiple integration profiles

Create a child alias to set up multiple integration profiles with unique connections and manage different configurations for each integration profile.

## Before you begin

Role required: admin or sam\_integrator

## Procedure

1.  Create an integration profile.

    For more information about creating an integration profile, see [Integrate with SaaS applications](../concept/create-integration-profile.md).

2.  Open the connection &amp; credential record set on the integration profile.

    If the **Parent Alias** field on an alias is empty, then the alias is a parent. If the field is filled, then the alias is a child of the alias specified in the **Parent Alias** field.

    -   If the record is a parent alias, select the **Child Aliases** tab.
    -   If the record is a child alias, select the **Parent Alias** record and then select the **Child Aliases** tab.
3.  Select **New**.

    **Tip:** If the **New** button isn't visible, change the scope to the respective application of the alias from the application scope.

4.  Reload the Connection &amp; Credential Aliases page.

5.  On the new child alias form that opens up, provide a name of your choice for the alias.

6.  Select **Submit**.

7.  Open the child alias record that you created, select **Create New Connection &amp; Credential**.

8.  Configure the connection and credential in the same way that you have done for the parent integration.

9.  After the connection is configured, return to the integration profile and then select the newly created child alias on the **Connection &amp; Credential** field.

10. Select **Save** and publish the integration profile.


**Parent Topic:**[SaaS License Management](../concept/sam-subscription-management.md)

**Related topics**  


[Request SaaS License Management](request-saas-license-management.md)

[SaaS Overview dashboard](../concept/saas-overview-dashboard.md)

[Playbook for SaaS integrations](../concept/playbook-saas-integrations.md)

[Integrate with SaaS applications](../concept/create-integration-profile.md)

[Integrate with SSO providers](../concept/saas-sso-integration.md)

[Viewing your SaaS and SSO subscriptions](../concept/usage-summary-saas.md)

[SaaS License Connections](../concept/saas-license-connections.md)

[Review a software reclamation rule](add-reclamation-rule-sub.md)

[Reclaiming user subscriptions](../concept/reclaiming-user-subscriptions-saas.md)

[Disconnect SSO apps](disconnect-azure-ad-apps.md)

[Delete an integration profile](../concept/delete-saas-integration.md)

[Subscription identifiers for SaaS and SSO applications](../concept/subscription-identifiers.md#)

