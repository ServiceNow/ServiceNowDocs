---
title: Certification templates
description: Certification templates can define attributes, relationships, and reference field values that indicate what a record is expected to contain.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [CMDB Compliance, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Certification templates

Certification templates can define attributes, relationships, and reference field values that indicate what a record is expected to contain.

These values are used to perform audits on ServiceNow records. The certification filter selected in the template identifies the table and records to audit, and the template conditions set the expected state for those records. The type of audit you create determines which tables and template conditions are available.

Users with the certification\_admin role can create, update, and delete templates. Users with the certification role can view template versions.

## Certification template audit types

When you create a template, ServiceNow assigns an Audit type that determines which tables and conditions are available in the certification template. This value is based on the application from which the template is created. Each application lists only the templates with the associated type.

## Available Condition Builders

The available condition builders for each audit type:

-   Compliance: Runs audits on any set of ServiceNow records, not only configuration items \(CI\). This audit type provides the following types of conditions for any ServiceNow table:
    -   Attribute: Sets conditions for the attributes of the records.
    -   Related List: Runs audits on records in tables that reference the table defined in the template.
-   Architecture Compliance: Defines the following types of conditions for tables that extend the Configuration Item \[cmdb\_ci\] table.
    -   Attribute: Sets conditions for physical attributes of CIs, such as memory or disk size.
    -   Related List: Runs audits on records in tables that reference the table defined in the template.
-   Desired State: Defines the following types of conditions for tables that extend the Configuration Item \[cmdb\_ci\] table.
    -   Attribute: Sets conditions for physical attributes of CIs, such as memory or disk size.
    -   CI relationship: Defines the relationships these CIs have with other CIs. An example of a relationship is a business service, such as Outlook Web Access, that depends on a server.
    -   User relationship: Defines the user who reviewed the log records. The only operator available with this condition builder.
    -   Group relationship: Defines user groups who backed up this CI. The only operator available with this condition builder.
    -   Related List: Runs audits on records in tables that point toward the table defined in the template.

## Certification Template Record List

The default Templates list displays only the active version of each template, but you can update the breadcrumbs to display all template versions.

-   Default Templates List: The default Templates list displays only the active version of each template, filtered by **Audit type**.
-   All Template Versions: To view all template versions for an audit type, click the arrow before **Active=true** to remove that condition from the breadcrumbs. ![Breadcrumbs.](../image/DesiredStateBreadcrumbs.png)

