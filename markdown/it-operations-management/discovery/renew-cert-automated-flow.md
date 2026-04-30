---
title: Renew a certificate using automated certificate management
description: Request renewal for a certificate and automatically retrieve the certificate for an application. This maintains secure and uninterrupted services as you extend the validity period of the certificate, preventing potential service disruptions due to expired certificates.
locale: en-US
release: xanadu
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Automated certificate management for TLS certificates, Configuring Certificate Inventory and Management, Certificate Inventory and Management, Discovery, ITOM Visibility, IT Operations Management]
---

# Renew a certificate using automated certificate management

Request renewal for a certificate and automatically retrieve the certificate for an application. This maintains secure and uninterrupted services as you extend the validity period of the certificate, preventing potential service disruptions due to expired certificates.

## Before you begin

[Set up the routing policy for automated certificate management](setup-routing-policy.md) to ensure the Certificate Management catalog is enabled.

To renew an existing certificate, make sure the certificate has its extension details populated in the \[sn\_disco\_certmgmt\_certificate\_extension\] table. Currently, these details populate automatically by the Discovery DigiCert CA Pattern or for any certificates created through the automated flow. However, for Entrust certificates, this only works if you [Request new certificate using automated certificate management](request-new-cert-automated-flow.md).

Role required: PKI Admin, Admin, Certificate Owner, or Users that are part of the Certificate Owner Group.

The Certificate Owner and Certificate Owner group contains the Certificate Requester role \(minimal role\).

**Note:** Approvals are only supported in the Fulfiller approval experience at this time.

## About this task

To renew an existing certificate, request a new certificate with the same details as the original certificate. Currently, there is no Renew API available for Entrust CA Gateway and Microsoft CA certificates. During a renewal request, a new certificate is generated internally with the same attributes as the selected certificate.

For renewing an existing certificate, CSR is mandatory. The requester can use an existing CSR if available or use a new CSR. If you want to use an existing CSR, use the same CSR to request a new certificate from the CA. If fields are entered using vault and java APIs, the CSR is generated.

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Certificate Management**.

2.  Click **Renew Certificate – Automated flow**.

3.  Provide details for the mandatory fields: **CSR** and **Validity Period**.

4.  Fill in or choose additional information on the form, and then click **Submit** to proceed with the order.


## Result

1.  The Routing Policy \[sn\_disco\_certmgmt\_routing\_policy\] table helps fetch the CA routing policy ID.
    -   If a single routing policy isn't matched, the approver must select the CA and trigger the flow.
    -   If the CSR contains a different domain name than the issued certificate domain name, the task requests approval.
    -   If a single routing policy is matched but renewal certificate information isn't available in the Certificate Extension \[sn\_disco\_certmgmt\_certificate\_extension\] table, the task requires approval.
    -   Certificates can't be renewed if the Certificate Authority and Order id or thumbprint details are missing for the certificate in the Certificate Extension \[sn\_disco\_certmgmt\_certificate\_extension\] table. Discover the certificate via [Certificate Authority query](../concept/run-cert-discovery.md) to populate the required details in the Certificate Extension table. After Discovery, select the routing policy and approve the task.
2.  This creates a task for the ordered certificate which triggers the flow to request renewal certificates.
3.  Once the request is submitted, the automated flow makes the request to the CA to get the certificate.

    **Note:** Powershell Step is used for Microsoft CA. This requires the plugin: com.glide.hub.action\_step.powershell.

4.  The Order id is stored in the Certificate Task \[sn\_disco\_certmgmt\_certificate\_task\] table and Certificate Extension \[sn\_disco\_certmgmt\_certificate\_extension\] table.

    **Note:** For Entrust CA Gateway, Certificate Serial Number and Enrollment Id are fetched. The Serial Number is stored in the Certificate Extension \[sn\_disco\_certmgmt\_certificate\_extension\] table.

5.  Every 30 minutes, the “DigiCert – Track Certificate Order Status” scheduled job runs and checks for status.

**Note:**

The system fetches details about the selected certificate from the Certificate Extension \[sn\_disco\_certmgmt\_certificate\_extension\] table and makes the request to the CA to renew the certificate. Certificates can't be renewed if the Certificate Authority, Order id, or thumbprint are missing from this table. If additional details are missing for renewing the certificate, the system logs a message and suggests what to do. In this case, you must discover the certificate using CA-based discovery. For more information, see [Run Certificate Discovery via Certificate Authority query](../concept/run-cert-discovery.md) to populate these details to the Certificate Extension table.

