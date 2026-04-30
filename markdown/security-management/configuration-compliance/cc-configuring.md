---
title: Setting up, installing, and configuring the Configuration Compliance application
description: Before you run the application in your ServiceNow AI Platform instance, you must first download and install the Configuration Compliance application from the ServiceNow Store. This application is available as a separate subscription.
locale: en-US
release: xanadu
product: Configuration Compliance
classification: configuration-compliance
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
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

-   **[Install Configuration Compliance](../task/install-and-configure-cc.md)**  
Before you run Configuration Compliance in your ServiceNow AI Platform® instance, you must first download and install the Configuration Compliance application from the ServiceNow Store. This application is available as a separate subscription.
-   **[Components installed with Configuration Compliance](../reference/installed-with-config-compliance.md)**  
Several types of components are installed with activation of the Configuration Compliance plugin, including tables and user roles.
-   **[Create or edit Configuration Compliance assignment rules](../task/create-cc-assign-rules.md)**  
Create rules to automatically assign test results based on filter conditions. These rules assign test results as they are imported.
-   **[Configuration Compliance remediation target rules](cc-remed-target-rules.md)**  
With remediation target rules, you can set the expected time frames for remediating test results. You can send notifications to users and groups when target dates are approaching and when they are past due.
-   **[Configuration Compliance calculator groups](vuln-config-compl-calc-groups.md)**  
Configuration Compliance calculators are used to update record values when pre-defined conditions are met. The calculators are grouped based on the criteria used to determine how the records are updated.
-   **[Create a Configuration Compliance calculator group](../task/create-confi-compl-calc-group.md)**  
Configuration Compliance calculator groups are used to group calculators based on how you want to use them.
-   **[Create or edit Configuration Compliance remediation task rules](../task/create-cc-group-rules.md)**  
You can create rules to automatically group test results based on filter conditions. These rules automatically group test results as they are imported. Use the filter to limit the test results grouped by this rule, such as selecting all test results with exploits.
-   **[Specify the duration of an exception requested for a remediation task](../task/cc-ex-mgmt-sys-prop.md)**  
Use system properties to limit the duration for which an exception is requested for a remediation task. Remediation of the remediation task is deferred for the specified period.
-   **[Configure Exception Management for Configuration Compliance](../task/configure-exception-management-configuration-compliance.md)**  
Limit the duration of an exception requested and add a questionnaire to the exception using the Configuration Compliance module. By default, an exception is requested using the ServiceNow® Vulnerability Response module. You can also request an exception using the GRC: Policy and Compliance Management integration.
-   **[Add an exception approver for Configuration Compliance](../task/cc-ex-request-add-approver.md)**  
Add users to the approver groups so that you can request an exception for a remediation task in Configuration Compliance.
-   **[Create a Configuration Compliance criticality map](../task/create-criticality-map.md)**  
Configuration Compliance criticality mapping provides a transform map for third-party source criticality fields to recognizable fields in Configuration Compliance severity.
-   **[Create email notifications](../task/cc-create-email-notification.md)**  
Vulnerability administrators can edit the notification or add new ones, specifying when to send the notification, who receives the notification, and what content is in the notification.
-   **[Configure approval rules for Exception Management in Configuration Compliance](../task/cc-exception-mgt-approval-rules.md)**  
Use the flow designer to approve exception requests for exception management and exception rules. If you are deploying Configuration Compliance for the first time, the flow designer is activated by default.

**Parent Topic:**[Configuration Compliance](../reference/vr-config-compliance-landing.md)

