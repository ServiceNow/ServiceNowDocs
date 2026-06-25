---
title: Roles and permissions matrix
description: Learn about the roles required to access each UI Generation feature.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/now-assist-for-creator/roles-and-permissions-matrix.html
release: australia
product: Now Assist for Creator
classification: now-assist-for-creator
topic_type: reference
last_updated: "2026-06-25"
reading_time_minutes: 1
breadcrumb: [Reference, UI generation, Use generative AI, Now Assist for Creator, Agentic development on the ServiceNow AI Platform, Building applications]
---

# Roles and permissions matrix

Learn about the roles required to access each UI Generation feature.

## UI Generation roles and permissions

The ui\_builder\_admin role is the primary role for using Now Assist UI Generation skills.

|Feature|ui\_builder\_admin|workspace\_admin|admin|
|-------|------------------|----------------|-----|
|Experience Generation \(AI-Generated\)|✓|–|–|
|Client Script Summarization|✓|–|–|
|Data Binding Generation|✓|–|–|
|UI Builder Agent \(Learn / Understand / Accelerate\)|✓|–|–|
|Module Generation|✓|✓|–|
|View AI-Generated Indicator Badge|✓|✓|✓|
|Manage UI Generation System Properties|–|–|✓|
|Assign ui\_builder\_admin Role|–|–|✓|

## Role descriptions

-   **ui\_builder\_admin**

    Primary role for UI Generation. Contains ui\_interaction\_admin, canvas\_user, and workspace\_admin as sub-roles.

    For more information, see [UI generation roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/now-assist-for-creator/ui-generation-roles.md) and [Grant UI Builder admin role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/now-assist-for-creator/grant-ui-builder-admin-role.md).

-   **workspace\_admin**

    Allows workspace-level configuration and management within UI Builder.

-   **admin**

    Full instance administration, including system properties management and role assignment.


**Parent Topic:**[UI generation reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/now-assist-for-creator/ui-generation-reference.md)

