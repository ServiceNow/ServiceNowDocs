---
title: Use bulk certificate upload
description: In Certificate Inventory and Management version 1.2.0 and later, you can import up to 5000 SSL certificates in bulk using a single .xlsx file.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery/run-cert-inventory-mgmt-bulk-url.html
release: brazil
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Visibility to TLS certificates, Configure, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Use bulk certificate upload

In Certificate Inventory and Management version 1.2.0 and later, you can import up to 5000 SSL certificates in bulk using a single .xlsx file.

## Before you begin

Role required: pki\_user or pki\_admin

The default admin is assigned both the pki\_user and pki\_admin roles. The users with the following roles have access to bulk certificate upload.

-   sn\_disco\_certmgmt.pki\_user
-   sn\_disco\_certmgmt.pki\_admin

## Procedure

1.  Navigate to **All** &gt; **Certificate Management** &gt; **Bulk Upload Certificates**.

2.  From the Bulk Upload page, select **Download Template File** \(.xlsx\) link to download the `sample_cmdb_ci_certificate.xlsx` file.

3.  Open the downloaded `sample_cmdb_ci_certificate.xlsx` file.

4.  Refer to the values in the sample rows as a guide and add the SSL certificate's properties into the corresponding columns.

    Each entry in the Excel sheet corresponds to a CI certificate. For a description of each field in the `sample_cmdb_ci_certificate.xlsx` field, see [.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery/bulk-certificate-upload-template-fields.md)

    **Note:**

    -   For maintaining the certificate’s chain relationship, every certificate must have the fingerprint of its root certificate in the **root\_issuer** column and the fingerprint of its issuer in the **issuer** column.
    -   For self-signed certificates, both **root\_issuer** and **issuer** must have the value of the certificate's fingerprint.
5.  Delete the sample rows and then save the `sample_cmdb_ci_certificate.xlsx` file.

6.  Navigate back to the Bulk Upload Certificates form.

7.  Select **Browse File** and choose the updated `sample_cmdb_ci_certificate.xlsx` file.

8.  Select **Upload**.


## Result

If any errors occur while uploading, a warning message and link to the error logs appears. Only users with the admin role can view these logs. Errors can occur when a mandatory field is left empty or a valid\_from epoch value is greater than that of valid\_to.

After the file is successfully uploaded, you can see a success message displayed with a **View All** redirect link. You can view a list of the certificates that were added to the Unique Certificate \[cmdb\_ci\_certificate\] table.

