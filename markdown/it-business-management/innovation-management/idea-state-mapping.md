---
title: Idea state mapping
description: Map your idea states to the Universal Request states to provide a better user experience during the idea state transition and to track the progress of the idea.
locale: en-US
release: australia
product: Innovation Management
classification: innovation-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integrating Innovation Management with Universal Request, Innovation Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Idea state mapping

Map your idea states to the Universal Request states to provide a better user experience during the idea state transition and to track the progress of the idea.

## Before you begin

Role required: admin

## About this task

Mapping the states of the idea to the universal request state ensures that the status of idea is also reflected on the state of universal request. As the idea moves through different stages of the life cycle, the state of the universal request also gets updated to reflect the change.

For example, consider a universal request that has an idea attached to it as a primary ticket. When the state of idea changes from **Submitted** to **Need more information**, the state of the universal ticket state is also updated to **Awaiting Response**.

The following image is an example of a default state mapping. The **Submitted**, **Under Review**, **In Backlog**, **Planned** and **In Development** states of an idea are mapped to **In Progress** state of a Universal Request.

The following table lists the default mapping of different idea states with the universal request states.

|Idea state|Universal Request state|
|----------|-----------------------|
|Submitted|In Progress|
|Under Review|In Progress|
|In Backlog|In Progress|
|Planned|In Progress|
|In Development|In Progress|
|Unlikely to implement|Closed|
|Duplicate|Closed|
|Already exists|Closed|
|Completed|Closed|
|Need more information|Awaiting Response|

## Procedure

1.  Navigate to **All** &gt; **Universal Request** &gt; **Administration** &gt; **State Mapping**.

2.  Select **New**.

3.  On the form, fill in the fields.

    For more information, see [State mapping form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/universal-request-for-hr-service-delivery/ur-state-mapping-form.md).


**Parent Topic:**[Integrating Innovation Management with Universal Request](../concept/universal-req-idea-mgmt.md)

