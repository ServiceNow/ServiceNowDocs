---
title: Quote transaction personas
description: Personas define distinct user types in the quoting experience, controlling what users can view and edit on a quote at each stage in ServiceNow CPQ.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/quote-tm-personas.html
release: australia
topic_type: concept
last_updated: "2026-05-07"
reading_time_minutes: 1
breadcrumb: [Configuring Quote Experience, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Quote transaction personas

Personas define distinct user types in the quoting experience, controlling what users can view and edit on a quote at each stage in ServiceNow CPQ.

ServiceNow Quote Experience uses personas to represent the distinct roles found in a sales organization, such as a sales representative or a sales manager. Each persona has customized access to data — controlling what users with that persona can view and edit and how the layout appears at each stage of the quote lifecycle.

## Persona behavior

A persona is assigned to a view, which defines the field and event access privileges for users with that persona at each stage. A user account can be assigned to only one persona. Personas are assigned to views, and a persona can only be assigned to one view.

## Personas and blueprints

Personas aren't part of the ServiceNow Quote Experience blueprint. They are not included in the blueprint export file. When a blueprint is migrated to a new environment, personas must be recreated in that environment.

## User access prerequisite

To assign a user account to a persona, the user must first be created using the User Access function in Utilities. User accounts that aren't in the User Access list can't be assigned to a persona.

