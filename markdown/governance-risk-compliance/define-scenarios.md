---
title: Create a scenario and link it to an event
description: Create a scenario in the Operational Resilience application so that you can associate it with an event and assess its impact on your business services.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/define-scenarios.html
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Completing general administrative tasks, Configure, Operational Resilience, Governance, Risk, and Compliance]
---

# Create a scenario and link it to an event

Create a scenario in the Operational Resilience application so that you can associate it with an event and assess its impact on your business services.

## Before you begin

Role required: sn\_oper\_res.admin

## About this task

A scenario helps you to determine the risks that are applicable to your business. If you have the sn\_oper\_res.admin role, you can create a scenario in the Operational Resilience application. You can use a scenario to test how an event can impact your organization.

## Procedure

1.  Navigate to **All** &gt; **Operational Resilience** &gt; **Admin** &gt; **Scenarios**.

2.  Click **New**.

    The sample configuration for the Scenario New record form is shown in the following example.

    \[Omitted image "new-scenario-active.png"\] Alt text: Sample configuration for the Scenario New record form.

3.  On the form, fill in the fields.

    For the description of the field values, see [Scenario New record form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/scenario-reference.md).

4.  Click **Submit**.

    You have associated an event with a scenario. The Events related list displays the associated events as shown in the following example.

    \[Omitted image "scenario-associated-with-an-event.png"\] Alt text: Events that are associated with a scenario.

    The order for the event is tied to the scenario and it is auto-filled by default in the related list.


