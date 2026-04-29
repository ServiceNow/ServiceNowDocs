---
title: App generation supported metadata
description: App generation creates seven metadata types, including tables, roles, and record producers. Use this reference to understand what each metadata type does and how app generation uses it.
locale: en-US
release: australia
product: Now Assist for Creator
classification: now-assist-for-creator
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [agentic ai, app gen, app generation, now assist, application generation, app creation, application creation, servicenow studio, generative ai]
breadcrumb: [Reference, App generation, Use generative AI, Now Assist for Creator, Vibe coding and AI app development on the ServiceNow AI Platform, Building applications]
---

# App generation supported metadata

App generation creates seven metadata types, including tables, roles, and record producers. Use this reference to understand what each metadata type does and how app generation uses it.

When you generate an application, app generation creates the following metadata types.

<table id="table_skd_wwj_w1c"><thead><tr><th>

Label

</th><th>

Name

</th><th>

Usage

</th></tr></thead><tbody><tr><td>

[Access control list \(ACL\)](https://www.servicenow.com/docs/access?context=exploring-access-control-list&version=australia&pubname=australia-platform-security&ft:locale=en-US)

</td><td>

sys\_security\_acl

</td><td>

ACLs manage role-based access control for the application:-   Rules that define role access to resources and permitted operations
-   ACLs that can be applied at the field or table level

</td></tr><tr><td>

[Flows](https://www.servicenow.com/docs/access?context=exploring-flows&version=australia&pubname=australia-build-workflows&ft:locale=en-US)

</td><td>

sys\_hub\_flow

</td><td>

Flows automate a repeatable, multi-step process.

</td></tr><tr><td>

[Form](https://www.servicenow.com/docs/access?context=c_UsingForms&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US)

</td><td>

sys\_ui\_form

</td><td>

Interface that enables users to submit data to create or update records in a table

</td></tr><tr><td>

[Record producer](https://www.servicenow.com/docs/access?context=c_RecordProducer&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)

</td><td>

sc\_cat\_item\_producer

</td><td>

Type of form that enables users to enter information that generates a task-based record

</td></tr><tr><td>

[Role](https://www.servicenow.com/docs/access?context=ua-creating-roles&version=australia&pubname=australia-platform-administration&ft:locale=en-US)

</td><td>

sys\_user\_role

</td><td>

Set of permissions that are assigned to users and groups

</td></tr><tr><td>

[Table](https://www.servicenow.com/docs/access?context=c_TableAdministration&version=australia&pubname=australia-platform-administration&ft:locale=en-US)

</td><td>

sys\_db\_object

</td><td>

Tables organize data into rows and columns for easy reference:-   Collection of records with information
-   Records contain fields that store data for the application
-   Each record corresponds to a table row, and each field on a record corresponds to a table column

</td></tr><tr><td>

[Workspace Builder](../../workspace-builder/concept/workspace-builder-landing.md)

</td><td>

sys\_ux\_page\_registry

</td><td>

A targeted experience for an application that includes data visualizations and other user experience components to allow a user to interact with an application.

</td></tr></tbody>
</table>**Parent Topic:**[App generation reference](../concept/sns-app-gen-reference-landing.md)

