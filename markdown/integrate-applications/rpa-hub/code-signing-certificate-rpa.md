---
title: Obtaining client authentication and code signing certificates for RPA Hub
description: Use mTLS authentication for client authentication and verify authenticity of the automation packages by generating a code signing certificate.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring RPA Hub, RPA Hub, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Obtaining client authentication and code signing certificates for RPA Hub

Use mTLS authentication for client authentication and verify authenticity of the automation packages by generating a code signing certificate.

-   **Client authentication**

    Client authentication enables mutual TLS \(mTLS\) authentication between the Unattended Robot application and the ServiceNow server while making a connection.

    You can either generate and install user certificates or export active directory certificates.

-   **Code signing certificate**

    A code signing certificate is used for signing and verifying the automation packages from RPA Desktop Design Studio. This certificate detects any tampering or corruption of scripts before they're run.

    The code signing certificate is validated during the Unattended Robot and Attended Robot executions.


If you set the **sn\_rpa\_fdn.code\_signing\_required** system property to true in the RPA Hub scoped application, a code signing certificate is required while publishing an automation project. For more information, see [Configure RPA Hub properties](../../rpa-hub/reference/rpahub-sys-properties.md) and [Publish an automation project in RPA Desktop Design Studio](../../rpa-studio/task/publish-automation-project.md).

Explore the following topics to generate a client authentication and a code signing certificate.

-   **[Generating and installing user certificates](use-user-certificates-rpa.md#)**  
You can generate and install a user certificate for client authentication and code signing in your Windows machine, if you have the admin role.
-   **[Exporting Microsoft Active Directory certificates](export-certificates-rpa.md#)**  
You can export Microsoft Active Directory certificates, such as root, intermediate, and a client authentication certificate, for authentication purposes. You then register the exported root and intermediate certificate in the ServiceNow instance and map the exported client authentication certificate to the user.

**Parent Topic:**[Creating integrations with applications](../../../build/create-integrations-apps/concept/create-integrations-applications.md)

