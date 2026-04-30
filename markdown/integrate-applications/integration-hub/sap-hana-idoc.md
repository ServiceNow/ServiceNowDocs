---
title: SAP S4 HANA IDoc Spoke
description: The SAP S4 HANA IDoc spoke is built by Bristlecone, Inc. Manage finance, items, and procurement in SAP S4 HANA IDoc account from your ServiceNow instance.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-06"
reading_time_minutes: 4
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# SAP S4 HANA IDoc Spoke

The SAP S4 HANA IDoc spoke is built by Bristlecone, Inc. Manage finance, items, and procurement in SAP S4 HANA IDoc account from your ServiceNow instance.

## Request apps on Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html). Starting on March 1st 2022, all SAP spokes will be available only on the Store.

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

SAP S4 HANA IDoc spoke v1.2.0 is the latest version.

## Supported versions

This spoke was built for SAP S4 HANA IDoc 2023.

## Spoke requirements

-   Contact the admin of your SAP S4 HANA IDoc account and obtain these SAP proprietary JAR files and other required files:

    -   `sapidoc3.jar` and `sapjco3.jar`.
    -   `libsapjco3.so`: If your MID Server is installed on a Linux machine, obtain this file.
    -   `sapjco3.dll`: If your MID Server is installed on a Windows machine, obtain this file.
    A JAR file, `sapConnector-1.0.1.jar` is available along with the spoke to provide a custom interface between SAP S4 HANA IDoc account and ServiceNow instance. The JAR file is installed as part of the spoke in your ServiceNow instance.

-   Copy and record the client value of the target host where the SAP S4 HANA IDoc server is installed.
-   To retrieve information for authorization purposes, use the Execute RFC spoke action in the [SAP S4 HANA RFC Spoke](sap-s4hanarfc-spoke.md).
-   If you are using this spoke along with the SAP ECC IDoc, SAP ECC RFC, SAP S4 HANA RFC spokes, during spoke upgrades, ensure that you upgrade all the spokes to their latest versions.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   Complex Object \(com.glide.cobject\)
-   Flow Designer Action Step - Script on MID \(com.glide.hub.action\_step.script\_mid\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The SAP S/4 HANA IDoc spoke provides actions to automate SAP S4 HANA IDoc tasks when events occurs in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Customer Account|Create Customer Account|Creates a customer account in SAP S/4HANA.|
|Update Customer Account|Updates details of the specified customer account in SAP S/4HANA.|
|Finance|Create Fixed Assets|Creates a fixed asset in SAP S4 HANA IDoc.|
|Create GL Account|Creates a GL account in SAP S4 HANA IDoc.|
|Create Invoice|Creates an invoice document in SAP S4 HANA IDoc.|
|Post Journal Entry|Posts a journal entry to a GL account in SAP S4 HANA IDoc.|
|Update Fixed Assets|Updates details of a fixed asset in SAP S4 HANA IDoc.|
|Update GL Account|Updates details of the specified GL account in SAP S4 HANA IDoc.|
|Items|Create Material|Creates a material \(item\) in SAP S4 HANA IDoc.|
|Update Material|Updates details of the specified material \(item\) in SAP S4 HANA IDoc.|
|Procurement|Create Goods Receipt|Creates a goods receipt in SAP S4 HANA IDoc.|
|Create Purchase Order|Creates a purchase order in SAP S4 HANA IDoc.|
|Create Vendor|Creates a vendor in SAP S4 HANA IDoc.|
|Update Purchase Order|Updates details of the specified purchase order in SAP S4 HANA IDoc.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

For information about setting up the spoke, see [Set up the SAP S4 HANA IDoc spoke](../task/setup-sap-s4-hana-idoc.md).

## MID Server requirements

These actions use Remote Function Call \(RFC\) protocol \(SAP Proprietary protocol – SAP Standard Interface\) leveraging Application Link Enabling \(ALE\) framework, which can run on an instance or MID Server. Use the connection record associated with the SAP S4 HANA IDoc alias to configure where actions run as well as set MID Server selection attributes. For more information about running actions on the MID Server, see [Integration steps](../../integrationhub/concept/integration-steps.md)

To set up the MID Server for this spoke, see [Set up MID Server for a spoke](../task/config-adv-mid-settings-for-oauth-on-mid.md).

