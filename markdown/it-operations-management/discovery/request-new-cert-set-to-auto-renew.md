---
title: Request a new certificate and set it to auto-renew
description: Set your certificate to auto-renew when you first request it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery/request-new-cert-set-to-auto-renew.html
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Automated certificate renewal, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Request a new certificate and set it to auto-renew

Set your certificate to auto-renew when you first request it.

## Before you begin

Complete the following tasks to configure your system to renew your certificates automatically:

1.  [Configure the MID Server for automatic certificate renewal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/configure-mid-server-automatic-cert-renewal.md)
2.  [Add the required applications and capabilities to your MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/add-req-apps-capabilities-to-mid-server.md)
3.  [Configure System Properties for automatic certificate renewal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/config-sys-props-for-auto-cert-renewal.md)

Role required: pki\_admin or admin

## Procedure

1.  Navigate to **Service Catalog** &gt; **Certificate Management** &gt; **Automated Flow** &gt; **Request New Certificate \(Automated\)**.

2.  Select the check box **Want to Generate CSR?**

3.  On the "request a new certificate" form, fill in the fields.

    For a description of the field values, see [Certificate request form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/req-new-cert-form-table-fields.md).

4.  Select **Generate**.

5.  Set the **Validity Period for Certificate \(in Days\)** field to validity period of the certificate.

6.  Set the **Renew Automatically** field to **Yes**.

    **Note:** By selecting **Yes**, a new field appears called **How many days before expiry does this certificate need to be renewed?**.

7.  Select the number of days before the certificate you want to renew in the **How many days before expiry does this certificate need to be renewed?** field.

8.  Select **Submit**.


## Result

Your new certificate is issued with instructions to renew automatically before it expires.

