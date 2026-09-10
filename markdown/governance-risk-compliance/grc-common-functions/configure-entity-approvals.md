---
title: Configure entity approvals
description: Specify which types of entity changes require review before they take effect.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-common-functions/configure-entity-approvals.html
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-09-02"
reading_time_minutes: 1
breadcrumb: [Entity lifecycle management, Common GRC features, Governance, Risk, and Compliance]
---

# Configure entity approvals

Specify which types of entity changes require review before they take effect.

## Before you begin

Role required: sn\_grc\_change\_mgmt.admin

## About this task

Entity approvals can be configured for new, updated, or retired entities. When a change meets the configured condition, the system creates a change task for review.

## Procedure

1.  Navigate to **All** &gt; **Entity management** &gt; **Impact approvals**.

2.  Select **Settings**.

3.  Turn on the **Enable impact approvals** toggle.

4.  Configure the condition for the entity changes that require review.

    |Field|Description|
    |-----|-----------|
    |Field|Attribute used to define the approval condition. The available option is **Change type**.|
    |Operator|Method used to evaluate the change type. Select **is** to specify one change type or **is one of** to specify multiple change types.|
    |Value|Entity change types that require review. Select **New**, **Update**, **Retire**, or a combination of these values.|

5.  Select **Save**.


## Result

Entity approvals are configured for the selected change types. When an entity change meets the configured condition, the system creates a change task on the **Impact approvals** page. Changes that don't meet the condition take effect without a change task.

**Parent Topic:**[Entity lifecycle management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/entity-change-management.md)

