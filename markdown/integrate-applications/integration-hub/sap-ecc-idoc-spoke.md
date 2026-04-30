---
title: SAP ECC IDoc Spoke
description: The SAP ECC IDoc spoke is built by Bristlecone, Inc. Manage finance, items, and procurement in SAP ECC IDoc account from your ServiceNow instance.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# SAP ECC IDoc Spoke

The SAP ECC IDoc spoke is built by Bristlecone, Inc. Manage finance, items, and procurement in SAP ECC IDoc account from your ServiceNow instance.

## Request apps on Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html). Starting on March 1st 2022, all SAP spokes will be available only on the Store.

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

SAP ECC IDoc spoke v1.5.1 is the latest version.

## Supported versions

This spoke was built for these SAP ECC IDoc versions, but may be compatible with later versions:

-   SAP application version: SAP ECC6 \(Spoke is developed on EHp8.\)
-   NetWeaver Version: SAP NW 7.5
-   SAP JCo:3.0.20

## Spoke requirements

-   Contact the admin of your SAP ECC IDoc account and obtain these SAP proprietary JAR files and other required files:

    -   `sapidoc3.jar` and `sapjco3.jar`.
    -   `libsapjco3.so`: If your MID Server is installed on a Linux machine, obtain this file.
    -   `sapjco3.dll`: If your MID Server is installed on a Windows machine, obtain this file.
    A JAR file, `sapConnector-1.0.1.jar` is available along with the spoke to provide a custom interface between SAP ECC IDoc account and ServiceNow instance. The JAR file is installed as part of the spoke in your ServiceNow instance.

-   Copy and record the client value of the target host where the SAP ECC IDoc server is installed.
-   If you are using this spoke along with the SAP ECC RFC spoke, during spoke upgrades, ensure that you upgrade both the spokes.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   Complex Object \(com.glide.cobject\)
-   Flow Designer Action Step - Script on MID \(com.glide.hub.action\_step.script\_mid\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The SAP ECC IDoc spoke provides actions to automate SAP ECC IDoc tasks when events occurs in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Finance|Create Fixed Assets|Creates fixed asset in your SAP ECC IDoc account.|
|Create GL Account|Creates a GL account in your SAP ECC IDoc account.|
|Create Invoice|Creates an invoice document in your SAP ECC IDoc account.|
|Post Journal Entry|Posts a journal entry in your SAP ECC IDoc account.|
|Update Fixed Assets|Updates details of the fixed assets in your SAP ECC IDoc account.|
|Update GL Account|Updates details of the specified GL account in your SAP ECC IDoc account.|
|Items|Create Material|Creates a material \(item\) in your SAP ECC IDoc account.|
|Update Material|Updates details of the specified material \(item\) in your SAP ECC IDoc account.|
|Procurement|Create Goods Receipt|Creates a goods receipt in your SAP ECC IDoc account.|
|Create Purchase Order|Creates a purchase order in your SAP ECC IDoc account.|
|Create Vendor|Creates a vendor in your SAP ECC IDoc account.|
|Update Purchase Order|Updates details of the specified purchase order in your SAP ECC IDoc account.|
|Customer|Create Customer|Creates a customer account in SAP ECC IDoc.|
|Update Customer|Update details of the required customer account in SAP ECC IDoc.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

## MID Server requirements

These actions use Remote Function Call \(RFC\) protocol \(SAP Proprietary protocol – SAP Standard Interface\) leveraging Application Link Enabling \(ALE\) framework, which can run on an instance or MID Server. Use the connection record associated with the SAP ECC IDoc alias to configure where actions run as well as set MID Server selection attributes. For more information about running actions on the MID Server, see [Integration steps](../../integrationhub/concept/integration-steps.md).

To set up the MID Server for this spoke, see [Set up MID Server for a spoke](../task/config-adv-mid-settings-for-oauth-on-mid.md).

