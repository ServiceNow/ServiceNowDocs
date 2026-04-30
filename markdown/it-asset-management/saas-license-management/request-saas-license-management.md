---
title: Request SaaS License Management
description: Request the Software Asset Management - SaaS License Management plugin \(sn\_sam\_saas\_int\) so that you can create and manage integrations with your SaaS and Single Sign-on \(SSO\) applications. You can use these integrations to track license usage and to reclaim unused licenses.
locale: en-US
release: xanadu
product: SaaS License Management
classification: saas-license-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [SaaS License Management, Software Asset Management, IT Asset Management]
---

# Request SaaS License Management

Request the Software Asset Management - SaaS License Management plugin \(sn\_sam\_saas\_int\) so that you can create and manage integrations with your SaaS and Single Sign-on \(SSO\) applications. You can use these integrations to track license usage and to reclaim unused licenses.

## Before you begin

Activate the ServiceNow Software Asset Management Professional plugin \(com.snc.samp\) on your ServiceNow instance. For more information on how to request and activate the Software Asset Management Professional plugin \(com.snc.samp\), see [Request Software Asset Management](t_RequSoftwareAssetMgmt.md).

Role required: admin

## About this task

To use the SaaS License Management application, you must request the Software Asset Management — SaaS License Management plugin \(sn\_sam\_saas\_int\) from the ServiceNow Store.

## Procedure

1.  From a web browser, go to the [ServiceNow Store](https://store.servicenow.com/).

2.  Log in using your HI credentials.

3.  In the search bar, enter `Software Asset Management - SaaS License Management` and then select **Search**.

4.  Select the result called Software Asset Management - SaaS License Management.

5.  On the Software Asset Management - SaaS License Management page, select **Request Install**.

6.  In the ServiceNow Request for App Installation - Software Asset Management - SaaS License Management dialog box, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Instance Name|Name of the instance on which you want to install the plugin. After you enter the instance name, select **Validate Instance** to verify that the instance exists.|
    |Reason for request|Reason for requesting the plugin.|

7.  Select **Request**.

8.  Select **Close**.


## Result

If your request is approved, you receive an email with detailed instructions on how to install the plugin.

## What to do next

Install the plugin according to the instructions from the email.

-   **[Installed with SaaS License Management](../reference/installed-with-saas.md)**  
User roles and tables are installed with SaaS License Management. Demo data is available for the Software Asset Management - SaaS License Management \(sn\_sam\_saas\_int\) plugin.
-   **[SaaS License Management setup for large companies](../concept/saas-setup-large-companies.md)**  
Set up SaaS License Management for large companies to confirm that you can view all SaaS usage data in your ServiceNow instance.

**Parent Topic:**[SaaS License Management](../concept/sam-subscription-management.md)

**Related topics**  


[SaaS Overview dashboard](../concept/saas-overview-dashboard.md)

[Playbook for SaaS integrations](../concept/playbook-saas-integrations.md)

[Integrate with SaaS applications](../concept/create-integration-profile.md)

[Integrate with SSO providers](../concept/saas-sso-integration.md)

[Create a child alias to set up multiple integration profiles](create-child-alias-saas.md)

[Viewing your SaaS and SSO subscriptions](../concept/usage-summary-saas.md)

[SaaS License Connections](../concept/saas-license-connections.md)

[Review a software reclamation rule](add-reclamation-rule-sub.md)

[Reclaiming user subscriptions](../concept/reclaiming-user-subscriptions-saas.md)

[Disconnect SSO apps](disconnect-azure-ad-apps.md)

[Delete an integration profile](../concept/delete-saas-integration.md)

[Subscription identifiers for SaaS and SSO applications](../concept/subscription-identifiers.md#)

