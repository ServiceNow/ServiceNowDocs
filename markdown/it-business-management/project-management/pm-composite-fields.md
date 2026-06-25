---
title: Composite Fields
description: A composite field combines information from two fields in a table to form a single field.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/project-management/pm-composite-fields.html
release: australia
product: Project Management
classification: project-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Basics of Project Management, Exploring Project Management, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Composite Fields

A composite field combines information from two fields in a table to form a single field.

For example, the **Task** field on the Project Tasks list displays the short description and the project task number. The short description appears above the project task number. The project task number appears and is a link to the Project Task form.

\[Omitted image "CompositeField.png"\] Alt text: Composite field

## Use a composite field

-   Editing a composite field changes the short description. Editing the short description changes the composite field.
-   Sorting on a composite field is based only on the short description and not the number.
-   Searching on a composite field is enabled for both the short description and the number:
    -   To search by the number using the list header, enter an asterisk \(\*\) before the search term. For example, \*PRJTASK0010016.
    -   To search by the number using the filter, create a condition similar to: \[Task\] \[contains\] \[PRJTASK0010016\].

**Parent Topic:**[Basics of Project Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-management/c_ProjectTasks.md)

**Related topics**  


[Parent-child rollup task calculations]()

[Project tasks]()

[Schedule conflicts between project tasks]()

[Change requests and project tasks]()

[Project task checklists]()

[Task resources]()

[Project and project task states]()

[Cost plan breakdown]()

[Actual project costs]()

[Types of external dependencies]()

[Project and portfolio funding]()

