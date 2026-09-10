---
title: Catalog client scripts
description: AI can generate a catalog client script from a plain-language description of catalog item behavior without requiring you to write code.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/service-catalog/catalog-client-scripts.html
release: australia
product: Service Catalog
classification: service-catalog
topic_type: reference
last_updated: "2026-09-02"
reading_time_minutes: 1
breadcrumb: [Things to know while creating items using AI, AI Authoring for Catalog Builder reference, AI Authoring for Catalog Builder, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Catalog client scripts

AI can generate a catalog client script from a plain-language description of catalog item behavior without requiring you to write code.

## Client script

When a user wants to create a client script and provides the requirements in natural language, AI can generate the client script based on those requirements.

If a variable name is duplicated or the same field exists across variable sets, AI asks users to specify which variable the validation should apply to.

Before creating a client script, AI checks whether similar client-side validation already exists \(through an existing client script or UI policy\). If found, AI asks the user with that information instead of proceeding to create a duplicate.

AI generates a catalog client script when asked for one explicitly, or when the behavior needs logic a UI Policy can't express.

If your description depends on a question that doesn't exist and its type is clear from description, AI creates the question, generates script, and confirms both actions. For example, you describe showing an Asset Tag field when Request Type is Hardware. But no Asset Tag question exists, AI adds a single-line text question named Asset Tag and confirms: "I've added an 'Asset Tag' question to this item, and created the client script that shows it when Request Type is Hardware."

## Event triggers

AI generates only `onLoad`, `onChange`, or `onSubmit` scripts.

|Event Trigger|Example|
|-------------|-------|
|`onLoad`|If the current user does not have the itil role, set the "Cost Center Override" variable to read-only.|
|`onChange`|When Quantity or Unit Price changes, calculate and display the Total Cost.|
|`onSubmit`|Before submitting, validate that End Date is after Start Date and block submission with an error if not.|

AI defaults new scripts to UI type: All.

## Roles

|Role|Description|
|----|-----------|
|Catalog builder developer|Required to create client scripts with AI. A catalog builder editor who attempts this is informed that they don't have the necessary privileges.|

**Parent Topic:**[Things to know while creating items using AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/things-to-know-while-creating-items-using-ai.md)

