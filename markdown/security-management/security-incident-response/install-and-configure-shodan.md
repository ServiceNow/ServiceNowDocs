---
title: Install and configure Shodan
description: Before you run the integration on your instance, complete the installation and configuration steps so the Shodan application properly integrates with ServiceNow AI Platform Security Operations.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Shodan integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Install and configure Shodan

Before you run the integration on your instance, complete the installation and configuration steps so the Shodan application properly integrates with ServiceNow AI Platform Security Operations.

## Before you begin

Complete the following setup checklist prior to installation. These setup tasks are required for a smooth installation and configuration.

<table id="table_rv4_tpl_mcb"><thead><tr><th>

Setup tasks

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Verify that you have assigned the required ServiceNow AI Platform roles for your instance.

</td><td>

The following roles are required for installation, configuration, and verification of expected results:-   The System Administrator \(admin\) installs the app and assigns the Security Incident Administrator \(sn\_si.admin\) role.
-   The Security Incident Administrator \(sn\_si.admin\) oversees the configuration and verifies the expected results. This role also has access to the Security Operations module.

</td></tr><tr><td>

Obtain the Shodan API key.

</td><td>

Create an account and obtain the API key from the Shodan website: [Shodan website](https://developer.shodan.io/api/requirements).

</td></tr><tr><td>

Verify that the ServiceNow core applications that are required to support the integration are installed and activated before you install the application for the integration.

</td><td>

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

1.  If you have not installed the application for the integration, see [Install a Security Operations integration](../../security-incident-response/task/install-non-core-apps.md) and follow the steps to install it.

2.  After the installation completes, navigate to **Integrations** &gt; **Integrations Configurations** and locate the Shodan tile.

    ![The tile with a description of the app and the button used to initiate the configuration.](../image/shodan-configure.png)

3.  Click **Configure**.

4.  In the **Shodan Configuration** dialog box, enter the API key you obtained from the Shodan website and click **Submit**.

    ![This field is populated with encrypted account information.](../image/shodan-api.png)

5.  Verify successful configuration.

    Configuration is successfully completed unless an error message is displayed.

    If an error message is displayed during the configuration, the Shodan API key may be invalid.


**Parent Topic:**[Shodan integration](../concept/shodan-lookups.md)

**Previous topic:**[Shodan integration](../concept/shodan-lookups.md)

**Next topic:**[Verify expected results for Shodan](shodan-verify-expected-results.md)

