---
title: Set up the routing policy for ACME
description: Set up a routing policy to establish an Automated Certificate Management Environment \(ACME\). It involves creating a policy based on factors such as Certificate Authority \(CA\), environment, and other features, ensuring efficient SSL/TLS certificate management.
locale: en-US
release: xanadu
product: Discovery
classification: discovery
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring ACME, Automated Certificate Management Environment, Discovery, ITOM Visibility, IT Operations Management]
---

# Set up the routing policy for ACME

Set up a routing policy to establish an Automated Certificate Management Environment \(ACME\). It involves creating a policy based on factors such as Certificate Authority \(CA\), environment, and other features, ensuring efficient SSL/TLS certificate management.

## Before you begin

Role required: pki\_admin, flow\_designer, action\_designer, or admin

## About this task

Duplicate certificate requests aren’t allowed. However, you can override this setting by checking the Allow duplicate requests check box. A certificate request is considered duplicate if there’s another certificate task with the same domain name that is still in progress.

The routing policy decides which CA must be contacted for certificate operations. It contains the CA, CA URL, Credential, Approval Group, Assignment Group, and CSR attributes. The routing policy triggers the flow for requesting certificates for specific CAs.

## Procedure

1.  Navigate to **All** &gt; **Certificate Management** &gt; **Certificate Routing Policies**.

2.  Select **New**.

3.  On the **Certificate Routing Policy** form, fill in the fields.

    For the description of the field values, see [Certificate Routing Policy form](../reference/certificate-routing-policy-field-values.md).

4.  Select **Update**.


