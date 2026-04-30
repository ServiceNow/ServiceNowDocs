---
title: Installed with Knowledge Document plugin
description: These elements are installed with the Knowledge Document plugin.
locale: en-US
release: zurich
product: Document Management Services
classification: document-management-services
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Knowledge Document plugin, Managed Documents, Document Services, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Installed with Knowledge Document plugin

These elements are installed with the Knowledge Document plugin.

## Dependencies

The Knowledge Document plugin depends on the Managed Documents plugin. Activating Knowledge Document activates Managed Documents.

## Tables

|Display Name \[table\_name\]|Description|
|----------------------------|-----------|
|Knowledge Records \[m2m\_document\_knowledge\]|A many-to-many table storing the relationship between a document and a knowledge article.|

## UI Actions

|UI action|Description|
|---------|-----------|
|Link to Knowledge|Creates or updates a knowledge article related to the current document, depending on whether a knowledge article already exists.|

## Scripts

|Script include|Description|
|--------------|-----------|
|KnowledgeDocument|Holds the main logic for the Knowledge Document plugin.|
|KnowledgeDocumentDB|Class that gets, inserts, and updates data for the Knowledge Document plugin.|

**Parent Topic:**[Knowledge Document plugin](../concept/c_KnowledgeDocument.md)

