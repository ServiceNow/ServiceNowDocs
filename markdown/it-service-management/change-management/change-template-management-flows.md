---
title: Change template management flows
description: Change template management flows trigger and manage steps for the template proposal, modification, and retirement processes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/change-management/change-template-management-flows.html
release: australia
product: Change Management
classification: change-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Create and propose a change template, Create a Change model, Configure, Change Management, IT Service Management]
---

# Change template management flows

Change template management flows trigger and manage steps for the template proposal, modification, and retirement processes.

Administrators can configure flows to trigger and manage the steps in the life cycle of a change template. These flows evaluate the predefined conditions and trigger requested actions to complete the modification or retirement actions for selected change templates.

Change template management uses the following flows:

-   The STTRM Template Publish Approval flow helps manage the template proposal and publishing actions in the application. The flow runs when you send a template in the Proposed state for review.
-   The STTRM Template Retire Approval flow helps manage template retirement actions. The flow runs when you retire templates and the selected templates move to the **Pending Retirement** state.


The approvers for both flows are the users and groups defined in the Template Management section of the change model.

**Parent Topic:**[Create and propose a change template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/create-change-template.md)

