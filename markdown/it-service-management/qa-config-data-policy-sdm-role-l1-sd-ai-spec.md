---
title: Configure coaching assessment access
description: Verify that the data policy and role configuration for coaching assessments are active in your instance. These settings control access to coaching opportunity records and give Service Desk Managers read access to quality assessments.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/qa-config-data-policy-sdm-role-l1-sd-ai-spec.html
release: australia
topic_type: task
last_updated: "2026-09-18"
reading_time_minutes: 1
breadcrumb: [Configure, L1 IT Service Desk AI Specialist, IT Service Management]
---

# Configure coaching assessment access

Verify that the data policy and role configuration for coaching assessments are active in your instance. These settings control access to coaching opportunity records and give Service Desk Managers read access to quality assessments.

## Before you begin

Role required: admin

## About this task

The IT Service Management Resolution coaching opportunity is protected by a data policy, and Service Desk Managers \(SDMs\) can view quality assessments tied to that opportunity.

## Procedure

1.  Verify that the data policy on the **ITSM Resolution** coaching opportunity \[sn\_coaching\_opportunity\] is active.

    The data policy makes the editable fields on the **ITSM Resolution** coaching opportunity record read-only. The policy applies across the UI, SOAP, and import sets.

2.  Verify that the **Service Desk Manager** \[sn\_sow\_itsm\_common.sn\_service\_desk\_manager\] role contains the **coaching trainee** \[sn\_coaching.trainee\] role.

    This role containment gives Service Desk Managers field-level read access to coaching assessment records.

3.  Verify that a user with both the coaching trainee and Service Desk Manager roles can view all quality assessments created from the **ITSM Resolution** coaching opportunity, and their own assessments.


