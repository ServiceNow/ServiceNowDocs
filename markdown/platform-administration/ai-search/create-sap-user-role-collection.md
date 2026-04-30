---
title: Create a SAP user and role collection
description: Create a user and a role collection in the SAP Business Technology Platform \(BTP\) cockpit. The SAP DMS external content connector needs this user account to access your SAP DMS content.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-11-06"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [SAP DMS external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Create a SAP user and role collection

Create a user and a role collection in the SAP Business Technology Platform \(BTP\) cockpit. The SAP DMS external content connector needs this user account to access your SAP DMS content.

## Before you begin

You must be a global account administrator on the SAP BTP.

A SAP global account administrator must have created a subaccount in your SAP BTP global account, with these entitlements:

-   Document Management Service, Application Option
-   Document Management Service, Integration Option
-   Document Management Service, Repository Option
-   Cloud Foundry Environment
-   Authorization and Trust Management Service

If you don't already have a subaccount with these entitlements in your SAP BTP global account, perform the [Create a subaccount in the SAP Business Technology Platform \(BTP\)](create-subaccount-sap-btp.md) preliminary task before performing this task.

Role required: none

## About this task

The SAP DMS external content connector requires a user account with specific roles. Create a role collection with these roles and assign it to a user account to allow the connector to access your SAP DMS folders and files.

## Procedure

1.  Create a new user account for use with the SAP DMS external content connector.

    1.  Log in to the SAP Business Technology Platform \(BTP\) at [https://cockpit.btp.cloud.sap/](https://cockpit.btp.cloud.sap/) using your global account credentials.

    2.  In the Subaccounts tab, select your subaccount with the aforementioned entitlements.

    3.  Navigate to **Security** &gt; **Users**.

    4.  Select **Create**.

    5.  On the Create User form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |User Name|Enter a name for this user account.|
        |Identity Provider|Select **Default identity provider**.|
        |E-Mail|Enter the email address for this user account.|

    6.  Select **Create**.

    The SAP BTP creates your new user account.

2.  Create a new role collection.

    1.  From your subaccount, navigate to **Security** &gt; **Roles Collections**.

    2.  Select **Create**.

    3.  On the Create Role Collection form, enter a name for your role collection.

    4.  Select **Create**.

    The SAP BTP creates your new role collection.

3.  Assign the required roles to your new role collection.

    1.  In your subaccount, search for and then select the name of your new role collection.

    2.  On the form for your new role collection, select **Edit**.

    3.  Select the name of your new role collection.

    4.  Select each of the following roles.

        -   SDMWeb\_Admin
        -   SDMWeb\_Migration
        -   SDMWeb\_User
        -   SDM\_MobileAdmin
        -   SDM\_Admin
    5.  Select **Add**.

4.  Assign your new role collection to your new user account.

    1.  From the Users list, search for and select the name of your new user account.

    2.  Select **Assign Role Collection**.

    3.  Select the name of your new role collection.

    4.  Select **Assign Role Collection**.


**Parent Topic:**[SAP DMS external content connector](../concept/sap-dms-external-content-connector.md)

