---
title: Glossary import error scenarios
description: Error and warning messages that can occur when uploading glossary term files, and their impact on the import process.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/glossary-import-error-scenarios.html
release: australia
topic_type: reference
last_updated: "2026-01-23"
reading_time_minutes: 2
keywords: [glossary import errors, import warnings, XLSX upload, data catalog errors]
breadcrumb: [Managing glossary terms, Data Catalog, Workflow Data Fabric]
---

# Glossary import error scenarios

Error and warning messages that can occur when uploading glossary term files, and their impact on the import process.

An error state indicates that the file cannot be uploaded without fixing the issue. A warning state means the specific field or value with the warning is skipped, but the rest of your data imports successfully.

## File-level errors

|Scenario|Type|Will import succeed?|
|--------|----|--------------------|
|The file format is incorrect. Only XLSX files are supported.|Error|NO|
|The file size exceeds the maximum allowed limit.|Error|NO|
|The file contains more rows than allowed. Consider splitting your upload into smaller files.|Error|NO|
|The file structure is invalid.|Error|NO|
|A system error occurred while processing your file.|Error|NO|

## Row-level errors

|Scenario|Type|Will import succeed?|
|--------|----|--------------------|
|The required **Title** field is empty for a new row.|Error|Partial — row is skipped|
|The **Title** field has been removed from an existing row. Title is required.|Error|Partial — row is skipped|
|The record cannot be found or you don't have permission to access it.|Error|Partial — row is skipped|

## Row-level warnings

|Scenario|Type|Will import succeed?|
|--------|----|--------------------|
|The domain does not exist in the system.|Warning|YES — domain field is skipped|
|The owner email does not match any user in the system.|Warning|YES — owner field is skipped|
|The status value is not valid for this field.|Warning|YES — status field is skipped|
|One or more tag names do not exist in the system.|Warning|YES — invalid tags are skipped; valid tags are applied|
|The title already exists in the system.|Warning|YES — row imports as a duplicate|
|A field value is too long and will be automatically shortened.|Warning|YES — value is truncated and applied|
|You attempted to change a system-managed field. The original value is retained.|Warning|YES — field is unchanged|

## Commit-time errors

|Scenario|Type|Will import succeed?|
|--------|----|--------------------|
|The record was modified by another user after your preview was generated.|Error|Partial — row fails; others may succeed|
|The record could not be updated due to a system error.|Error|Partial — row fails; others may succeed|

## Final import status

After the import completes, the system displays one of the following status values:

-   `COMMITTED` — All rows imported successfully
-   `PARTIAL` — Some rows imported; others failed
-   `FAILED` — No rows imported

**Parent Topic:**[Managing glossary terms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/managing-glossary-terms.md)

