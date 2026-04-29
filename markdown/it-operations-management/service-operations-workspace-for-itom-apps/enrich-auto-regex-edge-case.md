---
title: Regex preprocessing behavior in Enrich alert automation
description: Explains how Event Management alert automation preprocesses values before applying regex patterns, why matching behavior differs between pre-populated Additional Info JSON fields and free-text sample values, and how to design regex patterns that work reliably.
locale: en-US
release: australia
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create Enrich automation, Alert automation in SOW for ITOM, Using SOW for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# Regex preprocessing behavior in Enrich alert automation

Explains how Event Management alert automation preprocesses values before applying regex patterns, why matching behavior differs between pre-populated **Additional Info JSON** fields and free-text sample values, and how to design regex patterns that work reliably.

## Preprocessing alert fields

Event Management alert automation preprocesses alert field values before evaluating regex patterns. This preprocessing ensures consistent matching in the backend but can lead to different behavior in the UI depending on how you provide the sample value.

Understanding this behavior helps you build regex patterns that validate correctly and behave as expected at runtime.

## How preprocessing works

During regex evaluation, preprocessing occurs only if the value is a JSON value \(JSON inside the **Additional Info**\) regardless of how you enter the Sample Value. The system automatically preprocesses the Sample Value when you select a pre-populated **Additional Info** field from the **Extract from field** drop-down list.

Before applying regex matching, the backend preprocesses values as follows:

-   Removes quote characters \(`"`\)
-   Replaces ": " with "=" \(or ":" with "=", if no space is present\)
-   Converts JSON into `{key=value}`

## Free-text Sample Value limitation

When you manually enter a free-text sample value \(for example, when the selected field has no data or when testing without matching events\):

-   The UI does not preprocess the sample value.
-   The backend does preprocess the value during regex matching.
-   Regex patterns that work in external tools may not appear as matching in the UI.

|Current|Preferred|
|-------|---------|
|`{"type": "linux_server"}`|`{type=linux_server}`|
|`{"CI_Type": "server"}`|`{CI_Type=server}`|

## Impact

A mismatch can occur between the value entered in the **Sample Value** field, and the value the backend evaluates during regex matching.

## Workaround

Instead of matching JSON structure, match the preprocessed `{key=value}` format:

-   Use `{key=value}` instead of `{"key": "value"}`.
-   Avoid matching JSON structure \(quotes, colons, whitespace\).

