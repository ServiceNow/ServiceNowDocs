---
title: Create Connection and Credential alias for SCCM deployments
description: Microsoft System Center Configuration Manager \(SCCM\) requires the appropriate credentials to deploy applications using the Client Software Distribution application.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring SCCM, Client software distribution from SCCM, Client Software Distribution using Integration Hub, Integration Hub available solutions, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Create Connection and Credential alias for SCCM deployments

Microsoft System Center Configuration Manager \(SCCM\) requires the appropriate credentials to deploy applications using the Client Software Distribution application.

## Before you begin

Role required: sn\_client\_sf\_dist.csd\_admin or admin

## About this task

Client software distribution requires Windows credentials that have administrative rights on the SCCM server.

## Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name to uniquely identify the alias. For example, `CSD Alias`.|
    |ID|System generated unique ID.|
    |Application|Application scope that contains this record.|
    |Type|Alias type. Select **Connection and Credential**.|
    |Connection type|Connection type. Select **Basic**.|
    |Support Multiple Active Connections|Option to specify if the alias supports multiple active connections.|
    |Default Retry Policy|Default retry policy associated with **Connection Alias**.|
    |Configuration Template|Template that defines the inputs required to set up the spoke.|

4.  Right-click the form header, and click **Save**.

5.  Click the **Create New Connection &amp; Credential** related link.

6.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |SCCM Server Instance Name|Name to uniquely identify the SCCM server.|
    |Host|Fully qualified domain name of the target host where the SCCM server is installed.|
    |Credential Name|Credential record associated with the connection and credential alias.|
    |User Name|User name with access to the target Windows host.|
    |Password|Password for the account.|

7.  Click **Create**.


## Result

Connection record and SCCM Server Instance are created and associated with the connection and credential alias.

**Parent Topic:**[Configuring SCCM](../concept/configure-sccm-ihub.md)

