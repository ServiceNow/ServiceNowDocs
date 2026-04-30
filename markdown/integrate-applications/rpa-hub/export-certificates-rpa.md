---
title: Exporting Microsoft Active Directory certificates
description: You can export Microsoft Active Directory certificates, such as root, intermediate, and a client authentication certificate, for authentication purposes. You then register the exported root and intermediate certificate in the ServiceNow instance and map the exported client authentication certificate to the user.Export an active directory \(AD\) root certificate in your Windows machine to register the exported certificate on the ServiceNow instance.Export an active directory \(AD\) intermediate certificate in your Windows machine to register the exported certificate on the ServiceNow instance.Export an active directory \(AD\) client authentication certificate in your Windows machine to map the exported certificate to the user on the ServiceNow instance.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Obtaining client authentication and code signing certificates, Configuring RPA Hub, RPA Hub, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Exporting Microsoft Active Directory certificates

You can export Microsoft Active Directory certificates, such as root, intermediate, and a client authentication certificate, for authentication purposes. You then register the exported root and intermediate certificate in the ServiceNow instance and map the exported client authentication certificate to the user.

You must do these tasks in your Windows machine.

If you don't have the user-generated certificates \(client authentication and code signing\), do the tasks in the following topics to export active directory certifications. For more information, see [Generating and installing user certificates](use-user-certificates-rpa.md#).

**Parent Topic:**[Obtaining client authentication and code signing certificates](code-signing-certificate-rpa.md)

## Export a root certificate

Export an active directory \(AD\) root certificate in your Windows machine to register the exported certificate on the ServiceNow instance.

### Before you begin

Do this task in your Windows machine.

Role required: admin

### Procedure

1.  In your Windows machine, from the Search menu, enter `Manage computer certificates`.

2.  To export the root certificate, do the following actions:

    1.  In the Certificate Manager tool, navigate to **Certificates - Local Computer** &gt; **Personal** &gt; **Certificates**.

    2.  Double-click the required client authentication-based certificate.

    3.  On the **Certification Path** tab, double-click the root certificate.

    4.  On the **Details** tab, verify the serial number and select **OK**.

    5.  Navigate to **Certificates - Local Computer** &gt; **Trusted Root Certification Authorities** &gt; **Certificates**.

    6.  To match the root certificate with the serial number, double-click a root certificate.

    7.  On the **Details** tab, verify that the serial number matches and select **OK**.

        Repeat this step until you find a match.

    8.  After you identify the root certificate, right-click the root certificate, select **All Tasks**, and then select **Export...**.

    9.  In the Welcome to the Certificate Export Wizard dialog box, select **Next**.

    10. In the Export File Format dialog box, select the **Base-64 encoded X.509 \(.CER\)** file format, and then select **Next**.

    11. In the File to Export dialog box, select the file name location in the **File name** field or select **Browse** to save the certificate file, and then select **Next**.

    12. In the Completing to the Certificate Export Wizard dialog box, select **Finish**.

    13. After the export is complete, in the Certificate Export Wizard dialog box, select **OK**.

3.  To rename the file extension of the exported root certificate, do the following actions:

    1.  Locate the exported certificate file.

    2.  Right-click the certificate file and select **Rename**.

    3.  In the file name, rename the file extension from **.cer** to **.pem**.

        For example, change the Root CA.cer file name to `Root CA.pem`.

    4.  In the confirmation dialog box, select **Yes**.


### What to do next

Register the root certificate to make it available for authentication. For more information, see [Register the CA certificate](https://www.servicenow.com/docs/access?context=set-up-mutual-auth&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

## Export an intermediate certificate

Export an active directory \(AD\) intermediate certificate in your Windows machine to register the exported certificate on the ServiceNow instance.

### Before you begin

Do this task in your Windows machine.

Role required: admin

### About this task

If your organization doesn't require an intermediate certificate, skip this task.

### Procedure

1.  In your Windows machine, from the Search menu, enter `Manage computer certificates`.

2.  To export the intermediate certificate based on your business requirement, do the following actions:

    1.  In the Certificate Manager tool, navigate to **Certificates - Local Computer** &gt; **Personal** &gt; **Certificates**.

    2.  Double-click the required client authentication-based certificate.

    3.  On the **Certification Path** tab, double-click the intermediate certificate.

    4.  On the **Details** tab, verify the serial number and select **OK**.

    5.  Navigate to **Certificates - Local Computer** &gt; **Intermediate Certification Authorities** &gt; **Certificates**.

    6.  To match the intermediate certificate with the serial number, double-click an intermediate certificate.

    7.  On the **Details** tab, verify that the serial number matches and select **OK**.

        Repeat this step until you find a match.

    8.  After you identify the intermediate certificate, right-click the intermediate certificate, select **All Tasks**, and then select **Export...**.

    9.  In the Welcome to the Certificate Export Wizard dialog box, select **Next**.

    10. In the Export File Format dialog box, select the **Base-64 encoded X.509 \(.CER\)** file format, and select **Next**.

    11. In the File to Export dialog box, select the file name location in the **File name** field or click **Browse** to save the certificate file, and then select **Next**.

    12. In the Completing to the Certificate Export Wizard dialog box, select **Finish**.

    13. After the export is complete, in the Certificate Export Wizard dialog box, select **OK**.

3.  To rename the file extension of the exported intermediate certificate, do the following actions:

    1.  Locate the exported certificate file.

    2.  Right-click the certificate file and select **Rename**.

    3.  In the file name, rename the file extension from **.cer** to **.pem**.

        For example, change the Intermediate CA.cer file name to `Intermediate CA.pem`.

    4.  In the confirmation dialog box, select **Yes**.


### What to do next

Register the intermediate certificate to make it available for authentication. For more information, see [Register the CA certificate](https://www.servicenow.com/docs/access?context=set-up-mutual-auth&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

## Export a client authentication \(active directory\) certificate

Export an active directory \(AD\) client authentication certificate in your Windows machine to map the exported certificate to the user on the ServiceNow instance.

### Before you begin

Do this task in your Windows machine.

Role required: admin

### Procedure

1.  In your Windows machine, from the Search menu, enter `Manage computer certificates`.

2.  To export the client authentication certificate, do the following actions:

    1.  In the Certificate Manager tool, navigate to **Certificates - Local Computer** &gt; **Personal** &gt; **Certificates**.

    2.  Right-click the client authentication certificate, select **All Tasks**, and then select **Export...**.

    3.  In the Welcome to the Certificate Export Wizard dialog box, select **Next**.

    4.  In the Export File Format dialog box, select the **Base-64 encoded X.509 \(.CER\)** file format, and then select **Next**.

    5.  In the File to Export dialog box, select the file name location in the **File name** field or select **Browse** to save the certificate file, and then select **Next**.

    6.  In the Completing to the Certificate Export Wizard dialog box, select **Finish**.

    7.  After the export is complete, in the Certificate Export Wizard dialog box, select **OK**.

3.  To rename the file extension of the exported client authentication certificate, do the following actions:

    1.  Locate the exported certificate file.

    2.  Right-click the certificate file and select **Rename**.

    3.  In the file name, rename the file extension from **.cer** to **.pem**.

        For example, change the User CA.cer file name to `User CA.pem`.

    4.  In the confirmation dialog box, select **Yes**.


### What to do next

Map the PEM certificate to the user. For more information, see [Map the PEM certificate to user](https://www.servicenow.com/docs/access?context=set-up-mutual-auth&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

