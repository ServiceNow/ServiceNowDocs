---
title: Configure service maps for Source-to-Pay
description: For configuring service maps, provide the connection end point and the ERP credentials that you set up for your authentication profile. Also, create a separate web service record for each service request that you want to customize.
locale: en-US
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integration settings on Source-to-Pay side, Source-to-Pay integration framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Configure service maps for Source-to-Pay

For configuring service maps, provide the connection end point and the ERP credentials that you set up for your authentication profile. Also, create a separate web service record for each service request that you want to customize.

## Before you begin

-   Verify that the application scope is set to Finance – ERP Integration.
-   Ensure that the MID Server is installed and configured in your ServiceNow instance to connect to the ERP server. See [Installing the MID Server](https://www.servicenow.com/docs/access?context=mid-server-installation&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US) for details.

    **Note:** The MID Server integration is required only for an ERP integration using SOAP services.

-   For SOAP type service, SOAP API details \(WSDL information – soap action and endpoint details\), provided by ERP.
-   For REST type service, REST API details, as provided by ERP.

Role required: sn\_fcms\_intg.integration\_user

## About this task

If the application needs to support multiple ERP instances, create separate web services for each ERP instance.

## Procedure

1.  Navigate to **All** &gt; **Finance – ERP Integration** &gt; **ERP Source Configuration**.

2.  Open the ERP source for which you need to configure service maps.

3.  In the Service Mappings related list, click **New**.

4.  On the form, fill in the fields.

<table id="table_bl5_x5z_33b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the service map.

</td></tr><tr><td>

Service

</td><td>

Service to process the selected request.

</td></tr><tr><td>

Source

</td><td>

Name of the ERP source.

</td></tr><tr><td>

Type

</td><td>

Type of web service to connect with ERP. Select a type based on your ERP system.-   **SOAP**: Select if you are using SOAP services with your integration.
-   **REST**: Select if you are using REST services with your integration.


</td></tr><tr><td>

Use MID

</td><td>

Option to use MID Server to connect with ERP.The field is required only when you select SOAP in the **Type** field.

</td></tr><tr><td>

Credential alias

</td><td>

Basic authentication profile associated with the service.

</td></tr><tr><td>

SOAP action

</td><td>

SOAP action provided by ERP.This field appears when SOAP is selected in the **Type** field.

</td></tr><tr><td>

SOAP endpoint

</td><td>

SOAP endpoint provided by ERP.This field appears when SOAP is selected in the **Type** field.

</td></tr><tr><td>

Envelope

</td><td>

Reference to generate the service element maps.This field appears when SOAP is selected in the **Type** field.

</td></tr><tr><td>

HTTP Method

</td><td>

Method for the web service.This field appears when REST is selected in the **Type** field.

</td></tr><tr><td>

Base URL

</td><td>

Base URL of endpoint provided by ERP.This field appears when REST is selected in the **Type** field.

</td></tr><tr><td>

Resource Path

</td><td>

Path of the resource provided by ERP.This field appears when REST is selected in the **Type** field.

</td></tr></tbody>
</table>5.  Click **Submit**.


