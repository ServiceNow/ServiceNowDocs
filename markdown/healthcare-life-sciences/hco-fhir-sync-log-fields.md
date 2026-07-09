---
title: FHIR Sync Log fields
description: The FHIR Sync Log table \(sn\_hco\_intg\_fhir\_sync\_log\) records one row per resource type per sync run. Use these fields to monitor sync health and trace skipped or failed records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/healthcare-life-sciences/hco-fhir-sync-log-fields.html
release: australia
topic_type: reference
last_updated: "2026-06-16"
reading_time_minutes: 1
keywords: [sync log, fields, correlation id, status]
breadcrumb: [EMR Provider Directory Sync, Healthcare Integrations, Healthcare and Life Sciences]
---

# FHIR Sync Log fields

The FHIR Sync Log table \(`sn_hco_intg_fhir_sync_log`\) records one row per resource type per sync run. Use these fields to monitor sync health and trace skipped or failed records.

## Field reference

|Field|Description|
|-----|-----------|
|Resource type|The FHIR resource the row tracks: Organization, Location, Practitioner, or PractitionerRole.|
|Status|The outcome of the import: Running, Completed, or Failed. Skipped records do not change a Completed status to an error status.|
|Started|The time the import for this resource started. The most recent successful start time becomes the watermark for the next delta sync.|
|Ended|The time the import ended. Stamped automatically when the status leaves Running.|
|Records processed|The number of FHIR resources successfully upserted into the target tables.|
|Records skipped|The number of FHIR resources skipped — for example, missing a required field or an unresolvable reference. Per-record reasons are written to the platform system log.|
|Correlation ID|A unique identifier shared by all four rows of a single sync run. Use it to group a run's rows and to find the run's per-record entries in the system log.|
|Error message|A transport or system error summary, populated only when the status is Failed. It does not contain record-level detail or protected health information.|

## Record retention

Sync log records are automatically archived and permanently deleted after six months. Archive and destroy rules run nightly. Any row whose **Started** date is more than six months in the past is moved to the platform archive store and immediately purged.

