---
title: Activate Column Level Encryption Enterprise
description: With subscription to Column Level Encryption Enterprise, an admin can activate the com.glide.now.platform.encryption plugin.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-10-22"
reading_time_minutes: 1
breadcrumb: [Configuring Column Level Encryption, Column Level Encryption, Encryption]
---

# Activate Column Level Encryption Enterprise

With subscription to Column Level Encryption Enterprise, an admin can activate the com.glide.now.platform.encryption plugin.

## Before you begin

Role required: admin

To purchase a subscription, contact your ServiceNow account manager. The account manager can arrange to have the plugin activated on your organization's production and non-production instances, generally within a few days.

## About this task

Activating the Column Level Encryption Enterprise plugin \(`com.glide.now.platform.encryption`\) makes the following changes to your instance:

-   The Encryption Support \(com.glide.encryption\) plugin is also activated.

    **Note:** The Key Management Framework \(com.glide.kmf.global\) plugin is already active by default.

-   The `glide_encryption.set_value_support_cle.disabled` property is set to **false**, which turns on the SetValue feature. The SetValue support enables both `setDisplayValue()` and `setValue()` APIs to support encrypted data. It also enables both `getDisplayValue()` and `getValue()` to return clear text values.
-   Two scheduled jobs are enabled:

    -   **autoKeyMigration**: Migrates encryption context keys to Key Management Framework \(KMF\) cryptographic module keys.
    -   **autoDataMigration**: Migrates data that you already encrypted to use the KMF cryptographic module key.
    Administrators can modify when these scheduled jobs run, and can pause or restart them at any time.


## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin, `Platform Encryption - com.glide.now.platform.encryption` using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install**, and then in the Activate Plugin dialog box, select **Activate**.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`


**Parent Topic:**[Configuring Column Level Encryption](../../encryption/concept/configuring-column-level-encryption.md)

