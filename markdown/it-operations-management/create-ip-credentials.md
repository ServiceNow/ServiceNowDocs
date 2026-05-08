---
title: Create IP credentials
description: Create IP credentials for Discovery to securely connect to devices in your environment. Discovery uses these credentials to log in to devices and retrieve configuration data during the discovery process.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-04-28"
reading_time_minutes: 3
keywords: [ITOM, user roles, Now Assist]
breadcrumb: [ITOM Configuration Console for Discovery, Now Assist for Setup \(ITOM Visibility\), Now Assist for Setup \(ITOM\), IT Operations Management]
---

# Create IP credentials

Create IP credentials for Discovery to securely connect to devices in your environment. Discovery uses these credentials to log in to devices and retrieve configuration data during the discovery process.

## Before you begin

Verify the following:

-   You have installed the ITOM Visibility plugin. For more information, see [Install ITOM Visibility using Now Assist for Setup](install-nowassist-setup-itom-visibility.md).
-   You have installed the Now Assist for IT Operations Management plugin. For more information, see [Install Now Assist for IT Operations Management](install-now-assist-itom.md).
-   You're on the Configure IT Operations Management page of the Configuration Console. For more information, see [Access the ITOM Configuration Console](access-itom-config-console-disco.md).

Role required: discovery\_admin

## About this task

IP credentials store the authentication information that Discovery needs to access devices in your network. When Discovery runs, it tries each credential in the order you specify until it finds one that works for a given device. Set the credential order to control which credentials Discovery tries first. This is especially important when security policies lock out users after failed login attempts.

For more information about credential types and requirements, see Create and test your credentials.

## Procedure

1.  Navigate to **Configuration Summary** &gt; **Discovery** &gt; **Discovery Setup**.

2.  Select **IP credentials**.

3.  From the **Credential type** drop-down list, select a credential type.

    The following credential types are available for IP credentials.

    |Credential type|Description|
    |---------------|-----------|
    |Applicative Credentials|Credentials for discovering applications running on host machines.|
    |Basic Auth Credentials|Credentials that use basic authentication with a user name and password.|
    |CIM Credentials|Credentials for devices that use the Common Information Model protocol.|
    |Kubernetes Credentials|Credentials for discovering Kubernetes clusters and resources.|
    |oVirt Credentials|Credentials for oVirt virtualization environments.|
    |Secondary Bot Hash Token Credential|Token credentials for secondary bot integrations that use existing tokens.|
    |Secondary Bot Static Token Credential|Static token credentials for secondary bot integrations.|
    |SNP Community Credentials \(Password Only\)|Credentials that use an SNMP community string for network devices.|
    |SNMPv3 Credentials|Credentials that use the SNMPv3 protocol with authentication and privacy options.|
    |SSH Credentials|Credentials for Linux, UNIX, and other SSH-enabled devices.|
    |SSH Private Key Credentials|Credentials that use an SSH private key for authentication instead of a password.|
    |SSL Keystore Credentials|Credentials that use an SSL keystore for secure communication.|
    |VMWare Credentials|Credentials for VMware vCenter environments.|
    |Windows Credentials|Credentials for Windows devices that use WMI or WinRM protocols.|

4.  Select **Create new**.

5.  Complete the form.

    The fields in the form vary based on the credential type that you selected. The following fields appear in most credential types.

<table id="table_lxx_t5x_bjc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a unique and descriptive name for the credential.

</td></tr><tr><td>

User name

</td><td>

Enter the user name for this credential. Avoid leading or trailing spaces in user names.

</td></tr><tr><td>

Active

</td><td>

Select this check box to make the credential available for Discovery.

</td></tr><tr><td>

Credential alias

</td><td>

Select a credential alias to associate with this credential. Credential aliases enable you to define a credential once and reference it across multiple configurations.

</td></tr><tr><td>

Order

</td><td>

Enter the sequence in which Discovery tries this credential when it attempts to log in to devices. The smaller the number, the higher the priority. If all credentials have the same order number, Discovery tries them in a random order.**Note:** Establish credential order when you use large numbers of credentials or when security policies lock out users after failed login attempts.

</td></tr></tbody>
</table>6.  Select **Submit**.

    You're returned to the IP credentials page.

7.  To complete the setup, select **Mark as configured**.


**Related topics**  


[bundle-psec.credentials-getting-started]

