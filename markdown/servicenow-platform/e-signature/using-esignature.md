---
title: Using e-signature
description: Users with the assigned e-signature roles can create templates for documents that require an electronic signature.
locale: en-US
release: australia
product: e-Signature
classification: e-signature
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [E-signature, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Using e-signature

Users with the assigned e-signature roles can create templates for documents that require an electronic signature.

## Role assignment

Before you begin using e-signature, you must assign the e-signature roles to the appropriate roles, groups, or users in your application. See [Components installed with e-signature](../reference/components-installed-with-e-signature.md) for more information.

## How to use e-signature templates

Users with the e-signature administrator \[sn\_esign.admin\] or manager \[sn\_esign.config\_manager\] role can create e-signature templates. Each e-signature template pairs a document type to sign \(managed document or knowledge article\) with a signature type \(signature, credential, or acknowledgment\). For example, you could create an e-signature template for a non-disclosure agreement that requires a typed or drawn signature. For more information, see [Create or modify an e-signature template](../task/configure-e-signature-configuration.md).

You can then use the e-signature template in task forms to request electronic signatures from users. In the HR Service Delivery application, for example, you can add HR tasks to HR cases or configure HR task templates to request electronic signatures per the selected e-signature template. See [E-signature for HR](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/hr-service-delivery/hr-e-signature.md) for HR-specific examples.

-   **[Create or modify an e-signature template](../task/configure-e-signature-configuration.md)**  
Create or modify an e-signature template to define an electronic document and signature configuration for use in task forms.
-   **[Using e-signature template for non-HR tasks](../task/configure-e-signature-non-hr.md)**  
Create or modify an e-signature template to define an electronic document and signature configuration for use in non-HR task forms.

**Parent Topic:**[E-signature](e-signature.md)

