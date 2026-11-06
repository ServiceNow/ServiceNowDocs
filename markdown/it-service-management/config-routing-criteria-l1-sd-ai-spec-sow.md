---
title: Configure routing criteria
description: Add, edit, and delete the routing criteria that determine which incidents the L1 IT Service Desk AI Specialist handles.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/config-routing-criteria-l1-sd-ai-spec-sow.html
release: australia
topic_type: task
last_updated: "2026-10-01"
reading_time_minutes: 1
keywords: [routing criteria, routing decision]
breadcrumb: [Configure, L1 IT Service Desk AI Specialist, IT Service Management]
---

# Configure routing criteria

Add, edit, and delete the routing criteria that determine which incidents the L1 IT Service Desk AI Specialist handles.

## Before you begin

Role required: sn\_itsm\_common.sn\_service\_desk\_manager

## About this task

A routing criterion is a record generated from a reviewed evaluation. It defines which incidents within a theme the L1 IT Service Desk AI Specialist resolves and which it routes to a human. When an incident is assigned to the L1 IT Service Desk AI Specialist, it checks the incident against the routing criteria for the matching theme or use case.

If the incident matches, the criteria determine whether the L1 IT Service Desk AI Specialist continues to resolve it or routes it to a TSE or another L1 agent.

If no routing criteria match, the L1 IT Service Desk AI Specialist uses the default routing decision. For how the default routing decision is determined, see [Triage and diagnose](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/config-tasks-l1-sd-ai-spec-sow.md) fields.

## Procedure

1.  Navigate to **All** &gt; **Service Operations Workspace**.

2.  On the Homepage, in the **L1 Service Desk AI Specialist** card, select **View details**.

3.  Select **Tasks**.

4.  In the **Triage and diagnose** section, find **Routing criteria**.

    The list shows the criteria for the task you're configuring using pills. Each pill shows the name, and when selected, you can view the description and routing decision.

5.  Add, edit, or delete a routing criterion.

    -   To add a criterion, select **Add criteria** and complete the fields. It will automatically save and will be active by default.

        |Field|Description|
        |-----|-----------|
        |Name|The name of the criterion. This field is required.|
        |Routing instructions for LLM|Instructions that describe the incidents this criterion matches. This field is required.|
        |Routing decision|Select what the L1 IT Service Desk AI Specialist does with an incident that matches the criterion: **Attempt resolution** or **Reassign**.|

    -   To edit a criterion, select the pill and change the fields. It will automatically save.
    -   To delete a criteria, select the pill, select **Delete**, and confirm the deletion.

