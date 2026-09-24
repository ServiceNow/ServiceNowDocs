---
title: Process Mining templates
description: Templates let you save a reusable Process Mining project configuration and reapply it across your organization, instead of configuring each new project from scratch.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/process-mining/pm\_templates.html
release: brazil
product: Process Mining
classification: process-mining
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [process mining, templates, template mapping, governance]
breadcrumb: [Use, Process Mining, Platform Analytics]
---

# Process Mining templates

Templates let you save a reusable Process Mining project configuration and reapply it across your organization, instead of configuring each new project from scratch.

Before templates, only one default project configuration could exist per table. And that configuration couldn't be safely customized because Process Mining updates could overwrite it.

Templates remove both limits:

-   You can have multiple templates for the same table, each customized for a different use case.
-   Your customizations are never at risk of being overwritten by product updates.

## Key benefits

-   Multiple templates per table, so a single table like `incident` can support several distinct use cases instead of one generic configuration.
-   A safe way to customize configuration, since your custom templates are never overwritten by product updates.
-   Centralized management, so you can see and govern every template from one page instead of hunting through project records.

## How it works

Every template is one of two types:

-   **Standard**: Shared with everyone in the instance. Standard templates are read-only. Sharing settings can't be changed and the template can't be edited once created. Standard templates can't have filter conditions on their entities.
-   **Custom**: Visible only to the users or groups it's shared with, though anyone with the power user role or higher can see all custom templates. Custom templates can have filter conditions on their entities, which is what makes them suitable for the region-specific or team-specific use case.

Every template that ships with a Process Mining content pack is a Standard template. Shipped templates are additionally marked as content pack templates, which is what makes them read-only and protects your instance from losing customizations during an upgrade.

Creating a template has the following conditions:

-   Only power users or higher can create or delete Standard templates. Analysts can view them.
-   Analysts and above can create Custom templates.
-   An analyst never sees the type selector when creating a template. The type is always set to Custom automatically.

-   **[Create a Process Mining template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/process-mining/create-template.md)**  
Create a Process Mining template to reuse a Process Mining project configuration and reapply it across your organization without the need of creating it everytime.
-   **[Save a project as a template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/process-mining/save_project_as_template.md)**  
Save a project you have tested and refined as a template, so anyone can reuse its configuration for new projects.
-   **[Map a template to a table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/process-mining/map_template_to_table.md)**  
Map a template to a table so that launching Process Mining from a Performance Analytics indicator or a list view from any workspace uses the right template.
-   **[Edit a template mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/process-mining/edit-temp.md)**  
Edit a Process Mining template mapping to make updates as required.

**Parent Topic:**[Using Process Mining](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/process-mining/use-process-mining.md)

**Related topics**  


[Save a project as a template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/process-mining/save_project_as_template.md)

[Map a template to a table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/process-mining/map_template_to_table.md)

