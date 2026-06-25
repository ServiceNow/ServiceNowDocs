---
title: Create a child alias to set up multiple Confluence Cloud integration profiles
description: Create a child alias to set up multiple Confluence Cloud integration profiles.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/saas-license-management/create-child-alias-confluence.html
release: australia
product: SaaS License Management
classification: saas-license-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [SaaS License Management, Software Asset Management, IT Asset Management]
---

# Create a child alias to set up multiple Confluence Cloud integration profiles

Create a child alias to set up multiple Confluence Cloud integration profiles.

## Before you begin

Role required: sam\_integrator

## Procedure

1.  Create a Confluence Cloud integration profile.

    For more information about creating an integration profile, see [Integrating with Confluence Cloud](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/saas-license-management/integrate-with-confluence-cloud.md).

2.  Open the connection &amp; credential record set on the integration profile.

3.  Open the parent alias record \(sn\_conflunce\_spoke.Confluence\_Cloud\).

4.  Set the configuration template to the appropriate template based on the selected process in the profile.

    |Process selected on the profile|Configuration template|
    |-------------------------------|----------------------|
    |Both **Download activity** and **Reclaim subscriptions** check boxes are selected|Confluence Subscription Activity and Reclaim|
    |Only **Download activity** check box is selected|Confluence Subscription and Activity|
    |Only **Reclaim subscriptions** check box is selected|Confluence Subscription and Reclaim|
    |Both **Download activity** and **Reclaim subscriptions** check boxes aren’t selected|Confluence Subscription|

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

[Create a child alias to set up multiple Jira integration profiles]()

[Associate a user with subscription records]()

[Disconnect SSO apps]()

[Delete an integration profile]()

[Subscription identifiers for SaaS and SSO applications]()

[Subscription exclusions for SaaS and SSO applications]()

