---
title: Create routing policies for CyberArk Certificate Manager SaaS
description: Create routing policies to direct certificate requests to CyberArk Certificate Manager SaaS by matching attributes such as organization, domain, and certificate type to the Routing Policy \[sn\_disco\_certmgmt\_routing\_policy\] table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery/create-routing-policy-cyberark.html
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2024-12-19"
reading_time_minutes: 1
keywords: [CyberArk Certificate Manager SaaS routing policy]
breadcrumb: [Certificate management with CyberArk Certificate Manager SaaS, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Create routing policies for CyberArk Certificate Manager SaaS

Create routing policies to direct certificate requests to CyberArk Certificate Manager SaaS by matching attributes such as organization, domain, and certificate type to the Routing Policy \[sn\_disco\_certmgmt\_routing\_policy\] table.

## Before you begin

Configure CyberArk credentials. For more information, see [Configure CyberArk Certificate Manager SaaS credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/configure-cyberark-venafi-creds.md).

Role required: pki\_admin or admin.

## Procedure

1.  Navigate to **All** &gt; **Certificate Management** &gt; **Certificate Routing Policies**.

2.  Select **New**.

3.  On the Certificate Routing Policy form, fill in the fields.

    For a description of the field values, see [Certificate Routing Policy form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/certificate-routing-policy-form.md).

4.  If used by your organization as filtering criteria, set values for the **Organization**, **Organizational Unit**, **Locality**, **Country**, **State**, or **Email Address** fields.

    **Note:** Use an asterisk \(\*\) for wildcard matching and RegEx patterns for complex matching requirements.

5.  Select **Submit**.


## Result

The routing policy is created and directs matching certificate requests to CyberArk. Certificate requests matching the policy criteria are automatically routed to CyberArk for processing. For more information, see [Routing policy details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/how-routing-policy-works.md).

