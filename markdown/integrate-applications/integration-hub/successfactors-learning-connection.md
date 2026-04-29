---
title: Create a connection record for the SuccessFactors Learning spoke
description: Create a connection record for your spoke. The SuccessFactors Learning connection and credential aliases use these connections to perform actions in SuccessFactors Learning.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [SuccessFactors Learning Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Create a connection record for the SuccessFactors Learning spoke

Create a connection record for your spoke. The SuccessFactors Learning connection and credential aliases use these connections to perform actions in SuccessFactors Learning.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connections &amp; Credentials Aliases**.

2.  Open the alias record for **SuccessFactors Learning**.

3.  From the **Connections** tab, click **New**.

4.  On the form, fill these fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name to uniquely identify the record. For example, `<Application-Name> Connection`.|
    |Credential|Credential record created for SuccessFactors Learning. For example, `<Application-Name> Cred`.|
    |Connection alias|Alias record associated with this connection.|
    |Host|Fully qualified domain name of the target host where the **Learning** server is installed. For example, `<host>.<domain>.com`.|
    |Connection URL|Base URL to connect to **Learning**. Enter: `https://scfpart001153.scdemo.successfactors.eu/learning`|
    |Active|Option to actively use the connection record.|
    |Domain|Domain that the action runs in.|
    |Override default port|Target port used by the connection. If blank, the system uses the default port.|
    |Use MID server|Option to use a MID Servers for this connection. If the check box is selected, define the fields in the Advanced MID Server Configuration related list.|

5.  Click **Submit**.


