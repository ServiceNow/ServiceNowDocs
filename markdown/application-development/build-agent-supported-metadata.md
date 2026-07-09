---
title: Supported metadata in Build Agent
description: Metadata and app file types that Build Agent can create and manage.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/build-agent-supported-metadata.html
release: australia
topic_type: reference
last_updated: "2026-06-25"
reading_time_minutes: 5
keywords: [metadata, app files, development workflow, compatibility, business rules, client scripts, forms, tables, workflows, UI components, scripted REST APIs, ATF tests, LDAP, data import, JavaScript modules, application menus, record insertion, Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Reference, Build Agent, Agentic development on the ServiceNow AI Platform, Building applications]
---

# Supported metadata in Build Agent

Metadata and app file types that Build Agent can create and manage.

For metadata types not listed in this table, query Build Agent directly.

**Important:** Build Agent only creates metadata supported by ServiceNow® Fluent. For more information, see [ServiceNow Fluent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-fluent.md). For the latest API reference, see [https://servicenow.github.io/sdk/](https://servicenow.github.io/sdk/)

<table id="table_supported-metadata"><thead><tr><th>

Metadata type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Automated Test Framework \(ATF\) tests

</td><td>

Automated test cases for validating application behavior.

</td></tr><tr><td>

Application menus and modules

</td><td>

Application menus are the top-level categories in the application navigator sidebar. Modules are the individual links within those categories and can link to tables, URLs, lists, or other platform resources. When Build Agent creates a new application with tables, it generates the corresponding navigator structure so users can access the application from the sidebar.

</td></tr><tr><td>

Assignment rules

</td><td>

Rules that automatically assign records to users or groups based on field conditions.

</td></tr><tr><td>

Business rules

</td><td>

Server-side scripts that run when records are displayed, inserted, updated, or deleted.

</td></tr><tr><td>

Choice lists

</td><td>

Field value options for select fields on forms and tables.

</td></tr><tr><td>

Client scripts

</td><td>

Scripts that run in the browser to control form behavior.

</td></tr><tr><td>

Client-side logic

</td><td>

Browser-based logic for controlling UI interactions and form behavior.

</td></tr><tr><td>

Condition builder and query conditions

</td><td>

Filter conditions used in business rules, workflows, and list views.

</td></tr><tr><td>

Configuration

</td><td>

System and application configuration settings.

</td></tr><tr><td>

Connection and credential alias

</td><td>

External system connections and stored credentials for authenticating with third-party services and platforms.

</td></tr><tr><td>

Custom AI agents

</td><td>

AI agents scoped to application data models, roles, and ACLs. For more information, see [Create agentic workflows, agents, and skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/create-custom-ai-agent.md).

</td></tr><tr><td>

Data policies

</td><td>

Rules that enforce field-level data requirements, such as mandatory or read-only constraints, across all interfaces including the API.

</td></tr><tr><td id="entry_data-import">

Data import pipeline

</td><td>

Build Agent creates the full data import pipeline: data sources, staging tables, import sets, and transform maps. Supported source types include CSV, Excel, JSON, XML, JDBC, LDAP, and REST. Specify the external data source, target table, and field mapping, and Build Agent generates the pipeline artifacts. The capability covers both one-time bulk loads and recurring scheduled imports.

</td></tr><tr><td>

Data lookup

</td><td>

Metadata definitions for data lookup fields that retrieve values from related tables or external sources.

</td></tr><tr><td>

Dictionary overrides

</td><td>

Field-level customizations that override base system dictionary entries without modifying the original.

</td></tr><tr><td>

Event registry configurations

</td><td>

Event definitions that trigger notifications, scripts, or other platform actions.

</td></tr><tr><td>

Field-level overrides

</td><td>

Attribute overrides applied at the field level on extended tables.

</td></tr><tr><td>

Flows

</td><td>

Automated processes built in Workflow Studio using a no-code or low-code interface.

</td></tr><tr><td>

Forms

</td><td>

Record views that define which fields are displayed and how they are arranged.

</td></tr><tr><td>

Inbound email actions

</td><td>

Rules that process incoming email and create or update records based on message content.

</td></tr><tr><td>

JavaScript modules

</td><td>

Build Agent creates JavaScript modules for organizing reusable server-side code within an application. Modules support standard import and export patterns and can reference server-side APIs. Use this pattern when multiple business rules, script includes, or other server-side scripts must share utility functions, constants, or logic without duplicating code.

</td></tr><tr><td>

LDAP server configurations

</td><td>

Build Agent creates LDAP server configurations and LDAP server URLs for connecting to external directory services such as Active Directory and OpenLDAP. LDAP server configurations include failover and load-balancing URL configurations and SSL settings. For importing records from the directory into ServiceNow tables, use a data import pipeline instead.

</td></tr><tr><td>

List controls

</td><td>

Settings that control list view behavior, including column display and row counts.

</td></tr><tr><td>

Playbooks

</td><td>

Representations of cross-enterprise business processes that organize tasks and activities into logical stages to guide users through a record lifecycle. Playbooks combine triggers that specify when to start, stages that group sequences of activities, and activities that define the automation and user-facing experience. Build Agent can create playbook configurations and activity definitions to help organizations digitize and standardize their business processes.To generate a playbook in Build Agent attach a file, such as an image, an XML, or a text description.

For more information on playbooks, see [Workflow Studio playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio-playbooks-landing.md).

</td></tr><tr><td>

Record insertion

</td><td>

Build Agent inserts data into any table, including tables that don't have a dedicated build skill. The functionality covers seed data, demo data, reference data, and configuration records. The same approach applies to creating metadata records on platform tables that Build Agent does not have a specialized skill for yet.

</td></tr><tr><td>

REST message and HTTP method

</td><td>

REST message definitions and HTTP method configurations for building API integrations and outbound integrations.

</td></tr><tr><td>

Scheduled jobs

</td><td>

Automated tasks that run on a defined schedule.

</td></tr><tr><td>

Script includes

</td><td>

Reusable server-side JavaScript libraries callable from other scripts.

</td></tr><tr><td>

Scripted REST APIs

</td><td>

Custom REST endpoints built with server-side scripting.

</td></tr><tr><td>

Security

</td><td>

Access control lists \(ACLs\), roles, and related security configurations.

</td></tr><tr><td>

Server-side logic

</td><td>

Scripts and business rules that execute on the server.

</td></tr><tr><td>

Service Catalog items and configurations

</td><td>

Catalog items, variables, and fulfillment flows for the Service Catalog.

</td></tr><tr><td>

Service Portal configuration, pages, and widgets

</td><td>

Portal structure, page definitions, and custom widgets.

</td></tr><tr><td>

Skills

</td><td>

Now Assist skills for AI-powered responses and actions.

</td></tr><tr><td>

Tables

</td><td>

Database tables that store application data, including fields, relationships, and access controls.

</td></tr><tr><td>

UI actions

</td><td>

Buttons, context menu items, and links that trigger scripts or navigation on forms and lists.

</td></tr><tr><td>

UI components

</td><td>

Reusable interface elements built with UI Builder.

</td></tr><tr><td>

UI pages

</td><td>

Custom pages built outside of standard form and list views.

</td></tr><tr><td>

UI policies

</td><td>

Client-side rules that show, hide, require, or lock fields based on conditions.

</td></tr><tr><td>

UI views

</td><td>

Named configurations of form layouts for different user contexts.

</td></tr><tr><td>

User criteria

</td><td>

Rules and criteria definitions for filtering and selecting users based on field conditions and organizational structures.

</td></tr><tr><td>

Workflows

</td><td>

Automated process sequences built in the legacy workflow editor.

</td></tr><tr><td>

Workspaces

</td><td>

Agent-facing interfaces built with configurable workspace components.

</td></tr></tbody>
</table>**Parent Topic:**[Build Agent reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/build-agent-reference-landing.md)

