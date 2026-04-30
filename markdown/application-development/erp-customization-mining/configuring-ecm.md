---
title: Configuring ERP Semantic Mining
description: Set up ERP Semantic Mining \(ERP-CM\) to enable the app to scan the system of record for candidates to replatform. Administrators can also quickly check the health of the ERP \(Enterprise Resource Planning\) connection and investigate any issues, and view knowledge articles related to errors.
locale: en-US
release: yokohama
product: ERP Customization Mining
classification: erp-customization-mining
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [ERP Semantic Mining \(ERP-CM\), Building low-code applications, Developing your application, Building applications]
---

# Configuring ERP Semantic Mining

Set up ERP Semantic Mining \(ERP-CM\) to enable the app to scan the system of record for candidates to replatform. Administrators can also quickly check the health of the ERP \(Enterprise Resource Planning\) connection and investigate any issues, and view knowledge articles related to errors.

You must install Zero Copy Connector for ERP and configure connections and ERP data models before you can install ERP Semantic Mining.

## Server requirements

For the credentials, use an SAP service type user account in your system of record that requires the following S\_RFC SAP authorization objects:

-   S\_RFC with Activity = 16 \(Execute\) for the following Function Modules:
    -   SAPWL\_WORKLOAD\_GET\_STATISTIC
    -   SWNC\_COLLECTOR\_GET\_AGGREGATES
    -   SWNC\_COLLECTOR\_GET\_DIRECTORY
    -   SQLM\_API\_GET\_NEXT\_DATA\_PACKAGE
-   S\_TABU\_NAM with Activity 03 \(Display\) for the following table: TRNSPACET

There are additional authorizations needed for Zero Copy Connector for ERP. For more information, see [Configuring Zero Copy Connector for ERP](../../erp-integration/concept/erp-integration-configuration-overview.md).

**Note:** The credentials you specify for the Zero Copy Connector for ERP connection must match the service user credentials in the system of record.

## Types and number of available connections

Zero Copy Connector for ERP and ERP-CM currently support ECC \(minimum SAP Netweaver 7.31\) and S/4HANA SAP systems.

**Note:** Each installation of ERP-CM supports adding up to 10 systems. However, ERP-CM can connect to only one live ERP system at a time.

You should install Zero Copy Connector for ERP and add credentials there before you install and configure ERP-CM. For more information, see [Configure the Zero Copy Connector for ERP credentials and connection](../../erp-integration/task/set-up-erp-integration-connection.md).

The number of ERP connections you can have per ServiceNow instance depends on your license. If you have the ERP-CM license, you get one connection per instance.

For details on Connections and Credentials, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

## Plugins for ERP Semantic Mining

You must have the following plugins installed:

<table id="table_zj1_ykl_bwb"><thead><tr><th>

Plugin

</th><th>

Full name

</th><th>

Dependencies

</th></tr></thead><tbody><tr><td>

Zero Copy Connector for ERP

</td><td>

com.snc.sn\_erp\_integration

</td><td>

com.glide.script.vtable

</td></tr><tr><td>

ERP Semantic Mining

</td><td>

com.snc.uib.sn\_erp\_mining

</td><td>

-   com.snc.sn\_erp\_integration
-   com.glide.platform\_ml

</td></tr></tbody>
</table>## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

-   **[Configure SAP for ERP-CM](../task/ecm-configure-sap-system.md)**  
Enable SQLM \(SQL Monitor\) on the productive system and confirm that ST03 \(Workload Monitor\) is collected for daily workloads before you can install ERP Semantic Mining \(ERP-CM\).
-   **[Install ERP Semantic Mining](../task/install-erp-customization-mining.md)**  
Install the ERP Semantic Mining \(ERP-CM\) application \(sn\_erp\_mining\) if you have the admin role from the ServiceNow Store.
-   **[Run Guided Setup for ERP Semantic Mining](../task/set-up-erp-customization-mining-guided.md)**  
Run the Guided Setup to configure ERP Semantic Mining \(ERP-CM\).
-   **[Configure a new ERP Semantic Mining connection](../task/set-up-erp-customization-mining.md)**  
Specify the Connections and Credentials alias for ERP Semantic Mining \(ERP-CM\) to connect to the ERP \(Enterprise Resource Planning\) system.
-   **[Update an ERP-CM connection](../task/update-ecm-connection.md)**  
Update the Connections and Credentials alias for ERP Semantic Mining \(ERP-CM\) to change the connection to the ERP \(Enterprise Resource Planning\) system. For example, you may want to change from a non-production system to a production system.
-   **[Check and troubleshoot the data refresh status for ERP Semantic Mining](../task/erpcm-check-data-connection.md)**  
Check the data refresh status to find out when ERP Semantic Mining \(ERP-CM\) most recently loaded ERP \(Enterprise Resource Planning\) data from the system of record.
-   **[Create a snapshot to share and save data in ERP Semantic Mining](../task/create-a-snapshot-to-share-and-save-data.md)**  
Export and import ERP Semantic Mining base data to save and share.
-   **[Getting notifications for ERP Semantic Mining connection updates](erpcm-notifications.md)**  
ERP Semantic Mining \(ERP-CM\) can email you about the success and failures of ERP \(Enterprise Resource Planning\) system connections.
-   **[Configure notifications for ERP-CM tasks](../task/erpcm-enable-notifications.md)**  
Enable notifications to find out when ERP Semantic Mining \(ERP-CM\) succeeds or fails in a mining job for the ERP \(Enterprise Resource Planning\) system of record.
-   **[ERP Semantic Mining roles](erp-personas-roles.md)**  
Administrators assign roles to give team members permission to configure or use ERP Semantic Mining \(ERP-CM\).
-   **[ERP-CM and security](erpcm-and-security.md)**  
In addition to role-based security and access control, ERP Semantic Mining \(ERP-CM\) protects personally identifiable ERP \(Enterprise Resource Planning\) data in other ways.

**Parent Topic:**[ERP Semantic Mining \(ERP-CM\)](erp-customization-mining-overview.md)

