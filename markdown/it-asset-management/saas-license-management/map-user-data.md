---
title: Associate a user with subscription records
description: If the User field in the Software Subscription \[samp\_sw\_subscription\] table is empty, map the field with an associated user in the User \[sys\_user\] table within ServiceNow AI Platform.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/saas-license-management/map-user-data.html
release: australia
product: SaaS License Management
classification: saas-license-management
topic_type: task
last_updated: "2026-06-25"
reading_time_minutes: 4
keywords: [user resolution, map user data, user field empty, unresolved subscriptions]
breadcrumb: [SaaS License Management, Software Asset Management, IT Asset Management]
---

# Associate a user with subscription records

If the **User** field in the Software Subscription \[samp\_sw\_subscription\] table is empty, map the field with an associated user in the User \[sys\_user\] table within ServiceNow AI Platform.

## Before you begin

ServiceNow Role required: sam\_admin or sam\_integrator

**Important:** sam\_user can view the user resolution rules but not create them.

Review the list of unresolved subscriptions on the Subscriptions without user page in the [License operations view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/operations-workspace.md). Note the User principal name value for the subscription and then verify if this value matches any entry in the User \[sys\_user\] table. If no match is found, configure the rule accordingly.

## About this task

SaaS integrations create subscription records in the Software Subscription \[samp\_sw\_subscription\] table with fields populated by automated jobs and integrations. By default, the **User** field is resolved by matching the User principal name column value with the **Email** and **User ID** fields in the User \[sys\_user\] table. To accurately map user data when user data isn't resolved, create a user resolution rule.

## Procedure

1.  Navigate to **Workspaces** &gt; **Software Asset Workspace** &gt; **License operations** &gt; **User subscription** &gt; **User resolution rules**.

2.  Select **New**.

3.  On the form, fill in the fields.

    For a description of the field values, see [User resolution rule fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/user-resolution-rule-fields.md).

4.  Select **Save**.


## Result

If the user resolution rule is correctly configured and the Download subscription job **SAM - Refresh &lt;profile name&gt; Subscriptions** runs successfully, the unresolved subscription you targeted is cleared from the Subscriptions without user page in [License operations view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/operations-workspace.md).

If you find multiple records with the same email address but different User IDs and associated user classes, enable the system property **sn\_itam\_samp.user\_resolution\_exclude\_table**. Provide a list of comma-separated table names that extend the User \[sys\_user\] table to exclude them from user resolution. After making these changes, rerun the Download Subscription job **SAM - Refresh &lt;profile name&gt; Subscriptions** to associate users with their subscription records.

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

[Disconnect SSO apps]()

[Delete an integration profile]()

[Subscription identifiers for SaaS and SSO applications]()

[Subscription exclusions for SaaS and SSO applications]()

