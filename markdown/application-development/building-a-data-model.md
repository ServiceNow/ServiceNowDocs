---
title: Building a data model
description: Plan your data model carefully before building an application on the ServiceNow AI Platform. It defines what information you're managing, how it connects, and ultimately determines what your application can do.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Build your first app, Getting Started guide for developers, Building applications]
---

# Building a data model

Plan your data model carefully before building an application on the ServiceNow AI Platform. It defines what information you're managing, how it connects, and ultimately determines what your application can do.

## Why build the data model first?

Your data model is the blueprint for your entire application. It defines what information you're managing, how it connects, and ultimately determines what your application can do. Getting the data model right from the start saves massive refactoring effort later, because everything else—forms, lists, workflows, reports, integrations—is built on top of this foundation.

Think of it like building a house: the data model is your foundation and framing. You can change the paint color \(UI\) or add new rooms \(features\) easily, but changing the foundation after construction is expensive and disruptive.

## Planning considerations

-   Normalization: Avoid duplicating data. Instead of storing customer name/address on every order, reference a customer table.
-   Naming conventions: Use clear, consistent prefixes for custom fields \(like u\_ for user-created fields\) and descriptive names.
-   Field types: Choose appropriate types for the data you're gathering.
    -   String for text
    -   Integer/Decimal for numbers
    -   Reference for relationships
    -   Choice for dropdown options
    -   Date/DateTime for temporal data
    -   Boolean for true/false flags
-   Performance considerations:
    -   Don't create unnecessary fields, they slow down queries and forms.
    -   Use indexed fields for frequently searched/filtered columns.
    -   Consider table partitioning for very large data sets.
-   Required vs Optional fields: Mark fields as mandatory only when truly necessary for data integrity.
-   Choice lists: Define standardized dropdown options to help ensure data consistency rather than allowing free text.

## Application scope

Tables belong to an application scope - a namespace that isolates your app's data and logic. This helps prevent naming conflicts and allows for cleaner packaging/deployment. Custom tables are prefixed with your scope \(like `x_12345_myapp_customer`\).

## Design process

1.  Identify entities: What "things" must your app track? \(Customers, Orders, Products, etc.\)
2.  Define attributes: What information about each entity must you store?
3.  Map relationships: How do these entities connect to each other?
4.  Choose parent tables: Will you extend existing tables or create standalone ones?
5.  Create tables and fields: Use ServiceNow Studio to build your schema.
6.  Set up access controls: Define who can create, read, write, and delete records.

**Parent Topic:**[Build your first application](build-your-first-app.md)

