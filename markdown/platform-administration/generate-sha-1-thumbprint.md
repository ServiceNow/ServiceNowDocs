---
title: Generate a SHA-1 thumbprint
description: Generate an SHA-1 thumbprint using the JWT provider's sys\_id, the Java Key Store \(JKS\) certificate's sys\_id, and the JKS certificate's alias to the GraphCertificateOAuthTemplate script.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [SMTP OAuth2 to use certificates, Send email using client credential flow, Advanced email setup, Configure, Email Administration, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Generate a SHA-1 thumbprint

Generate an SHA-1 thumbprint using the JWT provider's sys\_id, the Java Key Store \(JKS\) certificate's sys\_id, and the JKS certificate's alias to the GraphCertificateOAuthTemplate script.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scripts-Background**.

2.  Paste the following script to generate the SHA-1 thumbprint value.

    ```
    var certId = "<sys_id of the certificate record>";​
    
    var certAlias = "<alias name for the certificate>";​
    
    var gce = new GlideCertificateEncryption();​
    
    var thumbprint = gce.getThumbPrintFromKeyStore(certId, certAlias,"SHA-1");​
    
    gs.log(thumbprint);​
    ```

3.  Select **Run script**.


## What to do next

[Create an OAuth API script](create-oauth-api-script-cred-flow.md)

**Parent Topic:**[Configure client credential flow for SMTP OAuth2 using certificate-based authentication](config-credential-flow-certificate.md)

