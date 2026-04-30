---
title: Install ERP Customization Mining
description: Install the ERP Customization Mining \(ERP-CM\) application \(sn\_erp\_mining\) if you have the admin role from the ServiceNow Store.
locale: en-US
release: xanadu
product: ERP Customization Mining
classification: erp-customization-mining
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring ERP Customization Mining, ERP Customization Mining \(ERP-CM\), Building low-code applications, Developing your application, Building applications]
---

# Install ERP Customization Mining

Install the ERP Customization Mining \(ERP-CM\) application \(sn\_erp\_mining\) if you have the admin role from the ServiceNow Store.

## Before you begin

You must:

-   Have a license and get entitlement to ERP-CM before you can install the application.

    For more information, see [Licensing](../../custom-application/reference/licensing.md).

-   Install ERP Data Hub. Use the application to configure connections to the system of record, as well as ERP \(Enterprise Resource Planning\) data models.
-   Configure the JCO connector before you install ERP-CM. See the SAP documentation for more information.

The following plugins are required:

-   ERP Data Hub
-   Predictive Intelligence

Role required: admin

## About this task

## Procedure

1.  In the ServiceNow Store, confirm that you have entitlements \(or licenses\) to the product and dependent applications.

    You can access the Store by navigating to **System Applications** &gt; **All Available Applications** &gt; **Available To Obtain From Store**.

2.  Search for ERP Customization Mining and select **Install**.

3.  Select **Load demo data** to create demo data in the app.

4.  Select **Install** to confirm the installation of ERP-CM.


## Result

The installation is complete. Select **Close** to return to the ServiceNow Store.

## What to do next

After you install ERP-CM, ERP data from the connected system of record populates the ERP extraction tables in ERP Data Hub. For example, ERP application activity, Collector directory data, and Namespace data. You can then incorporate extracted data into ERP data models and remote tables for use as a data source when building apps on ServiceNow. For more information, see the following topics:

-   [View ERP extraction tables](../../erp-integration/task/view-etl-data-sources.md)
-   [Standard ERP models and extraction tables for ERP Data Hub](../../erp-integration/reference/erp-canvas-standard-extraction-tables.md)

**Parent Topic:**[Configuring ERP Customization Mining](../concept/configuring-ecm.md)

