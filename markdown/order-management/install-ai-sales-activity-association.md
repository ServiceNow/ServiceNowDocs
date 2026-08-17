---
title: Install AI sales activity association
description: You can install the AI sales activity association application \(com.sn\_act\_assoc\_agent\) if you have the admin role. The application installs related ServiceNow Store applications and plugins if they are not already installed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/install-ai-sales-activity-association.html
release: australia
topic_type: task
last_updated: "2026-06-30"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Activity Management, Sales automation apps, Configure, Sales Customer Relationship Management]
---

# Install AI sales activity association

You can install the AI sales activity association application \(com.sn\_act\_assoc\_agent\) if you have the admin role. The application installs related ServiceNow® Store applications and plugins if they are not already installed.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Review the [AI sales activity association](https://store.servicenow.com/sn_appstore_store.do#!/store/application/e70338356063b690f8779654ad7ebaeb/) application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.

Role required: admin

## About this task

The following store applications and plugins are installed as a dependency with AI sales activity association:

-   Opportunity Management \[com.sn\_l2c\_oppty\_mgmt\]​
-   ServiceNow Otto for Platform \[com.sn.now.platform\]
-   User Mailbox Integration \[com.glide.email.user\_mailbox.integration\]
-   CRM Outlook Add-in \[com.sn\_crm\_outlook\_addin\]
-   Notifications Email Agents \[com.sn\_notif\_agents\]

For associating emails to Lead records, install Lead Management separately.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the AI sales activity association application \(com.sn\_act\_assoc\_agent\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    A list of the versions available to you is displayed.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are the sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

6.  Select **Install**.


## What to do next

-   Index the Lead \[sn\_lead\_mgmt\_core\_lead\] and Opportunity \[sn\_opty\_mgmt\_core\_opportunity\] tables, so that the records from these tables are searchable by the agentic AI workflow. For more information, see [Perform a full table index or reindex for a single AI Search indexed source](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/index-single-source-ais.md).
-   [Configure email promotion rules for Activity Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/promote-crm-outlook-emails.md)

**Related topics**  


[Indexing content from AI Search indexed sources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/indexing-content-ais.md)

[Install Lead Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/install-lead-management.md)

