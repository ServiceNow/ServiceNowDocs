---
title: Export the public key certificate to trust the LDAP certificate
description: Export the public key certificate and import it into the application when you configure Microsoft Active Directory for SSL access.
locale: en-US
release: xanadu
product: LDAP integration
classification: ldap-integration
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure Microsoft Active Directory for secure LDAPS communication, LDAP integration, Authentication, Access Management]
---

# Export the public key certificate to trust the LDAP certificate

Export the public key certificate and import it into the application when you configure Microsoft Active Directory for SSL access.

## Before you begin

Role required: admin

## About this task

If your Certificate Authority is not a trusted third party vendor, you must export the certificate for the issuing CA so we can trust it, and, by association, trust the LDAP server certificate. For MS Certificate Services users, you can view the certificate path by viewing the certificate in the console used to export; select the **Certificate Path** tab. You must export all certificates in the chain. You can find the CA certificate in the same folder as the LDAP certificate by looking for the name in the Certificate Path. Submit all certificates for importing to your instance.

## Procedure

1.  From a current or new MMC console, add the Certificate \(Local Computer\) snap-in.

2.  Open the `Personal/Certificates` folder.

3.  Locate the new certificate.

    The Issued to column shows the FQDN of the domain controller.

4.  Right-click the certificate and select All Tasks/Export.

5.  Export to DER or Base-64 format.

    Name the file using the format `MyCompany.cer`. This is the public key certificate the needs to be used on the instance to communicate securely with your domain controller.

6.  Test LDAPS locally before you submit the certificate to the instance.


## What to do next

After completing this procedure, import the public key certificate into the application.

See [Install the LDAP X.509 SSL certificate](t_UploadTheX509SSLCertificate.md) to upload the certificate into the application.

