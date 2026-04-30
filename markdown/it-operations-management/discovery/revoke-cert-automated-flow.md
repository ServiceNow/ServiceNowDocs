---
title: Revoke a certificate using automated certificate management
description: Revoke certificate for an application. Revocation doesn't require approval if order Id and certificate Id are present in the Certificate Extension table. If order Id and certificate Id aren't present in the Certificate Extension table, then you need approval.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-08-14"
reading_time_minutes: 2
breadcrumb: [Automated certificate management for TLS certificates, Configuring Certificate Inventory and Management, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Revoke a certificate using automated certificate management

Revoke certificate for an application. Revocation doesn't require approval if **order Id** and **certificate Id** are present in the Certificate Extension table. If **order Id** and **certificate Id** aren't present in the Certificate Extension table, then you need approval.

## Before you begin

[Set up the routing policy for automated certificate management](setup-routing-policy.md) to ensure the Certificate Management catalog is enabled.

To revoke an existing certificate, make sure the certificate has its extension details populated in the \[sn\_disco\_certmgmt\_certificate\_extension\] table. You don't need to include an endpoint URL. The system will automatically hardcode the revoke URLs for the discovery. Currently, these details populate automatically by the Discovery DigiCert CA Pattern or for any certificates created through the automated flow. However, for Entrust certificates, this only works if you [Request new certificate using automated certificate management](request-new-cert-automated-flow.md).

Role required: pki\_admin or admin

**Note:** Currently, approvals are only supported in the Fulfiller approval experience.

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Certificate Management**.

2.  Select **Revoke Certificate – Automated flow**.

3.  Enter the Issued Certificate which you want to revoke \(for instance: www.undefined.com\).

    Multiple Certificates can be selected for revoking.

4.  Provide an appropriate reason for revoking the certificate.

    For Microsoft CA the reason should be an integer. If any other value is given, a default value of 0 will be used which means unspecified.

5.  To place the revoke order, select **Submit**.

6.  In the confirmation pop-up, select **OK**.


## Result

1.  A task is automatically created when you request a revocation.
    -   If **order Id** and **certificate Id** are present in the Certificate Extension \[sn\_disco\_certmgmt\_certificate\_extension\] table, revocation does not require approval.
    -   If **order Id** and **certificate Id** aren't present in the Certificate Extension \[sn\_disco\_certmgmt\_certificate\_extension\] table, then the task requests approval.
    -   If the serial number for Entrust CA Gateway isn't present in the Certificate Extension \[sn\_disco\_certmgmt\_certificate\_extension\] table, then the task requests approval.
2.  Once the PKI team provides approval, the mapping between the certificate and CA occurs based on the Routing policy selected.
3.  This triggers the revocation operation for the CA selected which uses the CA APIs.
4.  Details are stored in the Certificate Extension table.
5.  Every 30 minutes, the following scheduled job runs and checks for status: DigiCert – Track Certificate Order Status.

    **Note:** There are no scheduled jobs for Entrust CA Gateway and Microsoft CA.

6.  The status of the certificate is marked as revoked.

**Note:**

Certificates can't be revoked if Certificate Authority or Certificate Id details are missing in the Certificate Extension \[sn\_disco\_certmgmt\_certificate\_extension\] table. For Entrust CA Gateway, certificates can't be revoked if the Serial number is missing. Discover the certificate via [Certificate Authority query](../concept/run-cert-discovery.md) to populate the required details in the Certificate Extension table. After that, Discovery selects the routing policy and approves the task.

Revoke certificate API request. If "skip\_approval" is true, the revoke process is completed faster. If "skip\_approval" is false, the revoke process is completed when the DigiCert or Entrust CA Gateway admin has approved or rejected the revoke request. To skip the approval step, the API key must have admin privileges.

