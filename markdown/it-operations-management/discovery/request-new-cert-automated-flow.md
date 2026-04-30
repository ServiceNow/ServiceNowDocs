---
title: Request new certificate using automated certificate management
description: Request a new certificate and automatically retrieve the certificates for an application using automated certificate management. Certificate Inventory and Management Version 2.1.0 supports requesting certificates from DigiCert and Entrust CA Gateway. Version 2.3.2 also supports Microsoft CA.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Automated certificate management for TLS certificates, Configuring Certificate Inventory and Management, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Request new certificate using automated certificate management

Request a new certificate and automatically retrieve the certificates for an application using automated certificate management. Certificate Inventory and Management Version 2.1.0 supports requesting certificates from DigiCert and Entrust CA Gateway. Version 2.3.2 also supports Microsoft CA.

## Before you begin

Ensure the Certificate Management catalog is enabled and that a Routing Policy is created.

For DigiCert only: You need to get the API key from DigiCert with the domain already validated by DigiCert. If you submit a certificate request with a new domain that is not validated by DigiCert, the request will show as Pending, the automated flow will not be able to fetch the certificate information, and the request will be marked as Failed.

Role required: Certificate requester, PKI Admin, PKI User, or Admin

Certificate requester is a user who does not have the PKI Admin or PKI User role.

**Note:** Approvals are only supported in the Fulfiller approval experience at this time.

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Certificate Management**.

2.  Select **Request New Certificate - Automated flow**.

3.  Provide details for the mandatory fields: **CSR** and **Validity Period**.

4.  Fill in or choose additional information on the form, and then click **Submit** to proceed with the order.

    The Routing Policy \[sn\_disco\_certmgmt\_routing\_policy\] table helps to fetch the CA routing policy ID. If a single routing policy ID is not returned, then the approver must select the routing policy and approve the task. For more information, see [Approve certificate tasks](../concept/automated-cert-requests.md).

    This creates a New Certificate Task which then triggers the automated flow. In the routing policy, if Approval Required field was checked, the task requires approval before the automated flow begins.


## Result

-   Once the request is submitted, the automated flow makes the request to the CA to get the certificate.

    **Note:** Powershell Step is used for Microsoft CA. This requires the plugin: com.glide.hub.action\_step.powershell.

-   A record is created in the Certificate Extension \[sn\_disco\_certmgmt\_certificate\_extension\] table once the certificate is successfully fetched.
-   Every 30 minutes, the following scheduled job runs and checks for status: DigiCert – Track Certificate Order Status.

    **Note:** There are no scheduled jobs for Entrust CA Gateway and Microsoft CA.

-   If the certificate is available, it is attached to the certificate task.
-   The certificate task is then marked Completed and a change request is created.
-   If multiple tasks are created for the same CSR and Allow Duplication is not checked in the routing policy, the task fails.
-   If the validity period exceeds the matched routing policy validity period, the task fails.

