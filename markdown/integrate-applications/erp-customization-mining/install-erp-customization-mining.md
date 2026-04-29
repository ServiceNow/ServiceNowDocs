---
title: Install ERP Semantic Mining
description: Install the ERP Semantic Mining application \(sn\_erp\_mining\) if you have the admin role from the ServiceNow Store.
locale: en-US
release: australia
product: ERP Customization Mining
classification: erp-customization-mining
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, ERP Semantic Mining overview, Zero Copy Connector for ERP overview, Workflow Data Fabric]
---

# Install ERP Semantic Mining

Install the ERP Semantic Mining application \(sn\_erp\_mining\) if you have the admin role from the ServiceNow Store.

## Before you begin

**Important:** Starting with the Zurich release, ERP Semantic Mining is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

You must:

-   Have a license and get entitlement to ERP Semantic Mining before you can install the application.
-   Install Zero Copy Connector for ERP. Use the application to configure connections to the system of record, as well as ERP \(Enterprise Resource Planning\) data models.
-   Configure the JCO connector before you install ERP Semantic Mining. See the SAP documentation for more information.

The following plugins are required:

-   Zero Copy Connector for ERP
-   Predictive Intelligence

Role required: admin

## About this task

## Procedure

1.  In the ServiceNow Store, confirm that you have entitlements \(or licenses\) to the product and dependent applications.

    You can access the Store by navigating to **System Applications** &gt; **All Available Applications** &gt; **Available To Obtain From Store**.

2.  Search for ERP Semantic Mining and select **Install**.

3.  Select **Load demo data** to create demo data in the app.

4.  Select **Install** to confirm the installation of ERP Semantic Mining.


## Result

The installation is complete. Select **Close** to return to the ServiceNow Store.

## What to do next

After you install ERP Semantic Mining, ERP data from the connected system of record populates the ERP extraction tables in Zero Copy Connector for ERP. For example, ERP application activity, Collector directory data, and Namespace data. You can then incorporate extracted data into ERP data models and remote tables for use as a data source when building apps on ServiceNow. For more information, see [Standard ERP models and extraction tables for Zero Copy Connector for ERP](../../erp-integration/reference/erp-canvas-standard-extraction-tables.md).

**Parent Topic:**[Configuring ERP Semantic Mining](../concept/configuring-ecm.md)

