---
title: Unified Approval Rules Overview
description: The approval rules and approval configuration are unified to provide a consistent approach to managing approval workflows.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/sem-approval-rules-overiew.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Use, Unified Security Exposure Management, Security Operations]
---

# Unified Approval Rules Overview

The approval rules and approval configuration are unified to provide a consistent approach to managing approval workflows.

The Unified Approval Rules simplifies approval management by combining approval rules and approval configurations into a single, unified table. This enables one approval rule to apply to multiple finding types such as VR, CVR, AVR, and CC, unlike before when rules were specific to individual tables or findings.

It is a standardized way to route approval requests across multiple findings and remediation task tables. Administrators use Unified Approval Rules to define how approval requests are triggered, which tables they apply to, and how approvers are assigned across levels. You can configure rule types, conditions, expiry values, and multi-level approval requirements.

**Key updates:**

-   Support for multiple findings and remediation task tables.
-   Step-based rule configuration—rule type, applies to, conditions, levels.
-   Required approval levels before activation.
-   Configurable expiry periods for approvals and notifications.
-   Role-based routing using users and groups.
-   Support for exception rule approvals: Approval rules of type **exception\_rules** route exception rule creation and extension requests through the unified approval workflow.
-   Integration with questionnaire configuration: Approval rules of types deferral\_requests, and false\_positive can be linked to conditional questionnaire configurations for structured information gathering.

