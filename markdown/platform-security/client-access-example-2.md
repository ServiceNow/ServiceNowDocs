---
title: Add your certificate to the ServiceNow Trusted Key Store
description: Upload your key and certificate to the ServiceNow Trusted Key Store.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring client accessible secrets, Secrets Management, Platform Security]
---

# Add your certificate to the ServiceNow Trusted Key Store

Upload your key and certificate to the ServiceNow Trusted Key Store.

## Before you begin

Role required: admin

The public certificate that you created in this example is considered a “self-signed” certificate \(meaning it didn't come from a trusted root authority\). You must add the certificate to the ServiceNow Trusted Key Store for it to be used. When using a certificate that came from a Certificate Authority, you don't need to complete this step.

## Procedure

1.  In your local environment, open Terminal \(On Mac or Linux\), or Command Line \(in Windows\).

2.  Using the terminal, use `cd` to move into the folder where you have created your encryption keys.

3.  In the terminal, enter the following command:

    ```
    cat sm_public_cert.pem
    ```

    You must view the contents of your public certificate to copy it into the trusted key store. This `cat` command displays the certificate.

    ![Contents of the public certificate displayed in terminal](../images/client-side-2.png)

4.  Copy the certificate information to your clipboard.

    Start with and include the `-----BEGIN CERTIFICATE-----` line and end with and include the `-----END CERTIFICATE-----` line.

5.  On your ServiceNow instance, navigate to the **X.509 certificate** list by entering `sys_certificate.LIST` in the navigation filter.

    ![sys_certificate.LIST entered into the instance navigation filter](../images/client-side-3.png)

6.  Select **New** to create a **X.509 Certificate** record.

7.  In the form, fill in the following fields.

<table id="table_vmb_4wf_jxb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the certificate. This name can be any name you choose.

</td></tr><tr><td>

Format

</td><td>

Select **PEM****Note:** Privacy Enhanced Mail \(PEM\) files are a type of Public Key Infrastructure \(PKI\) file used for keys and certificates. The records you created in the previous steps are of this file type.

</td></tr><tr><td>

Type

</td><td>

Select **Trusted Store Cert**

</td></tr><tr><td>

Short Description

</td><td>

Description of the certificate. Enter a value that lets you know what this certificate is being used for.

</td></tr><tr><td>

PEM Certificate

</td><td>

Paste the certificate information that you copied in step 4.

</td></tr></tbody>
</table>8.  Select **Submit** to save the record.


**Parent Topic:**[Configuring client accessible secrets](../concept/client-access-secret-landing.md)

