---
title: Request SaaS License Management
description: Request the Software Asset Management - SaaS License Management plugin \(sn\_sam\_saas\_int\) so that you can create and manage integrations with your SaaS and Single Sign-on \(SSO\) applications. You can use these integrations to track license usage and to reclaim unused licenses.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/saas-license-management/request-saas-license-management.html
release: australia
product: SaaS License Management
classification: saas-license-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [SaaS License Management, Software Asset Management, IT Asset Management]
---

# Request SaaS License Management

Request the Software Asset Management - SaaS License Management plugin \(sn\_sam\_saas\_int\) so that you can create and manage integrations with your SaaS and Single Sign-on \(SSO\) applications. You can use these integrations to track license usage and to reclaim unused licenses.

## Before you begin

Activate the ServiceNow Software Asset Management Professional plugin \(com.snc.samp\) on your ServiceNow instance. For more information on how to request and activate the Software Asset Management Professional plugin \(com.snc.samp\), see [Request Software Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/t_RequSoftwareAssetMgmt.md).

Role required: admin

## About this task

To use the SaaS License Management application, you must request the Software Asset Management — SaaS License Management plugin \(sn\_sam\_saas\_int\) from the ServiceNow Store.

**Note:** When upgrading to the Software Asset Management – SaaS License Management plugin \(sn\_sam\_saas\_int\) version 16.0.6 or later in the Zurich release, verify that the Software Asset Workspace store app \(sn\_sam\_workspace\) is updated to version 9.0.4.

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

After the application is installed and ready for use, you can choose the required SaaS applications that you need by selecting **Install optional features** on the [Application Manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/application-manager.md) page.

You can see the primary features and the list of optional features that you can select in the Review Installation Details dialog box. If you haven't selected any optional features, you would get the base system features of this application.

\[Omitted image "review-saas-install-details.png"\] Alt text: SaaS License Management installation details review.

After you select the optional features, select **Install**. You can initiate or schedule the installation process by selecting **Install now** or **Install later**. View the installation progress and you’ll get a success message after the installation is complete.

-   **[Installed with SaaS License Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/saas-license-management/installed-with-saas.md)**  
User roles and tables are installed with SaaS License Management. Demo data is available for the Software Asset Management - SaaS License Management \(sn\_sam\_saas\_int\) plugin.

**Parent Topic:**[SaaS License Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/saas-license-management/sam-subscription-management.md)

**Related topics**  


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

[Disconnect SSO apps]()

[Delete an integration profile]()

[Subscription identifiers for SaaS and SSO applications]()

[Subscription exclusions for SaaS and SSO applications]()

