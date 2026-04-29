---
title: Activate and configure the VirusTotal integration
description: Before you can use the VirusTotal integration, you must download it from the ServiceNow Store.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [VirusTotal integration setup, VirusTotal integration, Threat Intelligence integrations, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Activate and configure the VirusTotal integration

Before you can use the VirusTotal integration, you must download it from the ServiceNow Store.

## Before you begin

Role required: admin

Threat Intelligence must be installed and activated before you can use VirusTotal. The VirusTotal integration has been upgraded to version 3 APIs.

## Procedure

1.  [Download the integration from the ServiceNow Store](../../../security-incident-response/reference/download-app-first-time.md).

2.  When the installation is complete, access VirusTotal and obtain the API Key under your VirusTotal profile.

3.  In your instance, navigate to **Security Operations** &gt; **Integration Configuration**.

    The available security integrations appear as a series of cards.

4.  In the VirusTotal card, click **Configure**.

<table id="table_hbs_ccm_vzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the integration. For example, VirusTotal.

</td></tr><tr><td>

API Key

</td><td>

Enter \(or paste\) the **API Key** you acquired from the VirusTotal site.

</td></tr><tr><td>

Enable VT Private Scanning

</td><td>

Select this check box to analyze files with VirusTotal in a privacy preserving fashion. The files uploaded via this offering won't be shared with anyone beyond your organization, and will remain in VirusTotal only for a brief period of time.The resulting analyses will be ephemeral too and only visible to your VirusTotal group.

**Important:** To use the VT Private Scanning, your VirusTotal license should be entitled to this feature.

</td></tr><tr><td>

Send URL as SHA-256 Hash

</td><td>

Select this check box to send the URLs as hashes for threat lookup and protect the users' privacy on the integration.**Note:** If disabled, the URL is sent as Base64 encoding to the VirusTotal API.

</td></tr></tbody>
</table>5.  Click **Submit**.

    ![VirusTotal Configuration page](../image/virus-total-config.png)


## Result

After it is configured, VirusTotal can be selected for performing lookups on observables in Threat Intelligence and on observables in security incidents.

**Related topics**  


[Perform lookups on observables](../../../threat-intelligence/task/perform-lookups-on-observables.md)

