---
title: Deploy the ABAP program for SAP
description: Deploy the Advanced Business Application Programming \(ABAP\) program to establish a connection between your SAP system and your ServiceNow instance. Deploying the ABAP program allows data to be shared between SAP and your ServiceNow instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/software-asset-management/import-abap-program-sap.html
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Set up SAP integration to establish a connection with SAP, Software Asset Management publisher pack for SAP, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Deploy the ABAP program for SAP

Deploy the Advanced Business Application Programming \(ABAP\) program to establish a connection between your SAP system and your ServiceNow instance. Deploying the ABAP program allows data to be shared between SAP and your ServiceNow instance.

## Before you begin

Download the SAP ABAP for Software Asset Management application from the [ServiceNow Store](https://store.servicenow.com/). Make sure you download the application version that is compatible with the Australia release.

**Note:** The ABAP program performs only read operations on existing standard functional modules. It doesn't modify these modules in any way.

Role required: sam\_admin, SAP Basis administrator

## About this task

To deploy the ABAP program, import the transport files that are provided through the SAP ABAP for Software Asset Management application and then configure a service provider with the service-oriented architecture \(SOA\) Manager.

**Note:** If you upgrade your ServiceNow instance, you must download and deploy the version of the ABAP program that is compatible with the new release.

You must read all Release notes and Requirements under the Version details section in the SAP ABAP for Software Asset Management application. There are two transport files in the download folder, but only one of them should be deployed according to your SAP system requirements.

There are three different transport requests \(TR\) provided in the ABAP ZIP file. Refer the following table to see what purpose each transport request serves depending on the system type and required functionality.

|Transport type|Purpose|Supported systems|Notes|
|--------------|-------|-----------------|-----|
|Central Transport – With Digital Access|Includes Digital Access logic for extracting data such as sales documents, purchase orders, financial invoices, and so on.|SAP ERP Central Component \(ECC\), SAP S/4HANA|Used when Digital Access data collection is required.|
|Central Transport – Without Digital Access|Doesn't include Digital Access logic for document extraction.|SAP ECC, SAP GRC, SAP S/4HANA|Used when Digital Access data collection isn't required.|
|Satellite Transport|Contains HANA Database–specific code that is required for data extraction from satellite systems.|SAP S/4HANA|Import only if the satellite/RFC system is S/4HANA.|

**Note:** You must deploy one of the central transport types according to your requirement. Satellite transport is required only if the RFC system is SAP S/4HANA.

For further information on SAP setup, see [KB0813999](https://support.servicenow.com/kb_view.do?sysparm_article=KB0813999).

For more information on SAP and its related tools, refer to the [SAP Help Portal](https://help.sap.com/viewer/index).

## Procedure

1.  In your SAP system, import all applicable transport files using the SAP Transport Management System \(STMS\).

2.  Copy and extract the `COFILE` and `DATA` files to your directory.

3.  Start STMS and select **Import Overview**.

4.  Double-click the target system, select **Extras** &gt; **Other Requests** &gt; **Add**, and then enter the transport request number.

5.  Highlight the request and select **Request** &gt; **Import**.

6.  From the Import Transport Request window, enter the client number in the **Target Client** field.

7.  Select the Options tab, and then select the **Ignore Invalid Component Version** check box.

8.  Select **OK**.

9.  Verify the RFC connection.


## What to do next

In your SAP system, configure a service provider with the SOA Manager and generate a Web Services Description Language \(WSDL\) URL for the SAP service definition. For details, see [Create a WSDL for the SAP service definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/create-wsdl-sap-service.md).

**Parent Topic:**[Set up SAP integration to establish a connection with SAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/setup-sap-integration.md)

