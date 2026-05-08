---
title: Install Billing Account
description: You can install the Billing Account application \(com.snc.billing\_account\) if you have the admin role. The application includes demo data and installs related ServiceNow Store applications and plugins if they are not already installed.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-05-08"
reading_time_minutes: 1
breadcrumb: [Configuring billing accounts, Customer data, Set up your environment, Configure, Customer Service Management]
---

# Install Billing Account

You can install the Billing Account application \(com.snc.billing\_account\) if you have the admin role. The application includes demo data and installs related ServiceNow® Store applications and plugins if they are not already installed.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Review the [Order Management](https://store.servicenow.com/store/app/813bab2a1b246a50a85b16db234bcb8e) application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.

Role required: admin

## About this task

The billing account application has a modular plugin structure:

-   Base plugin \(com.snc.billing\_account\): Independent core functionality for billing account management
-   CSM integration: Install com.sn\_customerservice and com.snc.cs\_base to enable billing account integration with core CSM capabilities and the Related Party Framework
-   CSM Workspace support: Install com.snc.uib.csm\_agent\_workspace to enable CSM Workspace support for billing account integration
-   Household functionality: Install com.snc.household for household-related billing scenarios
-   Install Base and Sold Product functionality: Install sn\_install\_base for product inventory integration

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Customer** &gt; **Billing Accounts**.

2.  Select **New** from the billing accounts record.

3.  On the form, fill in the fields.

    |Field|Definition|
    |-----|----------|
    |Name|Name of the billing account.|
    |Number|Internal unique number identifying the billing account.|
    |Billing account type|Organization or user type associated with this billing account.|
    |Parent billing account|References the parent billing account.|
    |Status|Indicates the current state of the billing account.|
    |Account|Customer account to which this billing account belongs.|
    |Contact|Customer contact to which this billing account belongs.|
    |Consumer|Consumer to which this billing account belongs.|
    |Start date|Date when the billing account becomes active.|
    |End date|Date when the billing account is closed or terminated.|
    |Currency|Currency used for transactions in this billing account.|
    |Active|Status of the configuration. By using this functionality, you can enable or disable this configuration.|
    |Description|Description of the billing account.|

4.  Select **Submit** to create a new billing account record.


