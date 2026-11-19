---
title: Filter resources in Dispatcher Workspace
description: You can create your own advanced resource filters in Dispatcher Workspace to make complex filtering easy.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/field-service-scheduling/advanced-filtering-dw.html
release: brazil
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Advanced Filtering, Using Dispatcher Workspace, Assigning tasks from Dispatcher Workspace, Scheduling and dispatching, Use, Field Service Management]
---

# Filter resources in Dispatcher Workspace

You can create your own advanced resource filters in Dispatcher Workspace to make complex filtering easy.

## Before you begin

\[Omitted video\] Description: Filter resources in Dispatcher Workspace

Role required: wm\_dispatcher.

## Procedure

1.  Navigate to **Field Service** &gt; **Dispatching** &gt; **Dispatcher Workspace**.

2.  Select **Dispatcher Workspace**.

3.  Select **Filter resources**.

4.  Select **+ Advanced filters**.

5.  Select **Crews** if this is a new crew filter.

6.  Select a filter from the **Use existing filter** drop-down menu if you’re changing an existing filter.

7.  Add or edit the filter that you want to apply.

    |Field|Description|
    |-----|-----------|
    |**User · agentgroup\_user**|Filter by the users who are members of the territory's assignment groups. These are the territory's regular agents.|
    |**User · terrmember\_user**|Filter by the users added to the territory individually, outside its assignment groups. These are agents assigned to the territory temporarily.|
    |**Skill**|Filter by the skills of users.|
    |**Crew · crewgroup\_crew**|Filter by the crews in the territory's assignment groups. These are the territory's regular crews.|
    |**Crew · terrmember\_crew**|Filter by the crews added to the territory individually, outside its assignment groups. These are crews assigned to the territory temporarily.|
    |**Skills**|Filter by the skills of crews.|
    |**Equipment name**|Filter by the name of the equipment.|
    |**Category**|Filter by the equipment category.|
    |**Assignment Group**|Filter by the contractor's group name. The field is labeled Assignment Group, but it filters contractors.|

8.  Choose from the following:

    -   Select **Save Filter** to name the filter and save it.
    -   Select **Apply** to run the filter. Select the filter again to clear the filter from Dispatcher Workspace.
    -   Select the more actions icon \[Omitted image "more\_action\_triangle.png"\] Alt text: more actions, then **Update** to overwrite the filter if you were changing an existing filter. You can't update administrator-created filters.
    -   Select the more actions icon \[Omitted image "more\_action\_triangle.png"\] Alt text: more actions, then **Save as new** to save a new filter if you were changing an existing filter.
    If you saved the filter, you can select the filter from the **Advanced filters** drop-down menu. **Filter resources** changes to **Temporary filter** when a filter is applied.


