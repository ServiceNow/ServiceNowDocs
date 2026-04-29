---
title: Tables and data models
description: Tables are the foundation of ServiceNow applications, as they define what data you're storing and how it's structured. Each table consists of fields \(columns\) that hold specific data types such as strings, dates, numbers, and references to other tables.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Build your first app, Getting Started guide for developers, Building applications]
---

# Tables and data models

Tables are the foundation of ServiceNow applications, as they define what data you're storing and how it's structured. Each table consists of fields \(columns\) that hold specific data types such as strings, dates, numbers, and references to other tables.

When you create a table, ServiceNow automatically generates the underlying database structure, forms, and lists.

## Table relationships

ServiceNow uses reference fields to connect tables together.

-   One-to-many: Most common relationship. Example: One user can have many incidents assigned to them. You add a reference field on the "many" side \(incident\) pointing to the "one" side \(user\).
-   Many-to-many: Requires an intermediate table. Example: Users can have multiple roles, and roles can be assigned to multiple users. You create a junction table with two reference fields.
-   Related lists: Automatically appear on forms to show connected records from other tables based on reference fields.

## Table extension \(inheritance\)

ServiceNow supports table extension where child tables inherit all fields and functionality from parent tables.

-   Most custom tables extend from the Configuration items \[cmdb\_ci\] table, task \(workflow items\), or standalone tables.
-   Child tables inherit all parent fields automatically plus their own custom fields.
-   Table extension reduces redundancy, enables consistent reporting across similar record types, and enables polymorphic queries.

Example: The Incident, Problem, and Change tables all extend the Task table, inheriting fields like assignment, state, and priority while adding their own specific fields.

**Parent Topic:**[Build your first application](build-your-first-app.md)

