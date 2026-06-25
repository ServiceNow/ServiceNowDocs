---
title: Install and configure the MISP integration for Security Operations
description: Install and configure the MISP integration for Security Operations from the ServiceNow Store on your ServiceNow AI Platform instance so that you can start investigating security incidents using the MISP data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/install-and-configure-misp.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [MISP administration, MISP integration for Security Operations, Threat Intelligence integrations, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Install and configure the MISP integration for Security Operations

Install and configure the MISP integration for Security Operations from the ServiceNow Store on your ServiceNow AI Platform instance so that you can start investigating security incidents using the MISP data.

## Before you begin

Ensure that you’ve installed the valid SSL certificates on the MISP server.

Role required: sn\_si.admin

## Procedure

1.  Download the MISP integration for Security Operations from the ServiceNow Store and install it.

2.  Navigate to **Security Operations** &gt; **Integrations** &gt; **Integration Configurations**.

3.  Search for the MISP -SIR/TI Integration tile and click **Configure**.

4.  On the form, fill in the fields.

<table id="table_kyc_qbg_pa1"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the MISP instance configuration.

</td></tr><tr><td>

MISP Server URL

</td><td>

URL for the MISP server that serves as the REST endpoint for the MISP server.

</td></tr><tr><td>

API Key

</td><td>

API key that is configured for your user account on the MISP server. The API key corresponds to the **Authkey** in the MISP server.

</td></tr><tr><td>

On Premises Deployment

</td><td>

Option that you can select if your MISP server is deployed in an on-premise instance. When you select the **On Premises Deployment** option, you must use the MID Server to connect to the MISP server.

</td></tr><tr><td>

MID Application

</td><td>

String field that identifies the MID Application name that is used to communicate with MISP.This field is required when you select the **On Premises Deployment** option. For information on how to configure the MID server for your application, see [Configure a MID Server for each application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/t_SpecifyMIDServerApplications.md)

</td></tr></tbody>
</table>5.  Click **Submit**.


## Result

After you successfully validate and submit the configuration, the MISP - SIR/TI Integration is saved on the Security Integrations page as a tile.

**Parent Topic:**[MISP administration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/misp-administration.md)

**Related topics**  


[Getting started with MISP integration for Security Operations]()

[Review the MISP integration settings]()

[Configure MISP sighting searches]()

[Configure how an automatic event is created]()

[MISP event data]()

[Associated MISP events]()

[MISP user information]()

[Domain separation and MISP]()

[Troubleshooting MISP integration]()

