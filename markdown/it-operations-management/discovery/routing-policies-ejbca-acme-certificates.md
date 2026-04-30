---
title: Create a routing policy for EJBCA ACME certificates
description: Automate your EJBCA ACME workflows by creating a routing policy that aligns with your Certificate Signing Requests \(CSRs\) to request, renew, and revoke certificates.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-07-20"
reading_time_minutes: 1
breadcrumb: [ACME integration with KeyFactor EJBCA for automated flows, Automated Certificate Management Environment, ITOM Visibility, IT Operations Management]
---

# Create a routing policy for EJBCA ACME certificates

Automate your EJBCA ACME workflows by creating a routing policy that aligns with your Certificate Signing Requests \(CSRs\) to request, renew, and revoke certificates.

## Before you begin

Role required: discovery\_admin, Public Key infrastructure \(PKI\) admin, admin

## About this task

Streamline your certificate life-cycle workflow by filling out a routing policy form. This form configures your routing policy fields to make sure your Certificate Signing Request \(CSR\) aligns with the correct Certificate Authority \(CA\) routing policy.

## Procedure

1.  Navigate to **All** &gt; **Certificate Management** &gt; **Certificate Routing Policies**.

2.  Select **New**.

3.  On the Certificate Routing Policy form, fill in the fields.

    For a description of the field values, see [Certificate routing policy form table](../reference/certificate-routing-policy-form-table.md).

    **Warning:** For your automated workflow to work, you must fill in every field in your routing policy form. If you don’t, your CSR requires manual steps. You can see all the fields and values at the [Certificate routing policy form table](../reference/certificate-routing-policy-form-table.md).

4.  After you have filled out the fields, select **Submit**.


## What to do next

Navigate to **All** &gt; **Certificate Management** &gt; **Certificate Routing Policies**.

By locating your routing policy on the Certificate Routing Policies page, you validate your EJBCA ACME Certificate routing policy.

