---
title: Configure the CyberArk credential identifier
description: Create the unique key that CyberArk can use to identify specific credentials in the external repository.
locale: en-US
release: australia
product: Connections and Credentials
classification: connections-and-credentials
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [CyberArk integration configuration, CyberArk credential storage integration, External credential storage, Get started with credentials, Connections and Credentials, Access Management]
---

# Configure the CyberArk credential identifier

Create the unique key that CyberArk can use to identify specific credentials in the external repository.

## Before you begin

Role required: admin

Before starting this procedure, ensure that the External Credential Storage plugin is activated, and the [com.snc.use\_external\_credentials](../concept/c_CyberArkCredStorageIntegrate.md) system property is set to true.

## Procedure

1.  Navigate to **All** &gt; **Discovery** &gt; **Credentials** or **Orchestration** &gt; **Credentials**.

2.  Click **New**.

3.  From the list of credential types, select a type that [supports CyberArk](../concept/c_CyberArkCredStorageIntegrate.md) external storage.

4.  Complete the form using the fields from your [credential type](t_CreateCredential.md).

5.  Select the **External credential store** check box.

    The **User name** and **Password** fields are replaced with the **Credential ID** field.

    **Note:** If the check box is not visible, click the menu icon in the header bar and select **View** &gt; **External Storage**.

6.  In the **Credential ID** field, enter an expression using one of these formats:

    -   If all your credentials are in the same safe, configure this safe name in the MID Server `config.xml` file using the [ext.cred.safe\_name](t_ConfigureTheMIDServerForCyberArk.md) parameter, and then specify the credential ID by name only, as **&lt;credential ID&gt;**.
    -   To name credentials for a given platform that reside is a specific safe, define the credential ID as **&lt;safe&gt;:&lt;credential ID&gt;:&lt;platform ID&gt;**.
    -   If your credentials are in multiple safes, specify the credential ID in this format: **&lt;safe&gt;:&lt;credential ID&gt;**.
    -   If you want CyberArk to look up the credential by IP address, using an alternate safe, specify the credential ID in this format: **&lt;safe&gt;:**.
    -   If you want CyberArk to look up the credential for an alternate platform ID in the same safe, use this format: **::&lt;platform ID&gt;**
    -   If you want CyberArk to look up the credential in a configured safe by the IP address rather than the credential ID, leave this field blank. This is the best practice for handling installations in which each server has a unique credential. Without this type of lookup, you must create a credential ID record in your instance for every server in your environment.
    **Note:** The credential ID must match the value in the **Name** field for the CyberArk account. The **Credential ID** field has a limit of 180 characters.

7.  If you are storing SNMPv3 credentials in CyberArk and are using the privacy protocol and privacy key, configure the ID as follows:

    1.  In the **Credential Store Type** field, select **CyberArk**.

        The **Privacy Credential ID** field appears.

    2.  Enter the **Name** of the CyberArk SNMPv3 privacy account in the **Privacy Credential ID** field.

8.  Click **Submit**.


**Parent Topic:**[CyberArk integration configuration](../concept/c_CyberArkIntegrationConfiguration.md)

