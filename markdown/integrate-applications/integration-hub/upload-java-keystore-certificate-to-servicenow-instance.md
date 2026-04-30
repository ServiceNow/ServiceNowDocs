---
title: Upload Java KeyStore certificate to ServiceNow instance
description: Upload the Java KeyStore certificate to your ServiceNow instance to enable the creation of connections and credentials.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Set up the Oracle HCM Cloud spoke, Oracle HCM Cloud Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Upload Java KeyStore certificate to ServiceNow instance

Upload the Java KeyStore certificate to your ServiceNow instance to enable the creation of connections and credentials.

## Before you begin

Role required: admin

## Procedure

1.  On your ServiceNow instance, navigate to the X.509 certificate list by entering `sys_certificate.LIST` in the navigation filter.

2.  Select **New**.

3.  Fill the form.

    |Field|Description|
    |-----|-----------|
    |Name|Custom name of the certificate.|
    |Type|Type of certificate. Select Java Key Store.|
    |Notify on expiration|The role that should be notified when the certificate expires.|
    |Expires in days|The validity of the certificate.|
    |Warn in days to expire|The number of days before which the role receives a warning of expiry.|
    |Key store password|Key store password that you had created.|
    |Active|Indicates that the Java Key Store certificate is active.|
    |Short description|Short description of the record.|

4.  Right-click on the banner of the record and select **Save**.

    ![Save button.](../image/oracle-hcm-spoke-upload-jks-file.png)

5.  Select the **Manage Attachments** icon \(![Manage Attachments icon.](../image/manage-attachments-icon.png)\) to attach the Java KeyStore file.

    If your instance displays an error of the type "&lt;file-name&gt;.jks File type not permitted or mime type does not match the file content", complete the steps.

    1.  In the filter field of your instance, enter `sys_properties.LIST` and press **Enter**.

        ![Filter field.](../image/oracle-hcm-spoke-troubleshooting.png)

    2.  In the Name field of the System Properties page, enter `glide.security.file.mime_type.validation` and press **Enter**.

        ![Name field.](../image/oracle-hcm-spoke-system-property.png)

    3.  Select the system property glide.security.file.mime\_type.validation.
    4.  In the Value field, update the value to `False`.
    5.  Right-click on the banner of the form and select **Save**.
6.  Select **Save**.

7.  To validate the certificate, select the Validate Stores/Certificates link.

    You've uploaded the Java Key Store certificate to your ServiceNow instance.


