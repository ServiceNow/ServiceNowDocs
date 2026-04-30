---
title: ERP Data Hub connection and credentials field descriptions
description: The Connection and Credential Alias modal contains connection and credential details that specify how ERP Data Hub connects to the ERP \(Enterprise Resource Planning\) system.
locale: en-US
release: xanadu
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [ERP Data Hub field descriptions, ERP Data Hub reference, ERP Data Hub, Building low-code applications, Developing your application, Building applications]
---

# ERP Data Hub connection and credentials field descriptions

The Connection and Credential Alias modal contains connection and credential details that specify how ERP Data Hub connects to the ERP \(Enterprise Resource Planning\) system.

## Enter the Connection Information field descriptions

<table id="table_vdc_glp_cbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

Label or alias for the connection.

</td></tr><tr><td>

Host name or IP Address to SAP Application server or the Load Balancer

</td><td>

Host name or IP address of the ERP system server or load balancing host that connects to the ERP system.

</td></tr><tr><td>

Login Language

</td><td>

Two-character language code of the language of the ERP server you're connecting to.

</td></tr><tr><td>

SAP Client

</td><td>

Client value of the connection host where the SAP instance is installed.

</td></tr><tr><td>

SAP System Number

</td><td>

System number of the connection host where the SAP instance is installed.Don't enter anything in this field if the connection you're specifying is for a load balancer.

</td></tr><tr><td>

Load Balancing: SAP Message Server Port number or logical name

</td><td>

Port number or name of the message server host.Enter this value only if the connection you're specifying is for a load balancer.

</td></tr><tr><td>

Load Balancing: SAP R3 Name

</td><td>

Three-character system ID of the ABAP system to be addressed.Enter this value only if the connection you're specifying is for a load balancer.

</td></tr><tr><td>

Load Balancing: SAP Load Balancing Group

</td><td>

Name of load balancer.Enter this value only if the connection you're specifying is for a load balancer.

</td></tr></tbody>
</table>## Enter the Credential Information field descriptions

|Field|Description|
|-----|-----------|
|User Name|User name to log in to the system of record to access ERP data.|
|Password|Password to authenticate and log in to the system of record.|
|Credential Name|Alias or name for the login credential.|

**Parent Topic:**[ERP Data Hub field descriptions](erp-canvas-field-descriptions.md)

