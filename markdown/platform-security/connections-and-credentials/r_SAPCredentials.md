---
title: SAP credentials
description: The SAP credential type manages access to SAP JCo systems. This credential type is available for Discovery and Orchestration.
locale: en-US
release: australia
product: Connections and Credentials
classification: connections-and-credentials
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create and test your credentials, Get started with credentials, Connections and Credentials, Access Management]
---

# SAP credentials

The SAP credential type manages access to SAP JCo systems. This credential type is available for Discovery and Orchestration.

These fields are available in the Credentials form for SAP type credentials.

<table id="table_bz5_lqv_2y"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a unique and descriptive name for this credential.

</td></tr><tr><td>

Active

</td><td>

Enable or disable these credentials for use.

</td></tr><tr><td>

User name

</td><td>

Enter the user name to create in the Credentials table. Avoid leading or trailing spaces in user names. A warning appears if the platform detects leading or trailing spaces in the user name. For CIM discovery, the user must have the admin role.

</td></tr><tr><td>

Password

</td><td>

Enter the password.

</td></tr><tr><td>

Credential ID

</td><td>

Enter the unique key configured for external credentials in the JAR file uploaded to the MID Server for an external credential system. The **Credential ID** field has a limit of 40 characters.This field is only visible when the **External credential store** check box is selected.

</td></tr><tr><td>

Credential alias

</td><td>

Allow workflow creators to assign individual credentials to any activity in an Orchestration workflow or assign different credentials to each occurrence of the same activity type in an Orchestration workflow.To use the credential for discovering CIs not belonging to this CI type using Service Mapping and Discovery patterns, enter the table name for the CI type to which the CI belongs, for example cmdb\_ci\_apache\_web\_server.

</td></tr><tr><td>

External credential store

</td><td>

Select this check box to use an external credential storage system. When you select this option the **User name** and **Password** fields are replaced with the **Credential ID** field. [External credential storage](../concept/c_ExternalCredentialStorage.md) is only available when the External Credential Storage plugin in activated. **Note:** Currently, the only supported external storage system is [CyberArk](../concept/c_CyberArkCredStorageIntegrate.md).

</td></tr><tr><td>

Applies to

</td><td>

Select whether to apply these credentials to **All MID servers** in your network, or to one or more **Specific MID servers**. Specify the MID Servers that should use these credentials in the **MID servers** field.

</td></tr><tr><td>

MID servers

</td><td>

Select one or more MID Servers from the list of available MID Servers. The credentials configured in this record are available to the MID Servers in this list. This field is available only when you select **Specific MID servers** from the **Applies to** field.**Note:** Selecting Specific **Specific MID servers** doesn’t affect mid server selection. It’s used only to decide which mid servers should have visibility to the credential. **Specific MID servers** isn’t supported in Orchestration activities.

</td></tr><tr><td>

Order

</td><td>

Order \(sequence\) in which Discovery tries this credential as it attempts to log on to devices. The smaller the number, the higher in the list this credential appears. Establish credential order when using large numbers of credentials or when security locks out users after three failed login attempts. If all the credentials have the same order number \(or none\), the instance tries the credentials in a random order.

</td></tr><tr><td>

Windows MID Server Service Account

</td><td>

When active, the defined credential represents the MID Server service account.

</td></tr></tbody>
</table>