---
title: Content access filtering
description: Restrict access to subsets of playbook content by pairing a content definition with a filtering rule.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/build-workflows/workflow-studio/content-access-filtering-playbooks.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [Managing playbook permissions, Configure, Playbooks, Workflow Studio, Build workflows]
---

# Content access filtering

Restrict access to subsets of playbook content by pairing a content definition with a filtering rule.

Content access filtering restricts what a user sees at design time. Use it when a role grants broader access than specific users should have. For example, the pd\_author role allows users to edit any playbook and use any activity definition. You can grant a user playbook.write, which only lets them edit playbooks and use activity definitions that have been granted to them through content access filtering.

Filtering takes two records. A content definition describes a set of content. A content filtering rule names the roles that reach the content in that definition. Users need both the role named in the rule and a role that grants design-time access.

Filter on three axes. Filter by activity definition to control which activities a user can add to a playbook. Filter by playbook type to control which playbooks a user can see. Filter by resource tag to refine either.

**Note:** Assign the playbook.write role rather than pd\_author to users who should see filtered content. The pd\_author role grants access to all playbooks and all activity definitions, which overrides the restriction.

## Default content definition

One content definition ships by default: Playbooks - All Activity Definitions. It covers every activity definition, and two default filtering rules point at it. One grants access to users with the delegated\_developer role. The other grants access to users with the playbook.activity\_def\_read role.

## Content definitions

A content definition specifies a type of resource. Create a definition that covers an entire resource, or use the condition builder to narrow it.

A definition on the activity definition table with a condition matching Guided Decision in the name or package covers only those activity definitions. A definition on the playbook table with a condition on playbook type covers only playbooks of that type.

Refine a definition further with resource tags. For more information, see [Configure content filtering definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/configure-content-definitions.md).

## Content filtering rules

A content filtering rule specifies the role a user must have to reach the content in a content definition. Each rule associates one or more roles with a single content definition.

To create one, see [Configure content filtering rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/configure-content-filtering-rules-playbook.md).

## Filtering by playbook type

Filtering on playbook type gives a group of users access to one category of playbook and no others. A business unit that owns its own playbook types can be restricted to those types.

Create a content definition on the playbook table conditioned on playbook type, then a filtering rule that names a role for the group. For the procedure, see [Restrict access by playbook type](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/restrict-playbook-access-by-type.md).

## Filtering by activity definition

Filtering on activity definition controls which activities a user can add when building a playbook.

To restrict a single activity definition to named roles instead, set required roles on the definition. Required roles override content access filtering, so a user without the required role can't use the activity definition even when a filtering rule grants access to it. For the procedure, see [Restrict access to an activity definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/restrict-access-to-activity-definition.md).

## Read-only playbooks

A user who can't reach every activity definition in a playbook gets a read-only view of that playbook. The same applies to a user without write access to the process definition.

Read-only isn't necessarily a permissions problem. A form also displays as read-only when the activity has no declarative action that requires form fields. An editable form with no way to submit it is not useful.

If a playbook appears read-only, confirm whether the user lacks content access before changing filtering rules.

|Content|With access|Without access|
|-------|-----------|--------------|
|Activity definition|Visible and selectable when building a playbook. Can be copied and modified.|Hidden and not selectable. Playbooks that contain it are read-only.|

## Related permissions

Content access filtering is one of four ways to control playbook access. For the others and how they interact, see [Managing playbook permissions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/playbook-permissions.md).

Access control rules operate as a separate layer and can block content that a filtering rule grants. For more information, see [Access control rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/access-control-rules-playbooks.md).

-   **[Configure content filtering definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/configure-content-definitions.md)**  
Create a content definition that describes a set of content a filtering rule grants access to.
-   **[Configure content filtering rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/configure-content-filtering-rules-playbook.md)**  
Create a rule that grants a role access to the content in a content definition.
-   **[Restrict access by playbook type](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/restrict-playbook-access-by-type.md)**  
Use content access filtering to give a group of users access only to playbooks of a specific type.
-   **[Restrict access to an activity definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/restrict-access-to-activity-definition.md)**  
Limit which users can add a specific activity definition to a playbook.

**Parent Topic:**[Managing playbook permissions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/playbook-permissions.md)

