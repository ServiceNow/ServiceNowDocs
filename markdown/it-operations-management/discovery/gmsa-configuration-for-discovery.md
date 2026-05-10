---
title: gMSA configuration for Discovery
description: Group managed service accounts \(gMSAs\) are managed domain accounts that you use to help secure services. gMSAs can be used for credential-less Discovery.Use Group Managed Service Accounts \(gMSA\) to securely run MID Servers and perform Windows discovery without storing passwords locally. This configuration improves security and simplifies credential management by leveraging Active Directory for automatic password rotation and centralized control.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Advanced Discovery configuration, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# gMSA configuration for Discovery

Group managed service accounts \(gMSAs\) are managed domain accounts that you use to help secure services. gMSAs can be used for credential-less Discovery.

## Benefits

After you configure Discovery to use gMSA, password management for that account is handled by the Windows operating system. So, you can run Windows Discovery without sharing credentials with the ServiceNow instance. Benefits include the following:

-   You don’t have to handle gMSA passwords on your own.
-   You can choose the cycle of gMSA password rotation for better security.
-   You don't need to store the password on the ServiceNow instance.
-   The gMSA user doesn't need to be member of a domain admin group.
-   The gMSA user used as the MID Server service account doesn't need to be on the local admin group of the MID Server.

**Parent Topic:**[Advanced Discovery configuration](c_DiscoveryExtendedCapabilities.md)

## Configure gMSA for Discovery

Use Group Managed Service Accounts \(gMSA\) to securely run MID Servers and perform Windows discovery without storing passwords locally. This configuration improves security and simplifies credential management by leveraging Active Directory for automatic password rotation and centralized control.

### Before you begin

-   Verify that the gMSA account is created and configured in Active Directory.
-   Add the gMSA accounts to the MID Server host's local Administrator's group.
-   For target servers, add the gMSA account to their local Administrator's group.

Role required: agent\_admin, discovery\_admin, or admin

### Procedure

1.  On the PowerShell command line, create a KDS Root key on a Domain Controller using the following commands:

    ```
    Add-KdsRootKey -EffectiveImmediately
    ```

    or

    ```
    Add-KdsRootKey –EffectiveTime ((Get-Date).AddHours(-10))
    ```

2.  Set up your gMSA and security groups using the group managed services account information [https://docs.microsoft.com](https://docs.microsoft.com).

    **Note:** It's not usually necessary to add discovered Windows servers to the GMSAGroup. Member hosts obtain the current and previous password values directly from a domain controller, and Discovery doesn't require this step.

3.  Start the MID Server with the gMSA account following the directions here on using gMSA: [Install a MID Server on Windows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-server-install-prereqs.md)

4.  Create a Windows credential on the instance and select the check box **Use MID Server Service Account**.

5.  Launch a Discovery on the server hosting the MID Server and another computer.


