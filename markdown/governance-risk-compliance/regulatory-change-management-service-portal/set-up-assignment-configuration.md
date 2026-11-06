---
title: Set up auto-assignment for regulatory alerts
description: Set up an assignment configuration record to enable auto-assignments for regulatory alerts of the type regulatory event.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/governance-risk-compliance/regulatory-change-management-service-portal/set-up-assignment-configuration.html
release: australia
product: Regulatory Change Management Service Portal
classification: regulatory-change-management-service-portal
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Recommend citations on regulatory alerts, Regulatory alerts, Regulatory Change Management Core UI, Use, Regulatory Change Management, Governance, Risk, and Compliance]
---

# Set up auto-assignment for regulatory alerts

Set up an assignment configuration record to enable auto-assignments for regulatory alerts of the type regulatory event.

## Before you begin

The GRC: Assignment and Approval Configurations \(sn\_grc\_appr\) application for approval and assignment configurations is installed as a dependency of the Regulatory Change Management application.

Role required: sn\_grc\_appr.admin or sn\_grc\_reg\_change.manager

## About this task

You can route regulatory alerts to domain experts who can address compliance issues within their areas of specialization. This facilitates proactive management of regulatory risks and obligations.

When a regulatory alert is created without a coordinator, the assignment configuration is applied automatically.

## Procedure

1.  Navigate to **All** &gt; **Assignment and Approval Configurations** &gt; **Assignment Configurations**.

2.  Select **New**.

    The Assignment Configuration New Record form is displayed.

3.  On the form, fill in the fields.

    For information on the fields in the form, see [Assignment Configuration New Record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/governance-risk-compliance/grc-common-functions/assignment-configuration-new-record.md).

    **Warning:** You cannot have more than one approval configuration applying to the table with the same priority.

4.  Select **Submit**.


**Parent Topic:**[Recommend citations on regulatory alerts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/governance-risk-compliance/regulatory-change-management-service-portal/retrain-ml-reg-compliance-mapping.md)

