---
title: SNMP support for Discovery
description: Discovery supports SNMP versions 1, 2c, and 3. If you have an active SNMP v3 credential, valid options for SNMP version are v3 or All. If you have an active SNMP v1 or v2 credential \(community string\), valid options for SNMP version are v1, v2c, or All. Default is All.Set up your credentials so Discovery can access SNMPv3 targets.You must also set the SNMP version after choosing the appropriate credential.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# SNMP support for Discovery

Discovery supports SNMP versions 1, 2c, and 3. If you have an active SNMP v3 credential, valid options for SNMP version are v3 or All. If you have an active SNMP v1 or v2 credential \(community string\), valid options for SNMP version are v1, v2c, or All. Default is All.

MID Servers support all SNMP protocol versions by default. You can set a MID Server to support only specific versions of SNMP.

For SNMP credentials information, see [SNMP credentials](https://www.servicenow.com/docs/access?context=c_SNMPCredentials&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

SNMP probe parameters can be used while discovering an SNMP device. See [SNMP probe parameters](../reference/r_SNMPProbeParameters.md) for more information.

## Add an SNMPv3 user credential in Discovery

Set up your credentials so Discovery can access SNMPv3 targets.

### Before you begin

Role required: admin

### About this task

A MID Server parameter is also available to control SNMP versions. See [MID Server parameters](https://www.servicenow.com/docs/access?context=mid-server-parameters&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

### Procedure

1.  Navigate to **All** &gt; **Discovery** &gt; **Credentials**.

2.  Click **New**.

3.  Click **SNMPv3 Credentials**.

4.  Fill in the form, using the fields in the table.

    ![SNMPv3 credentials form](../image/SNMPv3UserCredentials.png "SNMPv3 credentials form")

<table id="table_zxd_wc1_djb"><thead><tr><th>

Field

</th><th>

Input value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique and descriptive name for this credential. For example, you might call it **SNMP Community Atlanta**.

</td></tr><tr><td>

Active

</td><td>

Enable or disable these credentials for use.

</td></tr><tr><td>

Applies to

</td><td>

Select whether to apply these credentials to **All MID servers** in your network, or to one or more **Specific MID servers**. Specify the MID Servers that should use these credentials in the **MID servers** field.

</td></tr><tr><td>

MID servers

</td><td>

Select one or more MID Servers from the list of available MID Servers. The credentials configured in this record are available to the MID Servers in this list. This field is available only when you select **Specific MID servers** from the **Applies to** field.

</td></tr><tr><td>

Order

</td><td>

Order \(sequence\) in which Discovery tries this credential as it attempts to log on to devices. The smaller the number, the higher in the list this credential appears. Establish credential order when using large numbers of credentials or when security locks out users after three failed login attempts. If all the credentials have the same order number \(or none\), the instance tries the credentials in a random order.

</td></tr><tr><td>

User name

</td><td>

Enter the SNMP user name. Avoid leading or trailing spaces in user names. A warning appears if the platform detects leading or trailing spaces in the user name.

</td></tr><tr><td>

Authentication protocol

</td><td>

Select the authentication type to use for this credential. The choices are: -   MD5
-   SHA-1
-   SHA-224
-   SHA-256
-   SHA-384
-   SHA-512


</td></tr><tr><td>

Authentication Key

</td><td>

Enter the authentication key to use for this credential.

</td></tr><tr><td>

Privacy protocol

</td><td>

Select the encryption protocol for this credential. The choices are:-   3DES
-   AES128
-   AES192
-   AES256
-   DES


</td></tr><tr><td>

Privacy key

</td><td>

Enter the key associated with the selected privacy protocol.

</td></tr><tr><td>

Credential ID

</td><td>

Enter the unique key configured for external credentials in the JAR file uploaded to the MID Server for an external credential provider. The **Credential ID** field has a limit of 40 characters.This field is only visible when the **External credential store** check box is selected.

</td></tr><tr><td>

Privacy Credential ID

</td><td>

Enter the privacy account key configured for SNMPv3 credentials in CyberArk. If you are using a privacy protocol in CyberArk, this field must have the same value as the **Name** field for the CyberArk SNMPv3 Privacy Account. This field is only visible for SNMPv3 when you select **CyberArk** from the **Credential Store Type** field. If you are not using a privacy key for CyberArk, leave this field empty.

</td></tr><tr><td>

Credential alias

</td><td>

Allow workflow creators to assign individual credentials to any activity in an Orchestration workflow or assign different credentials to each occurrence of the same activity type in an Orchestration workflow.

</td></tr><tr><td>

External credential store

</td><td>

Select this check box to use an external credential storage system. When external storage is enabled, the **Credential ID** field appears. External credential storage is only available when the [External Credential Storage plugin](https://www.servicenow.com/docs/access?context=t_ActivateExtrnlCredStoragePlugIn&version=zurich&pubname=zurich-platform-security&ft:locale=en-US) is activated and the **External Storage** view is selected.

</td></tr><tr><td>

Credential Store Type

</td><td>

Select the external storage provider. Select **CyberArk** only if you are using a CyberArk SNMPv3 privacy key. The **Privacy Credential ID** field appears to allow entry of the key.

</td></tr><tr><td>

Use Context

</td><td>

Select this check box to add a context value for this credential. This field is visible in the **Discovery** view. Contexts are not currently supported for external credential storage.**Note:** A context is a collection of management information accessed by an SNMPv3 credential that references a specific OID. Contexts are sometimes referenced to collect information about the device that cannot be accessed by the normal credential. A context can be provided by the manufacturer or configured separately. If you have multiple SNMPv3 credentials with the same user name and keys, but some of your devices need a context and some do not, then you will need to create separate records for each device.

</td></tr><tr><td>

Context Name

</td><td>

Enter the context name value for this credential. This should only be used if you have devices that require this value for full access. This field is visible when the **Use Context** check box is selected.

</td></tr></tbody>
</table><table id="table_cd3_xx5_1r"><thead><tr><th>

Option

</th><th>

Fields to configure

</th></tr></thead><tbody><tr><td>

**noAuthNoPriv security**

</td><td>

-   **Authentication protocol:** None
-   **Privacy protocol:** None
-   **Authentication Key:** Leave blank
-   **Privacy Key:** Leave blank


</td></tr><tr><td>

**authNoPriv security**

</td><td>

-   **Authentication protocol:** Set
-   **Privacy protocol:** Leave blank
-   **Authentication Key:** Set
-   **Privacy Key:** Leave blank


</td></tr><tr><td>

**authPriv**

</td><td>

-   **Authentication protocol:** Set
-   **Privacy protocol:** Set
-   **Authentication Key:** Set
-   **Privacy Key:** Set


</td></tr></tbody>
</table>
## Set SNMP version on the Discovery schedule

You must also set the SNMP version after choosing the appropriate credential.

### Before you begin

Role required: admin

### About this task

A MID Server parameter is also available to control SNMP versions. See [MID Server parameters](https://www.servicenow.com/docs/access?context=mid-server-parameters&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

### Procedure

1.  Navigate to **All** &gt; **Discovery** &gt; **Discovery schedules**&gt; *your Discovery schedule.*

2.  In the **Use SNMP Version** field, select the appropriate version.

    The default value is **ALL**. You can change this to **v1**,**v2c**, or **v3**.


