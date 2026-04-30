---
title: Install and configure the Netskope DLP integration for Data Loss Prevention
description: Install and configure the Netskope DLP integration from   ServiceNow Store   ServiceNow AI Platform instance. You can start investigating DLP incidents using the  Netskope DLP incident data.
locale: en-US
release: zurich
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Data Loss Prevention Incident Response Integration with Netskope, Integrate, Data Loss Prevention Incident Response, Security Operations]
---

# Install and configure the Netskope DLP integration for Data Loss Prevention

Install and configure the Netskope DLP integration from   ServiceNow Store   ServiceNow AI Platform instance. You can start investigating DLP incidents using the  Netskope DLP incident data.

## Before you begin

Role required: sn\_dlir.admin

## Procedure

1.  Download the  Netskope DLP integration from the ServiceNow Store and install it.

2.  Navigate to  **Security Operations ** &gt; **Integrations ** &gt; **Integration Configurations**

3.  Search for  `DLP Incident Response Integration with Netskope` tile, and click  **Configure**.

4.  On the form, fill in the fields.

    **Note:** Make sure your Netskope API v2 Token has the below endpoint privileges:

    -   Read: /api/v2/incidents/dlpincidents
    -   Read: /api/v2/events/dataexport/events/incident
    -   Read + Write: /api/v2/incidents/update
    ![Create REST API Token](../image/create_rest_api.png)![Netskope Configuration](../image/netskope-config.png)

    |Field|Description|
    |-----|-----------|
    |Name|Name of the Netskope DLP integration configuration.|
    |Netskope Tenant|The Netskope base URL for the Netskope tenant.|
    |Netskope API v2 Token|Token configured for REST API v2 on your user account at Netskope.|

5.  Click **Submit**.


## Result

**Note:** Please connect netskope sub prod to the ServiceNow sub prod. Keep all the username and passwords in sync across the instances to avoid accounts getting logged out.

After you successfully validate and submit the configuration, the Netskope DLP Integration is saved on the Security Integrations page as a tile.

**Parent Topic:**[Data Loss Prevention Incident Response Integration with Netskope](../concept/dlp-incident-response-integration-netskope.md)

