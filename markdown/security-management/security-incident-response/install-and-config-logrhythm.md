---
title: Install the plugin and configure LogRhythm
description: Before you run the integration on your instance, complete the installation and configuration steps so the application properly integrates with Security Operations on the ServiceNow AI Platform.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [LogRhythm Overview, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Install the plugin and configure LogRhythm

Before you run the integration on your instance, complete the installation and configuration steps so the application properly integrates with Security Operations on the ServiceNow AI Platform®.

## Before you begin

Role required: admin

Complete the following setup checklist prior to installation. These setup tasks are required for a smooth installation and configuration. The latest LogRhythm version is 7.8 or later.

**Note:** Your existing alarm profiles will no longer be supported on the latest LogRhythm version, so you need to create new alarm profiles and perform the required configurations.

<table id="table_xxz_jyj_4cb"><thead><tr><th>

Setup task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Verify that you have assigned the required ServiceNow AI Platform® and Security Incident Response \(SIR\) roles.

</td><td>

The following roles are required for installation, configuration, and verification of expected results:-   The system administrator \(admin\) installs the application plugin and assigns the security incident administrator \(sn\_si.admin\) role.
-   The \(sn\_si.admin\) oversees the following tasks:
    -   Names, creates, and edits alarm profiles.
    -   Maps and filters alarms – identifies specific LogRhythm alarms that create security incidents and configures how these alarm fields map to a ServiceNow AI Platform® security incident.
    -   Previews security incident details for accuracy prior to finalizing the configuration.
    -   Ingests historical alarms and schedules pulled alarms.
    -   Assigns the security incident analyst \(sn\_si.analyst\) role.
    -   This role also has access to the Security Operations module.
-   The security incident analyst \(sn\_si.analyst\) responds to security incidents that are created based on the alarm profile settings.

</td></tr><tr><td>

Obtain a LogRhythm API user name and password and verify that you are using version LogRhythm 7.8 or later.

</td><td>

Visit the product website for information on API keys and to create an account: [LogRhythm Enterprise website](https://logrhythm.com/). The user accounts, credentials, and certificates must be configured properly prior to installing the application. The integration requires LogRhythm version 7.8 or later and the LogRhythm REST APIs.

 See [Set up the REST API for LogRhythm](drilldown-api-lr.md).

</td></tr><tr><td>

Verify that you have installed and configured a MID Server.

</td><td>

A MID Server is required in your ServiceNow AI Platform environment. See the [ServiceNow Product Documentation website](https://servicenow.com/docs) for information about how to set up and configure MID Servers.

</td></tr><tr><td>

Verify that the ServiceNow core applications that are required to support the integration are installed and activated before you install the application for the integration.

</td><td>

For the Rome release and later family releases, the Security Incident Response Dependency plugin \(com.snc.si\_dep\) is required. This plugin automatically installs all the dependencies that are required to support the Security Incident Response product. Install and activate this plugin before you install and activate the other Security Operations applications required by the integration.

 Verify that the following Security Operations applications are installed and activated from the ServiceNow Store. If not installed, install and activate one application at a time in the following order to ensure a smooth installation.

 1.  Security Incident Response
2.  Security Integration Framework
3.  Security Support Common
4.  Security Support Orchestration

 For more information on setting up your ServiceNow AI Platform instance for the integration, see [Get entitlement for a Security Operations product or application](../../security-incident-response/task/entitle-secops-product.md) and [Activate a ServiceNow Store application](../../security-incident-response/task/activate-entitled-store-app.md).

</td></tr></tbody>
</table>**Important:** If you have any connectivity issues to the LogRhythm client console, refer to the [Verify connectivity for LogRhythm](verify-connectivity.md).

## Procedure

1.  If you have not installed the application for the integration, see [Install a Security Operations integration](../../security-incident-response/task/install-non-core-apps.md) and follow the steps to install it.

2.  Once the installation completes, navigate to **Integrations** &gt; **Integrations Configurations** and locate the LogRhythm tile.

3.  Click **Configure**.

    ![Task: Click Configure button for LogRhythm.](../image/lr-config-tile-4-2.png)

4.  Click the **New Configuration** link.

    ![Task: Click New Configuration link.](../image/lr-config-2-4-2.png)

5.  On the form, fill in the fields:

<table id="table_r5j_x2j_3tb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

LogRhythm server name, for example, `logrhythm-server-a`.

</td></tr><tr><td>

Base URL

</td><td>

Base URL hosting the LogRhythm REST API.The MID Server permits access to the network where the LogRhythm Client Console is hosted. This URL is where the LogRhythm server is hosted within that network. Click the lock icon on the right-end to edit the field and enter text for a URL, for example, `https://logrhythm.secops-eng.com:8501/`.

</td></tr><tr><td>

API Token

</td><td>

Enter the token that is associated with your REST API that you created on the LogRhythm Client Console.

</td></tr><tr><td>

On-Premise Deployment

</td><td>

Option to select if it's a LogRhythm on-premise deployment.

</td></tr><tr><td>

MID Server

</td><td>

Specific MID Server that is set up in your environment. Only the MID Servers that are active and have been validated are available from this choice list.

</td></tr></tbody>
</table>    The following figure is an example of a completed form.

    ![A completed LogRhythm Configuration form.](../image/logrhythm-configuration.png)

6.  Click **Validate and save**.

    After validation is successfully completed, a message is displayed and the LogRhythm Configurations page is reloaded. The next step is to create an alarm profile.


## What to do next

After you successfully complete the validation, the next step is to [Creating an alarm profile for LogRhythm](create-alarm-profile-logrhythm.md).

**Parent Topic:**[LogRhythm Overview](../concept/ovrview-logrhythm.md)

**Previous topic:**[Set up the REST API for LogRhythm](drilldown-api-lr.md)

**Next topic:**[Creating an alarm profile for LogRhythm](create-alarm-profile-logrhythm.md)

