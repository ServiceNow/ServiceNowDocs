---
title: Deploy the ABAP program for SAP
description: Deploy the Advanced Business Application Programming \(ABAP\) program to establish a connection between your SAP system and your ServiceNow instance. Deploying the ABAP program allows data to be shared between SAP and your ServiceNow instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/software-asset-management/import-abap-program-sap.html
release: brazil
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Set up SAP integration to establish a connection with SAP, Software Asset Management publisher pack for SAP, Supported software publisher licenses, Software Asset Management, IT Asset Management, Asset Management]
---

# Deploy the ABAP program for SAP

Deploy the Advanced Business Application Programming \(ABAP\) program to establish a connection between your SAP system and your ServiceNow instance. Deploying the ABAP program allows data to be shared between SAP and your ServiceNow instance.

## Before you begin

Download the SAP ABAP for Software Asset Management application from the [ServiceNow Store](https://store.servicenow.com/). Download the application version that is compatible with the Brazil release.

**Note:** The ABAP program performs only read operations on existing standard functional modules. It does not modify these modules in any way.

Role required: sam\_admin, SAP Basis administrator

## About this task

To deploy the ABAP program, import the transport files that are provided through the SAP ABAP for Software Asset Management application and then configure a service provider with the service-oriented architecture \(SOA\) Manager.

**Note:** If you upgrade your ServiceNow instance, you must download and deploy the version of the ABAP program that is compatible with the new release.

You must read all Release notes and Requirements under the Version details section in the [SAP ABAP for Software Asset Management](https://store.servicenow.com/store/app/85596fae1be06a50a85b16db234bcbff)application. The download folder contains multiple transport files. Deploy only the transport requests that apply to your SAP system type and the functionality that you require.

Four different transport requests \(TR\) are provided in the ABAP ZIP file. Refer to the following table to see what purpose each transport request serves depending on the system type and required functionality.

<table id="table_sfk_mry_fjc"><thead><tr><th>

Transport type

</th><th>

Purpose

</th><th>

Supported systems

</th><th>

Notes

</th></tr></thead><tbody><tr><td>

Central Transport – With Digital Access

</td><td>

Includes Digital Access logic for extracting data such as sales documents, purchase orders, financial invoices, and so on.

</td><td>

-   SAP ERP Central Component \(ECC\)
-   SAP S/4HANA
-   SAP S/4HANA Cloud, Private Edition

</td><td>

Used when Digital Access data collection is required.

</td></tr><tr><td>

Central Transport – Without Digital Access

</td><td>

Does not include Digital Access logic for document extraction.

</td><td>

-   SAP ECC
-   SAP Solution Manager
-   SAP GRC
-   SAP S/4HANA
-   SAP S/4HANA Cloud, Private Edition

</td><td>

Used when Digital Access data collection is not required.

</td></tr><tr><td>

Satellite Transport for On-Premises

</td><td>

Contains SAP S/4HANA Database–specific code that is required for data extraction from satellite systems.

</td><td>

SAP S/4HANA

</td><td>

Import only if the satellite or RFC system is SAP S/4HANA.

</td></tr><tr><td>

Satellite Transport for Private Cloud

</td><td>

Contains SAP S/4HANA Database–specific code and Full Usage Equivalent \(FUE\) user classification code that is required for data extraction from satellite systems.

</td><td>

SAP S/4HANA Cloud, Private Edition

</td><td>

Import only if the satellite or RFC system is SAP S/4HANA Cloud, Private Edition.

</td></tr></tbody>
</table>**Note:** You must deploy one of the central transport types according to your requirement. For satellite or RFC systems, deploy the satellite transport that matches your deployment: the on-premises satellite transport for SAP S/4HANA satellite systems, or the Private Cloud satellite transport for SAP S/4HANA Cloud, Private Edition satellite systems.

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

In your SAP system, configure a service provider with the SOA Manager and generate a Web Services Description Language \(WSDL\) URL for the SAP service definition. For details, see [Create a WSDL for the SAP service definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/create-wsdl-sap-service.md).

**Parent Topic:**[Set up SAP integration to establish a connection with SAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/setup-sap-integration.md)

