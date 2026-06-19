---
title: Case and account escalation process
description: The case and account escalation process follows several steps from request to completion.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/customer-service-management/case-escalation-process.html
release: zurich
product: Customer Service Management
classification: customer-service-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Case and account escalation, Administer, Customer Service Management]
---

# Case and account escalation process

The case and account escalation process follows several steps from request to completion.

1.  Your users with the escalation requester role request an escalation for a case or account. As part of the request, you can provide the following information:
    -   The reason for the request
    -   Justification for the escalation
    -   The [escalation severity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/administer-case-account-escalation.md)
    -   The [escalation template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/administer-case-account-escalation.md)
    -   The watch list for the escalation
2.  If approval is required for an escalation request, approvers from the selected approval group review and approve or reject the escalation request. The chosen approval subflow then updates the approval status accordingly.
3.  Following approval, the agent manages the escalation as it progresses using the [escalation form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/case-escalation-form.md). For example, the agent can add users to the watch list and update the escalation trend.

    **Note:** Updates to the escalation form send email notifications to the current user and to users on the watch list.

4.  When the issue has been resolved, your users with the de-escalation requester role can de-escalate a case or an account.

