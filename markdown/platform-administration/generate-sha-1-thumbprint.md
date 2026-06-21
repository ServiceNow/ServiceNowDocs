---
title: Generate SHA-1 thumbprint
description: Generate an SHA-1 thumbprint using the JWT provider's sys\_id, the Java Key Store \(JKS\) certificate's sys\_id, and the JKS certificate's alias to the GraphCertificateOAuthTemplate script.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/platform-administration/generate-sha-1-thumbprint.html
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure client credential flow for SMTP OAuth2 using certificate-based authentication, Send email using client credential flow, Advanced email setup, Configure email administration, Email Administration, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Generate SHA-1 thumbprint

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

[Create an OAuth API script](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-administration/create-oauth-api-script-cred-flow.md)

**Parent Topic:**[Configure client credential flow for SMTP OAuth2 using certificate-based authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-administration/config-credential-flow-certificate.md)

