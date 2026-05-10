---
title: Setting up an IBM License Metric Tool \(ILMT\) or BigFix Inventory integration using HTTPS
description: You can set up an IBM License Metric Tool \(ILMT\) or BigFix Inventory integration for IBM compliance reporting.Set up IBM License Metric Tool \(ILMT\) and BigFix Inventory integration for IBM compliance reporting using an HTTPS connection with the MID Server.Set up IBM License Metric Tool \(ILMT\) and BigFix Inventory integration for IBM compliance reporting using an HTTPS connection without the MID Server.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [ILMT and BigFix Inventory integrations, Software Asset Management publisher pack for IBM, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Setting up an IBM License Metric Tool \(ILMT\) or BigFix Inventory integration using HTTPS

You can set up an IBM License Metric Tool \(ILMT\) or BigFix Inventory integration for IBM compliance reporting.

If you're using an HTTPS connection, you can use any of the following connection types:

-   HTTPS with the MID Server
-   HTTPS without the MID Server

**Parent Topic:**[IBM License Metric Tool \(ILMT\) and BigFix Inventory integrations](ibm-ilmt-bigfix-inventory-integration.md)

## HTTPS with the MID Server

Set up IBM License Metric Tool \(ILMT\) and BigFix Inventory integration for IBM compliance reporting using an HTTPS connection with the MID Server.

### Before you begin

Role required: sys\_admin

### Procedure

1.  Download the certificate by logging in to the ILMT or BigFix Inventory server and navigating to **Management** &gt; **Server Settings**.

2.  [Import a certificate for the MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/add-ssl-certificates.md).


### What to do next

After you've finished uploading your certificates, [create a connection to ILMT/BigFix Inventory](../task/set-up-ibm-platform.md).

## HTTPS without the MID Server

Set up IBM License Metric Tool \(ILMT\) and BigFix Inventory integration for IBM compliance reporting using an HTTPS connection without the MID Server.

### Before you begin

Role required: sys\_admin

### About this task

**Note:** The firewall port must be opened for connectivity to your ServiceNow instance IP address.

### Procedure

1.  Download the certificate by logging in to the ILMT or BigFix Inventory server and navigating to **Management** &gt; **Server Settings**.

2.  From your ServiceNow instance, navigate to **System Definition** &gt; **Certificates** and create a [certificate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/t_UploadACertificateToAnInstance.md) \(Trust Store Cert, PEM format\).

3.  Paste the full downloaded ILMT or BigFix Inventory server certificate content into the **PEM Certificate** field \(including banners\).

4.  Select the **Validate Stores/Certificates** related link.

5.  To create the Java Key Store file using the IBM certificate file, open the command prompt on your computer and navigate to the folder that contains the JRE keytool.

6.  Execute the following commands:

    ```
    keytool -import -trustcacerts -alias <Certificate alias> -file <Certificate file path> -keystore IBM_Server.keystore -storetype jks
    keytool -list -v -keystore IBM_Server.keystore
    ```

    These commands generate the `IBM_Server.keystore` file.

7.  Return to the ServiceNow AI Platform, navigate to **System Definition** &gt; **Certificates** and create a certificate \(Java Key Store\).

8.  Upload the `IBM_Server.keystore` file that you generated as an attachment to the certificate record.

9.  Select the **Validate Stores/Certificates** related link.

10. Navigate to **System Security** &gt; **Protocol Profiles** and create a new protocol profile using the Java Key Store certificate that you created.

    **Note:** You need to select the protocol profile that you create when you create a connection to ILMT/BigFix Inventory.


### What to do next

After you've finished uploading your certificates, [create a connection to ILMT/BigFix Inventory](../task/set-up-ibm-platform.md).

