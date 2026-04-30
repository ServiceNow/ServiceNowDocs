---
title: Install and configure Hybrid Analysis
description: Before you run the integration on your instance, complete the installation and configuration steps so the Hybrid Analysis application properly integrates with ServiceNow AI Platform Security Operations.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Hybrid Analysis integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Install and configure Hybrid Analysis

Before you run the integration on your instance, complete the installation and configuration steps so the Hybrid Analysis application properly integrates with ServiceNow AI Platform Security Operations.

## Before you begin

Complete the following setup checklist prior to installation. These setup tasks are required for a smooth installation and configuration.

<table id="table_xxz_jyj_4cb"><thead><tr><th>

Setup task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Verify that you have assigned the required ServiceNow AI Platform and Security Incident Response roles.

</td><td>

The following roles are required for installation, configuration, and verification of expected results:-   The administrator \(admin\) installs the app and assigns the Security Incident Administrator \(sn\_si.admin\) role.
-   The Security Incident Administrator \(sn\_si.admin\) oversees the configuration and verifies the expected results. This role also has access to the Security Operations module and assigns the sn\_si.analyst role.

</td></tr><tr><td>

Obtain an API key.

</td><td>

Visit the Hybrid Analysis website for information on API keys and to create an account: [Hybrid Analysis website](https://www.hybrid-analysis.com/). The configuration requires that you enter the API keys.

</td></tr><tr><td>

Verify that the ServiceNow core applications that are required to support the integration are installed and activated before you install the application for the integration.

</td><td>

For the Madrid release and later family releases, the com.snc.si\_dep plugin is required. This plugin automatically installs all the dependencies that are required to support the Security Incident Response product. Install and activate this plugin before installing and activating the other Security Operations applications.

 The following Security Operations applications must be installed and activated from the ServiceNow Store. Install and then activate one application at a time in the order listed below to ensure a smooth installation:

1.  Security Integration Framework
2.  Security Support Common
3.  Security Support Orchestration
4.  Security Incident Response

 For more information on setting up your ServiceNow AI Platform instance for the integration, see [Get entitlement for a Security Operations product or application](../../security-incident-response/task/entitle-secops-product.md) and [Activate a ServiceNow Store application](../../security-incident-response/task/activate-entitled-store-app.md).

</td></tr></tbody>
</table>Role required: admin

## About this task

Perform the following steps to update system properties and install and configure the integration.

## Procedure

1.  In the navigation filter, enter `sys_properties.list` and press **Enter**.

    The **System Properties** list is displayed.

2.  Click **New**.

    A new record is displayed.

3.  Fill in the fields, or select the values listed in the following table and click **Submit**.

    |Field name|Value|
    |----------|-----|
    |**Name**|`glide.outbound.tls_sni.enabled`|
    |**Type**|Select **true l false**|
    |**Value**|`true`|

    ![Attributes for the system property required for this integration.](../image/hybrid-analysis-system-property.png)

4.  If you have not installed the application for the integration, see [Install a Security Operations integration](../../security-incident-response/task/install-non-core-apps.md) and follow the steps to install it.

5.  After the installation completes, navigate to **Integrations** &gt; **Integrations Configurations** and locate the Hybrid Analysis tile.

6.  Click **Configure**.

    ![A description of the app and the button used to initiate the configuration.](../image/hybrid-analysis-configure-tile.png)

7.  In the **Hybrid Analysis Configuration** dialog box, enter the API key you obtained from the Hybrid Analysis website and click **Submit**.

    ![The configuration fields populated with encrypted account information.](../image/hybrid-analysis-api-key-new.png)

8.  Verify successful configuration.

    Configuration is successfully completed unless an error message is displayed.

    If an error message is displayed during the configuration, the Hybrid Analysis API key may be invalid.


**Parent Topic:**[Hybrid Analysis integration](../concept/hybrid-analysis-lookups.md)

**Previous topic:**[Hybrid Analysis integration](../concept/hybrid-analysis-lookups.md)

**Next topic:**[Verify expected results for Hybrid Analysis](verify-expected-results-hybrid-analysis-.md)

