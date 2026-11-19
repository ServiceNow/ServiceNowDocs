---
title: Revoke certificates through CyberArk Certificate Manager SaaS
description: Revoke a certificate through the CyberArk Certificate Manager SaaS to invalidate it before its scheduled expiration date.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/discovery/revoke-cert-cyberark-venafi.html
release: zurich
product: Discovery
classification: discovery
topic_type: task
last_updated: "2024-12-19"
reading_time_minutes: 1
keywords: [CyberArk Certificate Manager SaaS certificate revocation]
breadcrumb: [Certificate management with CyberArk Certificate Manager SaaS, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Revoke certificates through CyberArk Certificate Manager SaaS

Revoke a certificate through the CyberArk Certificate Manager SaaS to invalidate it before its scheduled expiration date.

## Before you begin

The certificate must be originally issued through CyberArk and be currently valid.

Role required: pki\_admin or admin

## About this task

Common reasons for revocation include key compromise, change in certificate details, or decommissioning of the associated service.

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Service Catalog**.

2.  Access the form for renewing a certificate.

    1.  Select **Certificate Management**.

    2.  Select **Automated Flow**.

    3.  Select **Revoke Certificate \(Automated\)**.

3.  For the **Select how to manage your certificate** value, select **CyberArk Certificate Manager SaaS**.

4.  Select the certificate that must be revoked.

    1.  In the **Issued Certificate** field, select the Lock icon \[Omitted image "lock-icon.png"\] Alt text:.

    2.  Select the Lookup using list icon \[Omitted image "lookup-using-list.png"\] Alt text: to find and select the certificate.

    3.  On the Unique Certificates form, select the certificate to be revoked.

5.  In the **Reason for Revoking Certificate** field, provide one of the revocation reasons for CyberArk Certificate Manager SaaS.

    You can also display these reasons by expanding **More information**.

    -   SUPERSEDED: The certificate has been replaced
    -   KEY\_COMPROMISE: The private key has been compromised
    -   AFFILIATION\_CHANGED: The certificate holder's affiliation has changed
    -   CESSATION\_OF\_OPERATION: The service is no longer operational
    -   UNSPECIFIED: Any other reason.
6.  Select **Submit**.


## Result

The revocation request is sent to CyberArk for processing. The certificate status is updated in the relevant certificate task to reflect the revocation. The certificate is invalidated and can no longer be used for authentication.

