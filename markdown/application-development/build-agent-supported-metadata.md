---
title: Supported metadata in Build Agent
description: Metadata and app file types that Build Agent can create and manage. Ask Build Agent or Build Agent use this reference when determining compatibility for your development workflow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/build-agent-supported-metadata.html
release: zurich
topic_type: reference
last_updated: "2026-05-07"
reading_time_minutes: 4
keywords: [metadata, app files, development workflow, compatibility, business rules, client scripts, forms, tables, workflows, UI components, scripted REST APIs, ATF tests, LDAP, data import, JavaScript modules, application menus, record insertion, Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Reference, Build Agent, Agentic development on the ServiceNow AI Platform, Developing your application, Building applications]
---

# Supported metadata in Build Agent

Metadata and app file types that Build Agent can create and manage. Ask Build Agent or Build Agent use this reference when determining compatibility for your development workflow.

The best way to find out what metadata Build Agent supports is to ask it.

**Important:** Build Agent only creates metadata supported by ServiceNow® Fluent. For more information, see [ServiceNow Fluent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/servicenow-fluent.md). For the latest API reference, see [https://servicenow.github.io/sdk/](https://servicenow.github.io/sdk/)

|Metadata type|Description|
|-------------|-----------|
|Automated Test Framework \(ATF\) tests|Automated test cases for validating application behavior.|
|Application menus and modules|Application menus are the top-level categories in the application navigator sidebar. Modules are the individual links within those categories and can link to tables, URLs, lists, or other platform resources. When Build Agent creates a new application with tables, it generates the corresponding navigator structure so users can access the application from the sidebar.|
|Business rules|Server-side scripts that run when records are displayed, inserted, updated, or deleted.|
|Choice lists|Field value options for select fields on forms and tables.|
|Client scripts|Scripts that run in the browser to control form behavior.|
|Client-side logic|Browser-based logic for controlling UI interactions and form behavior.|
|Condition builder and query conditions|Filter conditions used in business rules, workflows, and list views.|
|Configuration|System and application configuration settings.|
|Custom AI agents|AI agents scoped to application data models, roles, and ACLs. For more information, see [Create agentic workflows, agents, and skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/create-custom-ai-agent.md).|
|Data import pipeline|Build Agent creates the full data import pipeline: data sources, staging tables, import sets, and transform maps. Supported source types include CSV, Excel, JSON, XML, JDBC, LDAP, and REST. Describe the external data that you need to import, the target table, and the field mapping, and Build Agent generates the pipeline artifacts. The capability covers both one-time bulk loads and recurring scheduled imports.|
|Dictionary overrides|Field-level customizations that override base system dictionary entries without modifying the original.|
|Event registry configurations|Event definitions that trigger notifications, scripts, or other platform actions.|
|Field-level overrides|Attribute overrides applied at the field level on extended tables.|
|Flows|Automated processes built in Workflow Studio using a no-code or low-code interface.|
|Forms|Record views that define which fields are displayed and how they are arranged.|
|Inbound email actions|Rules that process incoming email and create or update records based on message content.|
|JavaScript modules|Build Agent creates JavaScript modules for organizing reusable server-side code within an application. Modules support standard import and export patterns and can reference server-side APIs. Use this pattern when multiple business rules, script includes, or other server-side scripts need to share utility functions, constants, or logic without duplicating code.|
|LDAP server configurations|Build Agent creates LDAP server configurations and LDAP server URLs for connecting to external directory services such as Active Directory and OpenLDAP. This includes failover and load-balancing URL configurations and SSL settings. For importing records from the directory into ServiceNow tables, use a data import pipeline instead.|
|List controls|Settings that control list view behavior, including column display and row counts.|
|Record insertion|Build Agent inserts data into any table, including tables that do not have a dedicated build skill. The functionality covers seed data, demo data, reference data, and configuration records. The same approach applies to creating metadata records on platform tables that Build Agent does not have a specialized skill for yet.|
|Scheduled jobs|Automated tasks that run on a defined schedule.|
|Script includes|Reusable server-side JavaScript libraries callable from other scripts.|
|Scripted REST APIs|Custom REST endpoints built with server-side scripting.|
|Security|Access control lists \(ACLs\), roles, and related security configurations.|
|Server-side logic|Scripts and business rules that execute on the server.|
|Service Catalog items and configurations|Catalog items, variables, and fulfillment flows for the Service Catalog.|
|Service Portal configuration, pages, and widgets|Portal structure, page definitions, and custom widgets.|
|Skills|Now Assist skills for AI-powered responses and actions.|
|Tables|Database tables that store application data, including fields, relationships, and access controls.|
|UI actions|Buttons, context menu items, and links that trigger scripts or navigation on forms and lists.|
|UI components|Reusable interface elements built with UI Builder.|
|UI pages|Custom pages built outside of standard form and list views.|
|UI policies|Client-side rules that show, hide, require, or lock fields based on conditions.|
|UI views|Named configurations of form layouts for different user contexts.|
|Workflows|Automated process sequences built in the legacy workflow editor.|
|Workspaces|Agent-facing interfaces built with configurable workspace components.|

**Parent Topic:**[Build Agent reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/build-agent-reference-landing.md)

