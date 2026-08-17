---
title: MPN security log fields
description: Reference for the structured fields produced when a raw MPN security log document is parsed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-service-ops/telecommunications-service-operations-management/nokia-mpn-security-log-fields.html
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: reference
last_updated: "2026-07-15"
reading_time_minutes: 1
breadcrumb: [Reference, Telecommunications Service Operations Management]
---

# MPN security log fields

Reference for the structured fields produced when a raw MPN security log document is parsed.

## Structured log fields

The parser extracts the following fields from each raw security log document. Some fields, including the customer identifier, are extracted from unstructured message text using pattern matching when the raw document doesn't already contain a structured value for that field.

|Field|Description|
|-----|-----------|
|Timestamp|Time the log event occurred, parsed from the raw document.|
|Host|Host associated with the log event.|
|Severity|Severity assigned by the parser based on the detection type: Critical, Major, Minor, or OK.|
|External ID|Unique identifier for the log event. Uses the source event ID when available, or a generated identifier based on the timestamp and host.|
|Message|Raw message text of the log event.|
|Source type|Log source subtype detected by the parser.|
|Activity|Activity or operation recorded in the log event.|
|Email ID|Email address of the user associated with the log event, when present.|
|Remote IP|Source IP address recorded in the log event.|
|User UUID|Unique identifier of the user associated with the log event.|
|Customer ID|Customer identifier extracted from the log event.|
|Resource|Resource or endpoint accessed in the log event.|
|Category|Category assigned to the log event.|
|Status|Outcome of the recorded activity.|
|Failure reason|Reason for a failed activity, when applicable.|
|Site ID|Identifier of the site associated with the log event.|
|Is failure|Indicates whether the recorded activity failed.|
|Is unauthorized|Indicates whether the log event represents unauthorized access.|
|Is off hours|Indicates whether the log event occurred outside of standard business hours.|
|Is sensitive access|Indicates whether the log event represents access to a sensitive resource.|
|Detection type|Classification assigned by the parser, for example unauthorized audit access, sign-in access denied, off-hours sensitive access, or login failure.|
|Reasons|Supporting details for the assigned detection type.|

**Parent Topic:**[Telecommunications Service Operations Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/components-installed-with-tsom.md)

**Related topics**  


[Configure security log collection for MPN](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/configure-security-log-collection-for-mpn.md)

