---
title: Activate External Key Management Service
description: Install the External Key Management Service \(EKMS\) plugin and configure user permissions to enable external key management functionality.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring External Key Management Service, External Key Management Service, Field Encryption, Encryption]
---

# Activate External Key Management Service

Install the External Key Management Service \(EKMS\) plugin and configure user permissions to enable external key management functionality.

## Before you begin

Roles required: admin, security\_admin, and sn\_kmf.cryptographic\_manager

Dependencies:

The following plugins need to be already installed on your environment:

-   Key Management Framework Scoped App
-   Field Encryption Enterprise

## About this task

Activating EKMS installs the necessary components to encrypt ServiceNow data with external keys managed in AWS Key Management Service.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Plugins**.

2.  Under Search your licensed applications and plugins, search for `Platform Encryption External Key Management`.

    The search should reveal the plugin. If you purchase a subscription for External Key Management Service through either Platform Encryption or ServiceNow Vault, you can also see this plugin available.

    **Important:** To activate the External Key Management Service, you must first purchase a subscription to either Platform Encryption or ServiceNow Vault and ensure the dependent plugin is installed: Key Management Framework Scoped App.

3.  Select **Install**

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the global domain. Otherwise, the following error appears: Application installation is unavailable because another operation is running: Plugin Activation for &lt;plugin name&gt;.


## Result

The EKMS plugin is now installed and activated. You can proceed to configure your external key integration.

## What to do next

Next steps:

-   Set up AWS Key Management Service access within AWS \(the process for this is out of scope of the ServiceNow documentation\)
-   Configure the EKMS key definition in ServiceNow

**Parent Topic:**[Configuring External Key Management Service](../concept/ekms-configuring-external-key-management.md)

**Related topics**  


[External Key Management Service](../concept/ekms-external-key-management.md)

[Configure an external key definition](ekms-configure-external-key-definition.md)

