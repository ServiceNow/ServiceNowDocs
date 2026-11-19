---
title: Request certificates through CyberArk Certificate Manager SaaS
description: Submit a certificate request managed through CyberArk Certificate Manager SaaS using configured routing policies.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/discovery/request-cert-cyberark-venafi.html
release: zurich
product: Discovery
classification: discovery
topic_type: task
last_updated: "2024-12-19"
reading_time_minutes: 1
keywords: [CyberArk Certificate Manager SaaS certificate request]
breadcrumb: [Certificate management with CyberArk Certificate Manager SaaS, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Request certificates through CyberArk Certificate Manager SaaS

Submit a certificate request managed through CyberArk Certificate Manager SaaS using configured routing policies.

## Before you begin

-   CyberArk credentials must have been configured. For more information, see [Configure CyberArk Certificate Manager SaaS credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/configure-cyberark-venafi-creds.md).
-   Routing policies must have been configured. For more information, see [Create routing policies for CyberArk Certificate Manager SaaS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/create-routing-policy-cyberark.md).

Role required: pki\_admin, pki\_user, or admin.

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Service Catalog**.

2.  Access the form for requesting a new certificate.

    1.  Select **Certificate Management**.

    2.  Select **Automated Flow**.

    3.  Select **Request New Certificate \(Automated\)**.

3.  For the **Select how to manage your certificate** value, select **CyberArk Certificate Manager SaaS**.

4.  On the Request New Certificate \(Automated\) form, fill in the fields.

    For a description of the field values, see [Certificate request form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/req-new-cert-form-table-fields.md).

    **Note:** A configured routing policy is applied automatically based on certificate attributes. For more information, see [Create routing policies for CyberArk Certificate Manager SaaS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/create-routing-policy-cyberark.md)

5.  Select **Submit**.


## Result

The certificate request is routed to CyberArk for processing. The request status is updated in the relevant certificate task as it progresses through the workflow.

