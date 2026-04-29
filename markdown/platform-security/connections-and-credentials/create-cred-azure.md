---
title: Configure Azure credentials on a CyberArk vault
description: Configure your CyberArk vault with the Azure credentials to be retrieved for use by your instance.
locale: en-US
release: australia
product: Connections and Credentials
classification: connections-and-credentials
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [CyberArk integration configuration, CyberArk credential storage integration, External credential storage, Get started with credentials, Connections and Credentials, Access Management]
---

# Configure Azure credentials on a CyberArk vault

Configure your CyberArk vault with the Azure credentials to be retrieved for use by your instance.

## Before you begin

Role required: admin

## About this task

To store an Azure credential, first create an Azure credential template in the CyberArk vault. This process only needs to be completed once for the vault.

## Procedure

1.  Log in to CyberArk in Administration mode.

2.  Navigate to the **Administration** tab.

3.  In **System Configuration**, edit **Platform Management**.

4.  Navigate to **Cloud Provider Template** and duplicate it.

5.  Edit the template for Azure credentials.

6.  Add the following two properties:

    -   **Name** as **Username** and **Display Name** as **Client ID**

    -   **Name** as **Address** and **DisplayName** as **Tenant ID**

7.  Apply the changes.

8.  Navigate to the **Account** section and select **Add account**.

9.  Select **Safe**.

10. Set the **Device Type** to **Cloud Service**.

11. Select the Azure template that was previously edited.

12. Fill in the information in for the **Client ID**, **Tenant ID**, and **Password** fields.

13. Select **Save**.


**Parent Topic:**[CyberArk integration configuration](../../credentials/concept/c_CyberArkIntegrationConfiguration.md)

