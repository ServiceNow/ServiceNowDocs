---
title: Requirements for installing Zero Copy Connector for ERP
description: Before you install Zero Copy Connector for ERP \(Enterprise Resource Planning\), you must complete several configurations, on both the ERP system and on the ServiceNow AI Platform.
locale: en-US
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, install, require, prerequisite, mid-server, midserver, rfc]
breadcrumb: [Configure, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Requirements for installing Zero Copy Connector for ERP

Before you install Zero Copy Connector for ERP \(Enterprise Resource Planning\), you must complete several configurations, on both the ERP system and on the ServiceNow AI Platform.

## Licensing

You must have a license and get entitlement to Zero Copy Connector for ERP for installation. For more information, see [Licensing](https://www.servicenow.com/docs/access?context=licensing&version=australia&pubname=australia-application-development&ft:locale=en-US).

## ServiceNow AI Platform plugins

The following plugins and servers are required for installing Zero Copy Connector for ERP:

-   Integration Hub plugin \(for more information, see [Request Integration Hub](../../../administer/flow-designer/concept/request-ih-overview.md)\)
-   Financial Services Remote Tables plugin \(for more information, see [Activate the remote tables plugin](https://www.servicenow.com/docs/access?context=activate-remote-tables-plugin&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)\)

## MID Server requirements

**Note:** If you are going to use a cloud solution, such as S/4HANA Cloud or SuccessFactors, MID Server is not required.

Communicating with the system of record through a MID Server requires a valid connection and credential alias.

**Note:** The credentials you specify for the Zero Copy Connector for ERP connection must match the service user credentials in the system of record.

Zero Copy Connector for ERP and ERP Semantic Mining currently support ECC \(minimum SAP Netweaver 7.31\) and SAP S/4HANA systems.

Navigate to **All** &gt; **MID Server** &gt; **Servers**, select a MID Server, and add the following:

-   In the **Supported applications** tab, edit the list to include Zero Copy Connector for ERP.
-   In the **Capabilities** tab, in addition to **ALL**, edit the list to include Zero Copy Connector for ERP.

    ![MID server record related lists with capabilities tab displayed showing Zero Copy Connector for ERP.](../image/erpc-mid-server-capabilities.png)


For more information, see [MID Server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

Assign the mid\_user user the sn\_erp\_integration.erp\_mid\_server role. The role enables the [MID Server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US) to use the ImportSet API to send data to the ServiceNow instance.

1.  Navigate to **All** &gt; **User Administration** &gt; **Users**
2.  Find and select the **mid\_user**.
3.  Select the **Roles** tab.
4.  Select **Edit**.
5.  Find and assign the **sn\_erp\_integration.erp\_mid\_server** role.

## Required SAP authorizations in development system

For the credentials, use an SAP service type user account in your system of record that requires the following SAP authorization objects:

-   S\_RFC with Activity = 16 \(Execute\) for the following Function Modules:
    -   RFCPING
    -   BAPI\_MONITOR\_GETLIST
    -   RFC\_METADATA\_GET
    -   RFC\_GET\_FUNCTION\_INTERFACE
    -   RFC\_READ\_TABLE
    -   DDIF\_FIELDINFO\_GET
-   S\_TABU\_NAM with Activity 03 \(Display\) for the following tables:
    -   DD01L
    -   DD02L
    -   DD02T
    -   DD03L
    -   DD04L
    -   DD04T
    -   DD12L
    -   DD17S
    -   DD40L
-   S\_DEVELOP with Activity 03 \(Display\)

## Required SAP authorizations in production and test system

For the credentials, use an SAP service type user account in your system of record that requires the following SAP authorization objects:

-   S\_RFC with Activity = 16 \(Execute\) for the following Function Modules:
    -   RFCPING
    -   BAPI\_TRANSACTION\_COMMIT
    -   BAPI\_TRANSACTION\_ROLLBACK
    -   RFC\_METADATA\_GET
    -   RFC\_GET\_FUNCTION\_INTERFACE
    -   RFC\_READ\_TABLE
-   S\_TABU\_NAM with Activity 03 \(Display\) for the tables you have used in models.

## SAP proprietary files

Contact the admin of your SAP ECC RFC account to obtain the following SAP proprietary JARs and other required files.

-   Create a record called "SAP Jco Dll" and attach `sapjco3.dll`. Use this file if your MID Server is installed on a Windows server.
-   Create a record called "SAP Jco so" and attach `libsapjco3.so`. Use this file if your MID Server is installed on a Linux server.
-   Create a record called "SAP Eco Jar" and attach `sapjco3.jar`. Use this file for both Windows and Linux.

**Note:** Create the records at **All** &gt; **MID Server** &gt; **JAR Files**. For more information about creating JAR files and adding attachments, see [Synchronize a JAR file to MID Servers](https://www.servicenow.com/docs/access?context=t_SynchronizeAJARFiletoMIDServers&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

The MID Server restarts multiple times during this process.

For details about these files, see [SAP ECC RFC Spoke](../../../administer/integrationhub-store-spokes/concept/sap-ecc-rfc-spoke.md).

## SAP configuration

You must configure the JCO connector before you install Zero Copy Connector for ERP. For more information, see [Installing the SAP Java Connection \(JCo\)](https://help.sap.com/docs/SAP_ANALYTICS_CLOUD/00f68c2e08b941f081002fd3691d86a7/ffe3b941e82641bc97b76ce522423d83.html) on the SAP Help Portal.

You must add the DuckDB JDBC jar as a MID Server jar. For more information and to download, see [DuckDB JDBC Driver 1.1.1](https://mvnrepository.com/artifact/org.duckdb/duckdb_jdbc/1.1.1) on the Maven website.

Additionally, you need the following on your ERP system:

-   SAP ECC \(minimum SAP Netweaver 7.31\)
-   SAP S/4HANA \(all versions supported\)
-   SAP Java Connector

**Parent Topic:**[Configuring Zero Copy Connector for ERP](../concept/erp-integration-configuration-overview.md)

