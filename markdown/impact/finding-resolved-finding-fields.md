---
title: Scan Engine API field reference
description: Field reference for scan status, findings, and resolved findings API responses.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/finding-resolved-finding-fields.html
release: brazil
topic_type: reference
last_updated: "2026-08-25"
reading_time_minutes: 3
keywords: [findings, resolved findings, API, fields]
breadcrumb: [Scan Engine reference, Impact reference, Impact]
---

# Scan Engine API field reference

Field reference for scan status, findings, and resolved findings API responses.

## Scan status response fields

The scan status endpoint returns the following fields.

|Field|Description|
|-----|-----------|
|batches\_complete|Number of batches that have finished processing.|
|end\_time|Scan end timestamp in format YYYY-MM-DD HH:MM:SS, or null if still running.|
|number|Scan result number, for example SCAN0001234.|
|progress\_percent|Scan progress percentage from 0 to 100.|
|scan\_result\_sys\_id|Unique sys\_id of the scan result record.|
|scan\_type|Type of scan: full\_instance\_scan, delta\_instance\_scan, on\_demand\_instance\_scan, application\_scan, update\_set\_scan, or push\_commit\_scan.|
|source|Originating ServiceNow instance name, or null if not applicable.|
|start\_time|Scan start timestamp in format YYYY-MM-DD HH:MM:SS.|
|status|Current scan state: Waiting, Getting Ready, Scanning, Complete, complete\_with\_errors, Cancelled, Cancellation Requested, No Action Taken, or Queued Scan Cancelled. Keep polling while status is not a terminal state.|
|summary|Available only when status is Complete. Contains: total\_findings, total\_errors, total\_warnings, se\_score, total\_impact\_to\_instance, total\_technical\_debt, and definitions\_scanned\_for.|
|total\_batches|Total number of batches the scan is divided into.|
|trigger\_channel|Declared request channel, either API, UI, or Scheduled, captured from the request's source value at trigger time. Use this to determine if a scan was triggered via the API.|

## Finding and resolved finding fields

The findings and resolved findings endpoints return the following fields. Some fields appear in both response types.

|Field|Description|Finding|Resolved Finding|
|-----|-----------|-------|----------------|
|definition|Sys\_id of the scan definition that raised this finding.|✓|✓|
|definition\_number|Number of that scan definition, for example sn\_SE10524.|✓|✓|
|exception\_state|Status of the exception: Requested, Not Yet Requested, Rejected, Approved, No Longer Required, or Not Applicable, or null if none.|✓| |
|exception\_sys\_id|Sys\_id of an exception request filed against this finding, if any, or null if none.|✓| |
|finding\_count|Number of times this condition was detected.|✓| |
|finding\_details|Human-readable explanation of what the finding is and why it was raised.|✓| |
|finding\_policy\_status|Status of that finding policy: Acceptable as is or Prioritize, or null if none.|✓| |
|finding\_policy\_sys\_id|Sys\_id of a finding policy applied to this finding, if any, or null if none.|✓| |
|finding\_sys\_id|Sys\_id of the original finding that was resolved.| |✓|
|impact\_to\_instance|Severity and impact score for this finding.|✓|✓|
|net\_new\_finding|True if this is the first time reported, false if it also appeared in a prior scan.|✓| |
|resolved\_on|Date the finding was marked as resolved in ISO 8601 format YYYY-MM-DD.| |✓|
|scan\_type|Type of scan that produced this finding.|✓|✓|
|scanned\_date|Date and time the record was scanned in format YYYY-MM-DD HH:MM:SS.|✓| |
|scanned\_record|Object containing sys\_id and table of the record that was scanned.| |✓|
|scanned\_record\_display\_value|Display value of the scanned record, or null if the record no longer exists.|✓| |
|scanned\_record\_sys\_id|Sys\_id of the record that was scanned, or null if not tied to a specific record.|✓| |
|scanned\_record\_table|Table name of the scanned record.|✓| |
|scanned\_scope|Object containing sys\_id and display\_value of the application scope.| |✓|
|scanned\_scope\_display\_value|Display name of that application scope, such as Global.|✓| |
|scanned\_scope\_sys\_id|Sys\_id of the application scope containing the scanned record.|✓| |
|scanned\_table|Table name of the scanned record.| |✓|
|sys\_id|Unique identifier of the record.|✓|✓|

## Resolved findings query parameters

The resolved findings endpoint accepts the following query parameters.

|Parameter|Description|
|---------|-----------|
|definition|Filter by definition sys\_id or number. Optional.|
|impact\_to\_instance|Filter by exact impact score. Optional.|
|limit|Page size. Default 100, maximum 1000. Optional.|
|offset|Page offset. Default 0. Optional.|
|resolved\_by|Filter by who resolved it, using string name \(not a user reference\). Optional.|
|resolved\_by\_auto\_fix|Filter by whether the finding was auto-fixed. Use true or false. Optional.|
|resolved\_on\_from|Resolved on or after. Use ISO 8601 date format YYYY-MM-DD. Optional.|
|resolved\_on\_to|Resolved on or before. Use ISO 8601 date format YYYY-MM-DD. Optional.|
|scanned\_scope|Filter by application scope sys\_id. Optional.|
|scanned\_table|Filter by scanned table name. Optional.|

**Parent Topic:**[Scan Engine reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/scan-engine-reference.md)

