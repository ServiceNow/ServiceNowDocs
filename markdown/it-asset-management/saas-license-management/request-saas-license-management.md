---
title: Request SaaS License Management
description: Request the Software Asset Management - SaaS License Management plugin \(sn\_sam\_saas\_int\) so that you can create and manage integrations with your SaaS and Single Sign-on \(SSO\) applications. You can use these integrations to track license usage and to reclaim unused licenses.
locale: en-US
release: yokohama
product: SaaS License Management
classification: saas-license-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
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

Navigate to **All** &gt; **Admin Center** &gt; **Application Manager**. On the Application Manager page, search for and select **Software Asset Management - SaaS License Management**.

After the application is installed and ready for use, you can choose the required SaaS applications that you need by selecting **Install optional features** on the [Application Manager](https://www.servicenow.com/docs/access?context=application-manager&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) page.

You can see the primary features and the list of optional features that you can select in the Review Installation Details dialog box. If you haven't selected any optional features, you would get the base system features of this application.

![SaaS License Management installation details review.](../image/review-saas-install-details.png)

After you select the optional features, select **Install**. You can initiate or schedule the installation process by selecting **Install now** or **Install later**. View the installation progress and you’ll get a success message after the installation is complete.

-   **[Installed with SaaS License Management](../reference/installed-with-saas.md)**  
User roles and tables are installed with SaaS License Management. Demo data is available for the Software Asset Management - SaaS License Management \(sn\_sam\_saas\_int\) plugin.

**Parent Topic:**[SaaS License Management](../concept/sam-subscription-management.md)

**Related topics**  


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

[Disconnect SSO apps](disconnect-azure-ad-apps.md)

[Delete an integration profile](../concept/delete-saas-integration.md)

[Subscription identifiers for SaaS and SSO applications](../concept/subscription-identifiers.md#)

