---
title: App generation roles
description: Assign the correct role before using the ServiceNow Otto for Creator app generation skill. The role you need depends on whether you are creating or editing an application.The administrator role grants access to all system features, functions, and data, regardless of security constraints. For app generation, assign this role only when no more specialized role is available.Create applications through a conversation with generative AI.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/servicenow-studio-classic/sns-na-app-gen-roles.html
release: zurich
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: reference
last_updated: "2026-07-28"
reading_time_minutes: 1
keywords: [agentic ai, app gen, app generation, now assist, application generation, app creation, application creation, servicenow studio, generative ai, agentic ai, agentic ai, app gen, app generation, now assist, application generation, app creation, application creation, servicenow studio, generative ai]
breadcrumb: [Reference, App generation, AI tools and files, Use, ServiceNow Studio, Developing your application, Building applications]
---

# App generation roles

Assign the correct role before using the ServiceNow Otto for Creator app generation skill. The role you need depends on whether you are creating or editing an application.

To edit \(not create\) applications using app generation, assign the delegated\_developer or now\_assist\_panel\_user role. For more information, see [Exploring Delegated Development](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/delegated-development-and-deployment/c_DelegatedDevelopment.md).

**Parent Topic:**[Now Assist for app generation in ServiceNow Studio reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/servicenow-studio-classic/sns-app-gen-reference-landing.md)

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

## Now Assist Creator \[now.assist.creator\] role for Now Assist for app generation in ServiceNow Studio

Create applications through a conversation with generative AI.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

None.

