---
title: Create a child alias to set up multiple integration profiles
description: Create a child alias to set up multiple integration profiles with unique connections and manage different configurations for each integration profile.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/saas-license-management/create-child-alias-saas.html
release: australia
product: SaaS License Management
classification: saas-license-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [SaaS License Management, Software Asset Management, IT Asset Management]
---

# Create a child alias to set up multiple integration profiles

Create a child alias to set up multiple integration profiles with unique connections and manage different configurations for each integration profile.

## Before you begin

Role required: sam\_integrator

## Procedure

1.  Create an integration profile.

    For more information about creating an integration profile, see [Integrate with SaaS applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/saas-license-management/create-integration-profile.md).

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

[Create a child alias to set up multiple Cisco Webex integration profiles]()

[Create a child alias to set up multiple Confluence Cloud integration profiles]()

[Create a child alias to set up multiple Jira integration profiles]()

[Associate a user with subscription records]()

[Disconnect SSO apps]()

[Delete an integration profile]()

[Subscription identifiers for SaaS and SSO applications]()

[Subscription exclusions for SaaS and SSO applications]()

