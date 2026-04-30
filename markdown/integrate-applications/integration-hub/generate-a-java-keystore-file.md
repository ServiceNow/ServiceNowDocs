---
title: Generate a Java KeyStore file
description: Convert the public certificate that you had generated to a Java KeyStore file on your machine because your ServiceNow instance supports a Java KeyStore file. After generating, you must upload the file to your ServiceNow instance.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Set up the Oracle HCM Cloud spoke, Oracle HCM Cloud Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Generate a Java KeyStore file

Convert the public certificate that you had generated to a Java KeyStore file on your machine because your ServiceNow instance supports a Java KeyStore file. After generating, you must upload the file to your ServiceNow instance.

## Before you begin

Role required: admin

## Procedure

1.  Open the command prompt on your machine.

2.  Use the `cd` command to change the directory to the location where you had generated the public certificate.

3.  On the command prompt, execute the command `openssl pkcs12 -export -in publickey.cer -inkey private.key -out <your-file-name>.p12 -name "<your-custom-name>”`.

4.  In the Enter Export Password prompt, create an export password.

5.  In the Verifying - Enter Export Password prompt, reenter the export password you had created.

    The P12 file is created.

6.  Copy the P12 file to the respective JDK/bin folder of your machine.

    **Note:** Depending on the OS of your machine, the location of the JDK/bin folder might vary.

7.  Copy the path to the JDK/bin folder.

8.  In the command prompt, use the `cd` command to change the current directory to the JDK/bin folder.

9.  To convert the P12 file to a Java KeyStore file, execute the command `keytool -importkeystore -srckeystore <P12-file-name>.p12 -srcstoretype pkcs12 -destkeystore <Java-KeyStore-filename>.jks`.

10. In the Enter destination keystore password prompt, create a password.

11. In the Re-enter new password prompt, reenter the destination keystore password you had created.

12. In the Enter source keystore password prompt, enter the same password that you had created to generate the P12 file.

    The Java KeyStore file is created in the JDK/bin location.


