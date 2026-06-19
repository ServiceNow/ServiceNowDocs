---
title: Validate the auto-renew status of your certificate
description: Confirm that you set your certificate to renew automatically before it expires.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery/validate-cert-auto-renew-status.html
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Automated certificate renewal, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Validate the auto-renew status of your certificate

Confirm that you set your certificate to renew automatically before it expires.

## Before you begin

Complete one of the following tasks before you validate your certificate:

-   [Set a certificate to renew automatically](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/set-certificate-to-renew-automatically.md)
-   [Request a new certificate and set it to auto-renew](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/request-new-cert-set-to-auto-renew.md)

Role required: pki\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Unique Certificates**.

2.  Select the Certificate that you want to validate.

3.  Select the **Certificates metadata** tab.

4.  Check that the **Auto renew enabled** field is set to **true**.

    **Note:** The pki\_admin can select this field and edit it.


