---
title: Install and configure RISKIQ and WHOISIQ
description: Before you run the integration on your instance, complete the installation and configuration steps so the RISKIQ and WHOISIQ applications properly integrate with ServiceNow AI Platform Security Operations.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [RISKIQ and WHOISIQ integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Install and configure RISKIQ and WHOISIQ

Before you run the integration on your instance, complete the installation and configuration steps so the RISKIQ and WHOISIQ applications properly integrate with ServiceNow AI Platform Security Operations.

## Before you begin

Role required: admin, RISKIQ and WHOISIQ admin.

Complete the following setup checklist prior to installation. These setup tasks are required for a smooth installation and configuration.

<table id="table_gd1_sfv_zcb"><thead><tr><th>

Setup task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Verify that you have assigned the required roles.

</td><td>

The following roles are required for installation, configuration, and verification of expected results:-   The System Administrator \(admin\) installs the app and assigns the Security Incident Administrator \(sn\_si.admin\) role.
-   The Security Incident Administrator \(sn\_si.admin\) oversees configuration and verifies expected results. This role also has access to the Security Operations module and assigns the Security Incident Analyst \(sn\_si.analyst\) role.
-   The Security Incident Analyst \(sn\_si.analyst\) works with Security Incident records.

</td></tr><tr><td>

Obtain an Username and API key.

</td><td>

Visit the website for information on the API key and how to create an account: [RISKIQ website](https://api.riskiq.net/api/concepts.html). The configuration requires that you enter the API key.

</td></tr><tr><td>

Verify that the ServiceNow core applications that are required to support the integration are installed and activated before you install the application for the integration.

</td><td>

Madrid and later release requirements

 For the Madrid release and later family releases, the Security Incident Response Dependency plugin \(com.snc.si\_dep\) is required. This plugin automatically installs all the dependencies that are required to support the Security Incident Response product. Install and activate this plugin before you install and activate the other Security Operations applications required by the integration.

 Verify that the following Security Operations applications are installed and activated from the ServiceNow Store. If not installed, install and activate one application at a time in the following order to ensure a smooth installation.

 1.  Security Incident Response
2.  Security Integration Framework
3.  Security Support Common
4.  Security Support Orchestration

 For more information on setting up your ServiceNow AI Platform instance for the integration, see [Get entitlement for a Security Operations product or application](../../security-incident-response/task/entitle-secops-product.md) and [Activate a ServiceNow Store application](../../security-incident-response/task/activate-entitled-store-app.md).

</td></tr></tbody>
</table>## Procedure

1.  If you have not installed the application for the integration, see [Install a Security Operations integration](../../security-incident-response/task/install-non-core-apps.md) and follow the steps to install it.

2.  Once the installation completes, navigate to **Security Operations** &gt; **Integrations** &gt; **Integrations Configurations** and locate the API tile.

3.  Click **Configure**.

    ![RISKIQ Configure button](../image/riskiq-tile.png)

4.  In the RiskIQ Configuration dialog box that is displayed, enter the **Username** and **API key**.

    ![Task: Enter the Username and API key.](../image/riskiq-configuration.png)

5.  Click **Submit**.

6.  Verify successful configuration.

    When configuration is successfully completed, the Security Integrations page with the integration tiles is displayed.


If an error message is displayed, the Username or API key may be invalid. Verify that your username and API key are correct:

![Configuration error message](../image/riskiq-config-error.png "Troubleshooting")

**Parent Topic:**[RISKIQ and WHOISIQ integration](../concept/riskiq-lookups.md)

**Previous topic:**[Supported observables for RISKIQ and RISKIQ WHOISIQ](../reference/riskiq_supported_obsv.md)

**Next topic:**[Verify expected results for RISKIQ SSL certificate lookups](verify-expected-rslts-for-riskiq.md)

