---
title: User Criteria output
description: User Criteria output based on Available For and Not Available For values.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/employee-service-management/employee-experience-foundation/user-criteria-output.html
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Reference, Employee Center, Unified Employee Experience, Employee Service Management]
---

# User Criteria output

User Criteria output based on **Available For** and **Not Available For** values.

|Available For|Not Available For|Result|
|-------------|-----------------|------|
|Not defined|Not defined|Accessible to all users.|
|Not defined|Defined|Accessible to all users except the users falling under **Not Available For** criteria.|
|Defined|Not defined|Accessible only to the users falling under **Available For** criteria.|
|Defined|Defined|Accessible only to the users falling under **Available For** criteria.|
|Defined|Defined \(with some users falling under **Available For** criteria\)|Accessible to all users falling under **Available For** criteria and not falling under **Not Available For** criteria.|

**Parent Topic:**[Employee Center reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/employee-experience-foundation/emp-center-reference.md)

**Related topics**  


[Activity Configuration form]()

[Activity Configuration Detail form]()

[Browser Extension for Employee Center forms]()

[Connected Content form]()

[Default Employee Profile Header Configuration record]()

[Employee Center widgets]()

[Employee Profile form]()

[Employee Profile Header Configuration form]()

[Employee Profile portal configuration form]()

[Employee Profile upgrade scenarios]()

[Enhanced Requests Experience forms]()

[External Link form]()

[Featured Content form]()

[Footer form]()

[Footer Menus form]()

[Guided Self-Service reference]()

[Menu Item form]()

[Overview section form]()

[Portal notification configuration form]()

[Portal notification content form]()

[Quick Link form]()

[Standard banner and icon sizes]()

[Trigger conditions form]()

[Tab widget mapping form]()

[Taxonomy form]()

[Topic form]()

[To-do content form]()

[User Criteria form]()

