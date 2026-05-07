---
title: Zero Copy Connector for ERP connection and credentials field descriptions
description: The Connection and Credential Alias modal contains connection and credential details that specify how Zero Copy Connector for ERP \(Enterprise Resource Planning\) connects to the ERP system.
locale: en-US
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, system, connection, credential, alias]
breadcrumb: [Zero Copy Connector for ERP field descriptions, Reference, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Zero Copy Connector for ERP connection and credentials field descriptions

The Connection and Credential Alias modal contains connection and credential details that specify how Zero Copy Connector for ERP \(Enterprise Resource Planning\) connects to the ERP system.

For process details, see [Configure an SNC connection in Zero Copy Connector for ERP](../task/erpc-configure-an-snc-connection-in-erp-canvas.md).

## Connection Information field descriptions

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

Host name or IP address of the ERP system server or load-balancing host that connects to the ERP system.

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

</td></tr><tr><td>

The communication partner's SNC name

</td><td>

Canonical name. \(Required if **SNC Connection** field is set to **true**.\)

</td></tr><tr><td>

SNC Connection

</td><td>

To use an SNC with a connection, set to **true**.

</td></tr><tr><td>

The quality of protection \(QoP\) level for SNC

</td><td>

Enter one of the following numbers \(just the number, not the text\):-   1: Apply authentication only
-   2: Apply authentication and integrity protection
-   3: Apply authentication, integrity, and privacy protection \(encryption\)
-   8: Apply global default protection
-   9: Apply the maximum protection

</td></tr><tr><td>

The external security product's library

</td><td>

Absolute path of the SAP Cryptography library file. \(Required if **SNC Connection** field is set to **true**.\)

</td></tr><tr><td>

The SNC mode flag to indicate whether the communication should use SNC protection

</td><td>

Enter one of the following numbers \(just the number, not the text\):-   0: Don't apply SNC to connections
-   1: Apply SNC to connections

</td></tr><tr><td>

SNC : Client SNC Name

</td><td>

Client Personal Security Environment \(PSE\) name. \(Required if **SNC Connection** field is set to **true**.\)

</td></tr></tbody>
</table>## Credential Information field descriptions

|Field|Description|
|-----|-----------|
|User Name|User name to log in to the system of record to access ERP data.|
|Password|Password to authenticate and log in to the system of record.|
|Credential Name|Alias or name for the login credential.|

**Parent Topic:**[Zero Copy Connector for ERP field descriptions](erp-canvas-field-descriptions.md)

