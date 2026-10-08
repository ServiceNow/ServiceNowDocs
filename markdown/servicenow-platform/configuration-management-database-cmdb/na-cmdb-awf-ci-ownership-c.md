---
title: CI ownership agentic workflow
description: The CI ownership agentic workflow matches unowned CIs to group profiles. It proposes an owner for a reviewer to approve or reject.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/configuration-management-database-cmdb/na-cmdb-awf-ci-ownership-c.html
release: brazil
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-09-28"
reading_time_minutes: 1
keywords: [CI ownership, CI ownership recommender, group profile, assignment recommendation, CMDB, ServiceNow Otto for CMDB]
breadcrumb: [Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CI ownership agentic workflow

The CI ownership agentic workflow matches unowned CIs to group profiles. It proposes an owner for a reviewer to approve or reject.

Many organizations have configuration items \(CIs\) with no value in their owning-group field, such as **managed\_by\_group**. Unowned CIs are harder to route during incident and change processes, and harder to hold accountable during audits.

The CI ownership agentic workflow samples each group's existing CIs to build a plain-language profile of what that group owns. It then evaluates unowned CIs against those profiles to propose an owner. A reviewer approves or rejects each proposal from an assignment recommendation. Approving a proposal writes the proposed group onto the CI. For step-by-step instructions, see [Determine the owner of a CI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/configuration-management-database-cmdb/na-cmdb-awf-ci-ownership-use.md).

## Workflow stages

The workflow runs in three stages: a group profile builder, CI ownership inference, and assignment review. For details on each stage, the tables and system properties the workflow uses, and the CI ownership recommender's tools, see [CI ownership agentic workflow reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/configuration-management-database-cmdb/na-cmdb-awf-ci-ownership-ref.md).

## Activation

The CI ownership agentic workflow is part of the Feature Preview Program and is inactive by default. Its scheduled jobs ship inactive as well. Until an admin activates the workflow, its list controls for adding CIs to the queue and for approving or rejecting proposals don't appear at all. An admin can activate the workflow from the Feature Preview Program. For steps to activate the workflow, see [Activate the CI ownership agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/configuration-management-database-cmdb/activate-na-cmdb-awf-ci-ownership.md).

After activation, an admin or the CI ownership recommender's Activate Jobs tool can start the two scheduled jobs.

