---
title: Create a connection for SAP concur event subscription service
description: Create connection and credential records for the Operational Sustainability Integration with Concur so that you can establish a new connection.
locale: en-US
release: zurich
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integrating ESG Management \(formerly ESG\) with SAP Concur, Integrating ESG Management \(formerly ESG\) with other applications, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Create a connection for SAP concur event subscription service

Create connection and credential records for the Operational Sustainability Integration with Concur so that you can establish a new connection.

## Before you begin

Role required: sn\_esg.admin

## Procedure

1.  Navigate to **All** &gt; **Environmental, Social, and Governance** &gt; **SAP Concur** &gt; **Connection and Credentials Alias**.

2.  Select **SAP Concur Event Subscription Service**.

3.  On the Connection and Credentials Aliases form, select the **Create New Connection &amp; Credential** related link.

    Contact your Concur administrator to obtain the information for the required fields.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Connection information|
    |Name|Name of the OAuth connection.|
    |Connection URL|Concur Connection URL.|
    |Version|Version of the API. This field is automatically set to **v4**.|
    |Credential information|
    |Token URL|Concur OAuth Server's token endpoint.|
    |Client ID|OAuth Client ID configured in Concur.|
    |Client Secret|OAuth Client Secret configured in Concur.|

5.  Select **Create and Get OAuth Token**.


## Result

The Oauth token is created successfully.

**Parent Topic:**[Integrating ESG Management \(formerly ESG\) with SAP Concur](../concept/integrate-esg-with-concur.md)

