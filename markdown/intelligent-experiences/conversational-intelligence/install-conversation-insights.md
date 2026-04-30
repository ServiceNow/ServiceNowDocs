---
title: Install Conversation Insights
description: If you have the admin role, you can install the Conversation Insights application \(sn\_aci\).If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:The application includes demo data and installs related ServiceNow Store applications and plugins, if they aren’t already installed.
locale: en-US
release: zurich
product: Conversational Intelligence
classification: conversational-intelligence
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Conversation Insights, Enable AI experiences]
---

# Install Conversation Insights

If you have the admin role, you can install the Conversation Insights application \(sn\_aci\).The application includes demo data and installs related ServiceNow® Store applications and plugins, if they aren’t already installed.

## Before you begin

-   Confirm that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Review the application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.
-   Inferred CSAT is calculated by an internal service that communicates with the instance using mutual Transport Layer Security \(mTLS\). To enable this, the instance must be configured to support Application Delivery Controller-to-Application \(ADC-to-APP\) mTLS. This setup ensures strong authentication and encrypted data exchange between internal services and the instance, requiring both client and server to present and validate certificates during the TLS handshake. For more information on mTLS configuration, refer to steps 1 and 2 in the Prerequisites section of [KB0993615](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0993615).

Role required: admin

## About this task

The following items are installed with Conversation Insights:

-   Plugins
-   Store applications
-   Roles
-   Scheduled jobs
-   Conversation Insights \[sn\_aci\_insights\] table

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Conversation Insights application \(sn\_aci\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you can’t find the application, you might have to request it from the ServiceNow Store.

    A list of the versions available to you’re displayed.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are the sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

6.  Select **Install**.


