---
title: Create Microsoft Azure credentials for billing download
description: Define the scheduled job that regularly uses a MID Server to download billing data from the provider. Cloud Provisioning and Governance saves the data in a cost table and uses the information to generate reports.
locale: en-US
release: yokohama
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Day 1 setup guide for Microsoft Azure Cloud on Cloud Provisioning and Governance, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Create Microsoft Azure credentials for billing download

Define the scheduled job that regularly uses a MID Server to download billing data from the provider. Cloud Provisioning and Governance saves the data in a cost table and uses the information to generate reports.

## Before you begin

**Important:**

Starting with the Vancouver release, the Billing dashboard is no longer available if you have downloaded and activated the ServiceNow Store Cloud Cost Management application. The following changes occur:

-   You’re redirected to the Cloud Cost Management home page by default.
-   The View Dashboard widget in the Cloud User portal is replaced by the View Resources widget.
-   The Current Month Spend widget and the Budget widget on the Cloud User portal don’t show any data if Cloud Cost Management is activated on the instance.

If you have activated the Cloud Cost Management application, you can only navigate to the Billing Dashboard when you’re using Cloud Provisioning and Governance on a domain-separated instance.

You must have an API Access Key credential for a Microsoft Enterprise Agreement EA for all Azure accounts that you want billing information for.

Role required: sn\_cmp.cloud\_governor

## About this task

During the billing download process, all the resources are pulled into the system. Azure databases are placed in the Database \[cmdb\_ci\_database\] table.

## Procedure

1.  Create Client Secret by navigating to the Overview page of the previously deployed Service Principal application.

    1.  On the left pane, select **Certificates &amp; secrets**.

    2.  In the Client secrets section, select **New client secret**.

    3.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Description|Description of the Client secret. For example, `Client secret for MyServicePrincipal`.|
        |Expires|Expiration period that suits your requirements. For example, `6 months`, `12 months`, `24 months`, or `Never`.|

    4.  Select **Add**.

    After adding the Client Secret, a value gets generated and displayed.

    **Note:** Copy this value immediately as it wouldn’t be shown again, which is your Client Secret \(access key\).

2.  Copy the Application \(client\) ID and Directory \(tenant\) ID for later use.

3.  Assign a role to the Service Principal.

    1.  On the left pane, select **Azure Active Directory**.

    2.  Select **Roles and administrators**.

    3.  Select **All roles** and find the role that you want to assign.

    4.  Select the role and then select **Add assignment**.

    5.  Search for and select your Service principal by its name and then select **Add**.

4.  Obtain a Subscription ID by selecting **Subscriptions**.

    1.  Select the subscription that you want to use.

    2.  Copy the Subscription ID from the Subscription Overview page.


