---
title: Case action status
description: The case action status feature displays the status of cases in the Case list. With this feature, customer service agents can easily identify cases that need attention.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/customer-service-case-action-status.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure case management, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Case action status

The case action status feature displays the status of cases in the Case list. With this feature, customer service agents can easily identify cases that need attention.

The case action status feature provides visual indicators in the **Action status** column on the My Cases and My Open lists to highlight case status. In addition to the colored indicators, the **Action status** column also displays a brief status message.

\[Omitted image "case-action-status-csm-config-workspace.png"\] Alt text: The Action status column on the Case list displays color-coded indicators and messages for cases that are blocked or need attention.

## Actionable case flows

The case action status feature uses [actionable case flows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/case-action-status-triggers.md) to automatically determine the action status for customer service cases. These flows create and resolve blocking tasks for different case-related actions and automatically update the action status indicators. Certain agent actions trigger these case flows, which in turn create and resolve the blocking tasks.

Customer service agents and managers can also manually set the action status for cases by enabling the **Needs Attention** field on the Case form.

## Blocking tasks

A [blocking task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/case-action-status-blocking-tasks.md) is something that prevents an agent from making progress toward case resolution. For example, a case might have one or more open related case task records or be waiting for customer feedback.

Certain agent actions trigger case flows that create and resolve blocking tasks for customer service cases. These tasks determine the case action status. Additionally, there are actions that resolve these blocking tasks, such as the customer responding to an agent’s question or an internal user resolving a problem task. For more information, see .

**Related topics**  


[Case action status](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/case-action-status-csm-workspace.md)

[Configure case action status](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/configure-case-action-status.md)

[Activate Case Action Status](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/activate-case-action-status.md)

