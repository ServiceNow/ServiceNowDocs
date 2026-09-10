---
title: Revoke certificates using ACME automated flow
description: Request a revoke certificate for an application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery/revoke-certificate-using-acme-automated-flow.html
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Automated certificate management with ACME, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Revoke certificates using ACME automated flow

Request a revoke certificate for an application.

## Before you begin

-   Ensure that a credential has been set up. For more information, see [Create credentials for ACME certificate authority](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/create-credential-for-acme-ca.md).
-   The Certificate Management catalog has been enabled.
-   A routing policy with a DNS challenge action exists. For more information, see [Set up routing policies for ACME](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/set-up-routing-policy-for-acme.md).
-   Role required: certificate administrator \[sn\_disco\_certmgmt.pki\_admin\] or admin.

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Service Catalog**.

2.  Access the form for renewing a certificate.

    1.  Select **Certificate Management**.

    2.  Select **Automated Flow**.

    3.  Select **Revoke Certificate \(Automated\)**.

3.  Unlock the **Issued Certificate** field.

4.  Select the Lookup using list icon \(\[Omitted image "lookup-using-list.png"\] Alt text: Lookup using list icon\) and select the certificate you want to revoke.

    You can select more than one certificate.

5.  Provide an appropriate reason for revoking the certificate.

6.  Place the revoke order by selecting **Submit**.

7.  In the confirmation dialog box, select **OK**.


## Result

A task is automatically created that triggers the revocation operation. After the operation is complete, the status of the certificate changes to Revoked.

