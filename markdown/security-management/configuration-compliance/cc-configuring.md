---
title: Setting up, installing, and configuring the Configuration Compliance application
description: Before you run the application in your ServiceNow AI Platform instance, you must first download and install the Configuration Compliance application from the ServiceNow Store. This application is available as a separate subscription.
locale: en-US
release: zurich
product: Configuration Compliance
classification: configuration-compliance
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Setting up, installing, and configuring the Configuration Compliance application

Before you run the application in your ServiceNow AI Platform® instance, you must first download and install the Configuration Compliance application from the ServiceNow® Store. This application is available as a separate subscription.

Complete the following setup checklist steps listed in the following table prior to installation. These setup tasks are required for a smooth installation and configuration.

For more information about released versions of the Configuration Compliance application, as well as third-party and ServiceNow applications that are compatible with it, see the [Vulnerability Response Compatibility Matrix and Release Schema Changes \[KB0856498\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0856498) article in the HI Knowledge Base.

For more information about getting entitlements for store apps, see [Security Operations and the ServiceNow Store](../../planning-and-policy/concept/secops-and-store.md).

<table id="table_wyt_b3p_v5b"><thead><tr><th>

Setup tasks

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Verify that you have the required ServiceNow roles for your instance.

</td><td>

The following roles are required for installation, configuration, and verification of expected results:-   If not already assigned, the System Administrator \[admin\] installs the application and assigns the Configuration Compliance Admin \[sn\_vulc.admin\] role.
-   The Configuration Compliance Admin \[sn\_vulc.admin\] oversees configuration and verifies expected results.
-   The Remediation Owner \[sn\_vulc.remediation\_owner\] reads and updates assigned records. The sn\_vulc.remediation\_owner role is also automatically assigned when any user is assigned the itil role.

</td></tr><tr><td>

Supported integrations

</td><td>

Before you can use Configuration Compliance to remediate configuration items, you must install a third-party scanner integration and perform at least one network scan.

 Verify that the Vulnerability Response application is installed and activated prior to configuring supported third-party integrations. See [Install Vulnerability Response](../../vulnerability-response/task/install-and-configure-vr.md).

 To verify that integration applications are installed and activated, navigate to **Subscription Management** &gt; **Subscriptions** in your instance. The list displays the subscriptions your organization has purchased.

 For more information about third-party integrations and a list of supported products, see [Configuration Compliance integrations](vuln-config-compl-integrations.md).

</td></tr></tbody>
</table>Qualys Vulnerability Integration

-   If the Qualys Vulnerability Integration is already installed on your system, and your API credentials are different than the ones you want to use for Configuration Compliance, go into Setup Assistant \(in Vulnerability Response\) and assign them to each **Qualys PC** integration.
-   Navigate to **Qualys Vulnerability Integration** &gt; **Primary Integrations** and edit the **Qualys API Credentials** field under the **Qualys REST Details** tab.

For more detailed information on the Qualys Vulnerability Integration, see [Understanding the Qualys Vulnerability Integration](../../secops-integration-vr/qualys/concept/c_QualysVulnIntegration.md).

You are now ready to install the Configuration Compliance application. See [Install Configuration Compliance](../task/install-and-configure-cc.md).

