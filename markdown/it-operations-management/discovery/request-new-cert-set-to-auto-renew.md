---
title: Request a new certificate and set it to auto-renew
description: Set your certificate to auto-renew when you first request it.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-09-02"
reading_time_minutes: 1
breadcrumb: [Automated Certificate Renewal, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Request a new certificate and set it to auto-renew

Set your certificate to auto-renew when you first request it.

## Before you begin

Complete the following tasks to configure your system to renew your certificates automatically:

1.  [Configure your MID Server for automatic certificate renewal](configure-mid-server-automatic-cert-renewal.md)
2.  [Add the required applications and capabilities to your MID Server](add-req-apps-capabilities-to-mid-server.md)
3.  [Configure System Properties for automatic certificate renewal](config-sys-props-for-auto-cert-renewal.md)

Role required: pki\_admin or admin

## Procedure

1.  Navigate to **Service Catalog** &gt; **Certificate Management** &gt; **Automated Flow** &gt; **Request New Certificate \(Automated\)**.

2.  Select the check box **Want to Generate CSR?**

3.  On the Request a new certificate form, fill in the fields.

    For a description of the field values, see [Requesting a new certificate form table](../reference/req-new-cert-form-table-fields.md).

4.  Select **Generate**.

5.  Set the **Validity Period for Certificate \(in Days\)** field to validity period of the certificate.

6.  Set the **Renew Automatically** field to **Yes**.

    **Note:** By selecting **Yes**, a new field appears called **How many days before expiry does this certificate need to be renewed?**.

7.  Select the number of days before the certificate you want to renew in the **How many days before expiry does this certificate need to be renewed?** field.

8.  Select **Submit**.


## Result

Your new certificate is issued with instructions to renew automatically before it expires.

