---
title: Renew certificates through CyberArk Certificate Manager SaaS
description: Renew an existing certificate through the CyberArk Certificate Manager SaaS to extend its validity period before expiration.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery/renew-cert-cyberark-venafi.html
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2024-12-19"
reading_time_minutes: 1
keywords: [CyberArk Certificate Manager SaaS certificate renewal]
breadcrumb: [Certificate management with CyberArk Certificate Manager SaaS, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Renew certificates through CyberArk Certificate Manager SaaS

Renew an existing certificate through the CyberArk Certificate Manager SaaS to extend its validity period before expiration.

## Before you begin

Role required: pki\_admin, pki\_user, or admin

## About this task

The renewal process uses the same certificate attributes and routing policy as the original certificate request.

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Service Catalog**.

2.  Access the form for renewing a certificate.

    1.  Select **Certificate Management**.

    2.  Select **Automated Flow**.

    3.  Select **Renew Certificate \(Automated\)**.

3.  In the **Issued Certificate** field, select the Lookup using list icon \[Omitted image "lookup-using-list.png"\] Alt text: to find and select the certificate.

    The date the certificate expires is displayed in the **Certificate Expires On** field.

4.  Review and update the details of the certificate as needed.

    For a description of the field values, see [Certificate request form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/req-new-cert-form-table-fields.md).

5.  Select **Submit**.


## Result

The renewal request is routed to CyberArk Certificate Manager SaaS. The original certificate remains valid until the renewed certificate is issued.

