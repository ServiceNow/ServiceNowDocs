---
title: ServiceNow files in applications
description: ServiceNow files are digital documents and assets stored within the ServiceNow AI Platform that serve various purposes across applications and workflows.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Building apps in ServiceNow, Getting Started guide for developers, Building applications]
---

# ServiceNow files in applications

ServiceNow files are digital documents and assets stored within the ServiceNow AI Platform that serve various purposes across applications and workflows.

## What are ServiceNow files?

In ServiceNow, files are attachments that can be associated with records in the platform. These include documents, images, spreadsheets, PDFs, and other file types. ServiceNow stores file metadata in the \[sys\_attachment\] table, while the actual file content is stored in the \[sys\_attachment\_doc\] table.

## Files are distinct from metadata

The fundamental difference between files and metadata is that application files are user data or content managed within the platform, while application metadata is the platform configuration that defines the application's structure, logic, and behavior. Metadata is what developers and admins configure to build applications; files are what end users and processes upload or generate within those applications.

## Application file examples

Application files are the actual file attachments stored in the ServiceNow AI Platform file storage system. These are binary data objects like:

-   Documents \(PDFs, Word files, Excel spreadsheets\)
-   Images \(PNG, JPEG, GIF\)
-   Videos, audio files
-   ZIP archives
-   Any other uploaded file content.

These files are stored in the \[sys\_attachment\] and \[sys\_attachment\_doc\] tables and represent the actual content that users upload or the system generates.

## How are files used in applications?

Files in ServiceNow applications serve several key functions:

**Record documentation**: Files can be attached to incidents, change requests, knowledge articles, and other records to provide supporting documentation, screenshots, or evidence. For example, a user reporting an IT issue might attach a screenshot showing an error message.

**Knowledge management**: Knowledge base articles often include attached PDFs, images, or other documents that provide detailed instructions or reference materials for end users and support teams.

**Workflow automation**: Files can trigger or be part of automated workflows. For instance, a business rule might process an uploaded spreadsheet, or a workflow could generate and attach reports to records automatically.

**Service Catalog**: When users request services through the service catalog, they can upload required documents like purchase requisitions, approval forms, or specifications that are then processed as part of the fulfillment workflow.

**Integration and import**: Files are used to import data into ServiceNow \(like CSV imports for bulk updates\) or as outputs from integrations with external systems.

The platform provides APIs and scripting capabilities to programmatically create, read, update, and manage attachments, making files a flexible component of custom ServiceNow applications.

**Parent Topic:**[Overview of building apps in ServiceNow](overview-building-apps-in-servicenow.md)

