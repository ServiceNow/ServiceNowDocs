---
title: Create a subaccount in the SAP Business Technology Platform \(BTP\)
description: Create a subaccount with required entitlements in your SAP global account using the SAP BT cockpit. You need this subaccount in order to configure SAP access for the SAP DMS external content connector.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-11-07"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [SAP DMS external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Create a subaccount in the SAP Business Technology Platform \(BTP\)

Create a subaccount with required entitlements in your SAP global account using the SAP BT cockpit. You need this subaccount in order to configure SAP access for the SAP DMS external content connector.

## Before you begin

You must be a global account administrator on the SAP Business Technology Platform \(BTP\). Your global account must be authorized to access the SAP Document Management Service.

Role required: none

## About this task

This task is optional. To configure the SAP DMS external content connector, you need a subaccount in your SAP BTP global account, with these entitlements:

-   Document Management Service, Application Option
-   Document Management Service, Integration Option
-   Document Management Service, Repository Option
-   Cloud Foundry Environment
-   Authorization and Trust Management Service

If your SAP BTP global account already includes a subaccount with these entitlements, you can skip this task and go on to configure your SAP BTP global account to allow access by the connector. For details on this procedure, see [Configure SAP DMS for external content indexing](configure-sap-dms-external-content-indexing.md).

## Procedure

1.  Create a new subaccount in your global account.

    1.  Log in to the SAP Business Technology Platform \(BTP\) at [https://cockpit.btp.cloud.sap/](https://cockpit.btp.cloud.sap/) using your global account credentials.

    2.  Select **Create** &gt; **Subaccount**.

    3.  Enter a display name for your new subaccount.

        As an example, you might enter `SAP DMS external content connector subaccount`.

    4.  Enter a description for your new subaccount.

    5.  Enter a subdomain for your new subaccount.

    6.  Select the desired region for your new subaccount.

    7.  Select a parent for your new subaccount.

        The parent can be your global account or a directory.

    8.  Select **Create**.

    SAP BTP creates your new subaccount.

2.  Create a Cloud Foundry organization in your new subaccount.

    1.  Select your new subaccount and navigate to its Overview page.

    2.  Select **Enable Cloud Foundry**.

    3.  On the Enable Cloud Foundry form, in the Plan field, select the plan for the Cloud Foundry runtime.

    4.  In the Org Name field, enter a name for your new Cloud Foundry organization.

        As an example, you might enter `sap-dms-integrate`.

    5.  Select **Create**.

    SAP BTP creates the new Cloud Foundry organization for your new subaccount.

3.  Create a new Cloud Foundry space named **DMS** in the Cloud Foundry organization for your new subaccount.

    1.  Navigate to the **Cloud Foundry** &gt; **Spaces** page for your new subaccount.

    2.  Select **Create Space**.

    3.  On the Create Space form, enter `DMS` as the name for your new space.

    4.  Select the options for the **Space Developer** and **Space Manager** roles.

    5.  Select **Save**.

    SAP BTP creates the new Cloud Foundry space in the Cloud Foundry organization for your new subaccount.

4.  Add a service plan for the SAP Document Management Service to your new subaccount.

    1.  Navigate to your global account.

    2.  In the menu, navigate to **Entitlements** &gt; **Entity Assignments**.

    3.  In the Subaccounts/Directories field, search for and select your new subaccount.

    4.  In the My Subaccount pane, select **Edit**.

    5.  Select **Add Service Plans**.

    6.  In the Services section, search for and select the **Document Management Service, Integration Option** entry.

    7.  In the Service Details pane, in the Available Plans field, select the **standard** plan.

    8.  Select **Add 1 Service Plan**.

    9.  Select **Save**.

    SAP BTP adds the service plan to your new subaccount.


## What to do next

Now that you've created a subaccount with the required entitlements, go on to configure service instances and service keys in your SAP BTP global account. For details on this procedure, see [Configure SAP DMS for external content indexing](configure-sap-dms-external-content-indexing.md).

**Parent Topic:**[SAP DMS external content connector](../concept/sap-dms-external-content-connector.md)

