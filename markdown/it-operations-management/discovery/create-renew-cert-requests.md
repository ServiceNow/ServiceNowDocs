---
title: Create a renewal certificate request
description: Manually initiate renewal requests for certificates using the Service Catalog for added flexibility and control.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Manual flow for certificate requests, Configuring Certificate Inventory and Management, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Create a renewal certificate request

Manually initiate renewal requests for certificates using the Service Catalog for added flexibility and control.

## Before you begin

Ensure that the Certificate Management catalog is enabled.

Role required: pki\_admin

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Certificate Management**.

2.  Select **Renew Certificate**.

3.  Select a Certificate CI.

4.  Provide the necessary information for the following mandatory fields.

    -   **Certificate Signing Request**
    -   **Requested for**
    -   **Approver**
5.  Enter or select additional details on the form as needed.

6.  Select **Submit**.


## Result

The Certificate task is generated and submitted for approval. The approval field is view-only for pki\_user and editable for pki\_admin.

**Note:** The notification process for certificate renewal exclusively supports manual flow and does not involve automated certificate management. For CSR information, you must use automated certificate management.

When monitoring the status of a certificate order, if there's a configuration-related issue, the task may get stuck in "work in progress." The PKI Admin is responsible for resolving such issues. For example, if the MID Server is down during the scheduled job tracking the certificate order status, the system waits for the next scheduled job instead of logging an error. If the MID Server is brought back up before the subsequent job, the certificate retrieval proceeds accordingly.

