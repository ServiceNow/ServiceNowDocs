---
title: Get started with the McAfee ESM - Incident Enrichment integration
description: McAfee ESM protects endpoints against viruses, spyware, Trojan horses, and other malware threats and integrates easily with Security Operations. Before you can use the McAfee ESM - Incident Enrichment integration, you must download it from the ServiceNow Store and add the appropriate API Base URL and login credentials.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [McAfee ESM - Incident Enrichment Integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Get started with the McAfee ESM - Incident Enrichment integration

McAfee ESM protects endpoints against viruses, spyware, Trojan horses, and other malware threats and integrates easily with Security Operations. Before you can use the McAfee ESM - Incident Enrichment integration, you must download it from the ServiceNow Store and add the appropriate API Base URL and login credentials.

## Before you begin

Role required: sn\_si\_admin

## Procedure

1.  [Download the integration from the ServiceNow Store](../../../security-incident-response/reference/download-app-first-time.md).

2.  When the installation is complete, navigate to **Security Operations** &gt; **Integrations** &gt; **Integration Configuration**.

    The available security integrations appear as a series of cards.

3.  In the McAfee ESM - Incident Enrichment card, click **New**.

    ![McAfee ESM configuration](../image/intel-config.png)

4.  Fill in the fields, as needed.

<table id="table_l2p_dcs_ns"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of this configuration.

</td></tr><tr><td>

McAfee ESM API Base URL

</td><td>

The base URL you acquired from the McAfee ESM site.

</td></tr><tr><td>

Link URL

</td><td>

\[Optional\] The Link URL that links to an McAfee ESM instance, when available.**Note:** If you're getting an error, please use the McAfee ESM API Base URL.

</td></tr><tr><td>

Username

</td><td>

Your McAfee ESM username.

</td></tr><tr><td>

Password

</td><td>

Your McAfee ESM password.

</td></tr><tr><td>

Max Rows

</td><td>

The maximum number of rows you want to search.

</td></tr><tr><td>

Earliest Result \(days\)

</td><td>

The earliest results you want to see in number of days.

</td></tr><tr><td>

Include raw data samples in search results

</td><td>

Select this to include samples of raw data in your sightings search results. The amount of data returned depends on your setting in the **number of rows of raw data** property in [Security Incident Response properties](../../../security-incident-response/reference/installed-with-sir.md).

</td></tr><tr><td>

MID Server

</td><td>

Select **Any** to use any active MID Server, or select a specific MID Server name.

</td></tr></tbody>
</table>    **Note:** Configuring this integration activates workflows. To manage the workflows, navigate to the **Workflow Editor**.

5.  Click **Submit**.

    The integration configuration card displays.

6.  When viewing the new configuration card, you can click **Configure** or **Delete** to change or delete the configuration, respectively.

7.  To return to the original list of integration configuration cards, select **No** from the **Show Configurations** drop-down list.


