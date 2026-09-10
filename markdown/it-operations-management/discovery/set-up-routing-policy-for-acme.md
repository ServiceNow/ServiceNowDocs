---
title: Set up routing policies for ACME
description: Set up routing policies to establish automated certificate management based on factors such as certificate authority \(CA\) and environment for efficient SSL/TLS certificate management.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/discovery/set-up-routing-policy-for-acme.html
release: zurich
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Automated certificate management with ACME, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Set up routing policies for ACME

Set up routing policies to establish automated certificate management based on factors such as certificate authority \(CA\) and environment for efficient SSL/TLS certificate management.

## Before you begin

Role required: pki\_admin, flow\_designer, action\_designer, or admin

## About this task

The routing policy decides which CA must be contacted for certificate operations. It contains the CA, CA URL, Credential, Approval Group, Assignment Group, and CSR attributes. The routing policy triggers the flow for requesting certificates for specific CAs.

Duplicate certificate requests aren’t allowed. However, you can override this setting by selecting the Allow duplicate requests check box. A certificate request is considered duplicate if there’s another certificate task with the same domain name that is still in progress.

## Procedure

1.  Navigate to **All** &gt; **Certificate Management** &gt; **Certificate Routing Policies**.

2.  Select **New**.

3.  On the **Certificate Routing Policy** form, fill in the fields.

    For a description of the field values, see [Certificate Routing Policy form for ACME](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/certificate-routing-policy-field-values.md).

4.  Select **Submit**.


