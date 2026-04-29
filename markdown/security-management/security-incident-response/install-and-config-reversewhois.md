---
title: Install and configure Reverse Whois
description: Before you run the integration on your instance, complete the installation and configuration steps so the Reverse Whois application properly integrates with the Security Operations product.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Reverse Whois integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Install and configure Reverse Whois

Before you run the integration on your instance, complete the installation and configuration steps so the Reverse Whois application properly integrates with the Security Operations product.

## Before you begin

Complete the following setup checklist prior to installation. These setup tasks are required for a smooth installation and configuration.

<table id="table_ywj_yls_ycb"><thead><tr><th>

Setup task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Verify that you have assigned the required ServiceNow roles.

</td><td>

The following roles are required for installation, configuration, and verification of expected results:-   The System Administrator \(admin\) installs the app and assigns the Security Incident Administrator \(sn\_si.admin\) role.
-   The Security Incident Administrator \(sn\_si.admin\) oversees the configuration. The security incident administrator also assigns the Security Incident Analyst \(sn\_si.analyst\) role.
-   The Security Incident Analyst \(sn\_si.analyst\) performs domain lookups with Reverse Whois and analyzes and works with security incidents.

</td></tr><tr><td>

Obtain an API key.

</td><td>

Visit the WhoisXML API website for information on API keys and to create an account: [WhoisXML API website](https://www.whoisxmlapi.com/reverse-whois-api.php). The configuration requires that you enter the API keys.

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
</table>Role required: admin

## Procedure

1.  If you have already installed and configured the Reverse Whois application, follow these steps:

    1.  Delete the existing configuration.

    2.  Install and create a new configuration using the API key that you have obtained.

2.  If you have not installed the application for the integration, see [Install a Security Operations integration](../../security-incident-response/task/install-non-core-apps.md) and follow the steps to install it.

3.  After the installation completes, navigate to **Integrations** &gt; **Integrations Configurations** and locate the Reverse Whois API tile.

4.  Click **Configure**.

    ![A description of the app and the button used to initiate the configuration.](../images/reverse-whois-config-tile.png)

5.  In the **Reverse Whois API Configuration** dialog box, enter the API key you obtained from the Whois XML API website.

6.  Choose one option in the following table to filter domain lookups for your search terms.

    |Description|Setting|
    |-----------|-------|
    |**Your search includes all domains, active and expired, that were registered after the Since date for the search terms you enter.This is the recommended setting.

**|**Since date**: Date entered in yyyy-mm-dd format. For example, `1991-06-01` for June 1, 1991.|
    |**Your search includes all active domains for the search terms you enter.**|**Since date**: Field cleared.|

    These configuration settings remain saved until you change them and apply to all Reverse Whois API searches.

    ![Reverse Whois API Configuration completed configuration.](../images/reverse-config-9-4.png)

7.  Click **Submit**.

    Configuration is successfully completed unless an error message is displayed.


If an error message is displayed, the API key may be invalid.

![Configuration error message example.](../images/reverse-whois-config-error.png "Error message")

**Parent Topic:**[Reverse Whois integration](../concept/reversewhois-lookups.md)

**Previous topic:**[Reverse Whois integration](../concept/reversewhois-lookups.md)

**Next topic:**[\(Optional\) Install and configure Whois](whois-install-and-config.md)

