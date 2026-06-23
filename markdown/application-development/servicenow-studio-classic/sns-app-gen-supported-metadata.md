---
title: Now Assist for app generation supported metadata
description: Now Assist for app generation supports metadata including tables, roles, and record producers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/application-development/servicenow-studio-classic/sns-app-gen-supported-metadata.html
release: yokohama
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: reference
last_updated: "2025-04-07"
reading_time_minutes: 1
breadcrumb: [Now Assist for app generation in ServiceNow Studio reference, Now Assist for app generation in ServiceNow Studio, Using ServiceNow Studio, Building applications with ServiceNow Studio, Developing your application, Building applications]
---

# Now Assist for app generation supported metadata

Now Assist for app generation supports metadata including tables, roles, and record producers.

App generation generates the following metadata.

<table id="table_skd_wwj_w1c"><thead><tr><th>

Label

</th><th>

Name

</th><th>

Usage

</th></tr></thead><tbody><tr><td>

[Access control list \(ACL\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-security/access-control/exploring-access-control-list.md)

</td><td>

sys\_security\_acl

</td><td>

ACLs manage role-based access control for the application:-   Rules that define role access to resources and permitted operations
-   ACLs that can be applied at the field or table level

</td></tr><tr><td>

[Flows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/build-workflows/workflow-studio/exploring-flows.md) \(available in the Yokohama Patch 3 release - May 2025\)

</td><td>

sys\_hub\_flow

</td><td>

Flows automate a repeatable, multi-step process.

</td></tr><tr><td>

[Form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-user-interface/configure-user-experiences/c_UsingForms.md)

</td><td>

sys\_ui\_form

</td><td>

Interface that enables users to submit data to create or update records in a table

</td></tr><tr><td>

[Record producer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/service-catalog/c_RecordProducer.md)

</td><td>

sc\_cat\_item\_producer

</td><td>

Type of form that enables users to enter information that generates a task-based record

</td></tr><tr><td>

[Role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/user-administration/ua-creating-roles.md)

</td><td>

sys\_user\_role

</td><td>

Set of permissions that are assigned to users and groups

</td></tr><tr><td>

[Table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/table-administration-and-data-management/c_TableAdministration.md)

</td><td>

sys\_db\_object

</td><td>

Tables organize data into rows and columns for easy reference:-   Collection of records with information
-   Records contain fields that store data for the application
-   Each record corresponds to a table row, and each field on a record corresponds to a table column

</td></tr><tr><td>

[Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/workspace-builder/add-workspace.md) \(available in the Yokohama Patch 3 release - May 2025\)

</td><td>

sys\_ux\_page\_registry

</td><td>

A targeted experience for an application that includes data visualizations and other user experience components to allow a user to interact with an application.

</td></tr></tbody>
</table>**Parent Topic:**[Now Assist for app generation in ServiceNow Studio reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/servicenow-studio-classic/sns-app-gen-reference-landing.md)

