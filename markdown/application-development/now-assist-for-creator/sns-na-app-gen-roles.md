---
title: App generation roles
description: Assign the correct role before using the Now Assist for Creator app generation skill. The role you need depends on whether you are creating or editing an application.The administrator role grants access to all system features, functions, and data, regardless of security constraints. For app generation, assign this role only when no more specialized role is available.
locale: en-US
release: australia
product: Now Assist for Creator
classification: now-assist-for-creator
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [agentic ai, app gen, app generation, now assist, application generation, app creation, application creation, servicenow studio, generative ai, agentic ai]
breadcrumb: [Reference, App generation, Use generative AI, Now Assist for Creator, Vibe coding and AI app development on the ServiceNow AI Platform, Building applications]
---

# App generation roles

Assign the correct role before using the Now Assist for Creator app generation skill. The role you need depends on whether you are creating or editing an application.

To edit \(not create\) applications using app generation, assign the delegated\_developer or now\_assist\_panel\_user role. For more information, see [Delegated development and deployment](../../applications/concept/c_DelegatedDevelopment.md).

**Parent Topic:**[App generation reference](../concept/sns-app-gen-reference-landing.md)

## Administrator \[admin\] role for app generation

The administrator role grants access to all system features, functions, and data, regardless of security constraints. For app generation, assign this role only when no more specialized role is available.

### Contains Roles

List of roles contained within the role.

-   sn\_employee.admin
-   taxonomy\_admin
-   sn\_ace.ace\_user
-   nlu\_admin
-   sn\_hr\_sp.esc\_admin
-   sn\_templated\_snip.template\_snippet\_admin

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

Grant the admin role only when no more specialized role is available. Assigning the admin role unnecessarily expands user access beyond what the task requires.

