---
title: Import a self-signed certificate
description: Import a self-signed certificate in a Windows system by using the Certificate Import Wizard. The Certificate Import Wizard is required to complete the self-signed certificate import process on a Windows Operating System \(OS\).
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Agent Client Collector Framework, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Import a self-signed certificate

Import a self-signed certificate in a Windows system by using the Certificate Import Wizard. The Certificate Import Wizard is required to complete the self-signed certificate import process on a Windows Operating System \(OS\).

## Before you begin

Ensure that you have followed the procedure for importing a self-signed certificate in a Windows system, as described in [Add a self-signed certificate to your operating system's truststore](add-certificate-trust-store.md).

Role required: agent\_client\_collector\_admin

## Procedure

1.  On the first page of the wizard, select **Next**.

    The truststore is typically located in the Trusted Root Certification Authorities directory of the certificate manager.

2.  Browse to the location where you have the self-signed certificate file.

    The file is typically located in the agent's `config/cert` directory.

3.  Select and hold \(or right-click\) the certificate file and select **Install certificate**.

4.  Select **Next**.

5.  Select the option to place the certificate in the Trusted Root Certification Authorities truststore.

6.  Select **Next** and **Finish** to complete the wizard.


## Result

The certificate is imported into the truststore.

## What to do next

If a security warning appears, select **Confirm** to confirm the import.

