---
title: ServiceNow metadata in applications
description: ServiceNow metadata refers to the configuration and structural definitions that make up a ServiceNow application itself.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Building apps in ServiceNow, Getting Started guide for developers, Building applications]
---

# ServiceNow metadata in applications

ServiceNow metadata refers to the configuration and structural definitions that make up a ServiceNow application itself.

## What is ServiceNow metadata?

Application metadata encompasses all the configuration elements that define how a ServiceNow application works. Think of it as the "blueprint" of your application. It's not the data users create, but rather the structure and rules that govern how the application behaves.

## Files are distinct from metadata

The fundamental difference between files and metadata is that application files are user data or content managed within the platform, while application metadata is the platform configuration that defines the application's structure, logic, and behavior. Metadata is what developers and admins configure to build applications; files are what end users and processes upload or generate within those applications.

## Metadata examples

There are many types of metadata you can associate with an application. Some examples are included here.

**Configuration records**: Tables, fields, forms, lists, UI policies, business rules, client scripts, access control lists \(ACLs\), workflows, and other platform components that define how an application works.

**Application scope**: In the ServiceNow scoped application model, metadata is organized into applications that have their own namespace and can be version-controlled.

**Update sets**: Metadata changes are captured in update sets, which are collections of configuration modifications that can be migrated between instances.

**System definition**: The structural elements stored in various system tables \(like \[sys\_db\_object\] for tables, \[sys\_dictionary\] for fields, \[sys\_ui\_section\] for forms\) that define the application's behavior and appearance.

## How is metadata used in applications?

Metadata is used in applications in several different ways.

**Application development**: Developers use ServiceNow Studio or the platform interface to create and modify metadata records. When you build a custom application, you create a collection of related metadata that works together.

**Scoped applications**: The ServiceNow application scope model organizes metadata into discrete applications with their own namespace \(like x\_company\_appname\). This prevents naming conflicts and makes applications portable and manageable.

**Version control**: Metadata is tracked in update sets or source control, allowing you to capture changes, migrate them between instances \(development, test, production\), and maintain version history.

**Platform interpretation**: At runtime, ServiceNow reads the metadata to understand how to render forms, enforce rules, execute logic, and control access.

**Customization without coding**: Much of the power of the ServiceNow AI Platform comes from the ability to let administrators configure complex applications by creating and modifying metadata records, often without writing code.

**Application store**: When you install applications from the ServiceNow Store, you import a package of metadata that gets installed into your instance.

**Parent Topic:**[Overview of building apps in ServiceNow](overview-building-apps-in-servicenow.md)

