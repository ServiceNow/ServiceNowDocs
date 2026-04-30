---
title: Revoke certificate using ACME automated flow
description: Request a revoke certificate for an application.
locale: en-US
release: xanadu
product: Discovery
classification: discovery
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Using ACME, Automated Certificate Management Environment, Discovery, ITOM Visibility, IT Operations Management]
---

# Revoke certificate using ACME automated flow

Request a revoke certificate for an application.

## Before you begin

Ensure that the Certificate Management catalog is enabled and that a Routing Policy is created.

Role required: pki\_admin or admin

## Procedure

1.  Access the certificate request automated flow.

    1.  Navigate to **All** &gt; **Service Catalog**.

    2.  Select **Certificate Management**.

    3.  Select **Automated Flow**.

2.  Select **Revoke Certificate \(Automated\)**.

3.  Unlock the **Issued Certificate** field.

4.  Select the Lookup using list icon \(![Lookup using list icon](../../itom-governance/image/lookup-using-list.png)\) and select the certificate you want to revoke.

    You can select more than one certificate.

5.  Provide an appropriate reason for revoking the certificate.

6.  Place the revoke order by selecting **Submit**.

7.  In the confirmation dialog box, select **OK**.


## Result

A task is automatically created that triggers the revocation operation. Once the operation completes, the status of the certificate changes to Revoked.

