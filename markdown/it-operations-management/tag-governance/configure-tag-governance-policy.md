---
title: Configure a tag policy for Tag Governance
description: Configure tag policies that define the criteria for tag audits on discovered cloud resources or CIs. View audit results on tag quality and compliance on the Tag Health dashboard.
locale: en-US
release: australia
product: Tag Governance
classification: tag-governance
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Establishing Tag Governance policies, Using Tag Governance, Tag Governance, ITOM Visibility, IT Operations Management]
---

# Configure a tag policy for Tag Governance

Configure tag policies that define the criteria for tag audits on discovered cloud resources or CIs. View audit results on tag quality and compliance on the Tag Health dashboard.

## Before you begin

Role required: sn\_itom\_tag.tag\_governance\_admin, admin.

## About this task

You can specify filters that narrow the scope of an audit, for example, to audit only service accounts and datacenters.

## Procedure

1.  Navigate to **All** &gt; **Tag Governance** &gt; **Policies**.

2.  Select **New** and then fill in the Tag Policies form.

    The form fields are described in [Tag Policies form](../../itom-cloud-accelerate/reference/tag-gov-tag-policies-form.md).

3.  Select **Submit**.

    -   The Tag Policy Runs related list displays the list of tag audit runs with their corresponding state, created, and updated timestamps.
    -   The Latest Policy Run Findings related list displays the results of the tag audit run.

## What to do next

-   Select the **Show Audit Results** related link to view all audit results.
-   Select the **Run Point Scan** related link to execute all applicable checks against the record.
-   For more information see, Flows and Subflows.

