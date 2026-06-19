---
title: Enable email with third-party contacts
description: Configure email communication with third-party contacts to enable email notification of assessments and issues.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/third-party-risk-management/set\_sys\_props\_for\_email.html
release: australia
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Enable email with third-party contacts

Configure email communication with third-party contacts to enable email notification of assessments and issues.

## Before you begin

Role required: admin

## About this task

**Note:** Third-party contacts see your organization's name in all references on the Third-party portal. You specify the name in the `sn_vdr_risk_asmt.company.name` property setting. See [Configure TPRM properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-properties-configure.md).

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **Email Properties**.

2.  Select both the **Email sending enabled** and **Email receiving enabled** check boxes and then select **Save**.

    Email sending and email receiving are enabled at the system level.


## What to do next

You can now proceed with configuring email communication scenarios, including those that involve external or third-party contacts.

Assessment-related email notifications are now sent as a single consolidated summary instead of individual per-event messages. Users can configure notification frequency, detail level, and delivery channel from their notification preferences. Multi-language email templates are available for supported languages.

