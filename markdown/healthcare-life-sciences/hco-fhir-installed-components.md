---
title: Components installed with the EMR Provider Directory Sync
description: Several types of components are installed with the EMR Provider Directory Sync, including a user role, a sync log table, a scheduled job, flows, a business rule, flow actions, and a decision table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/healthcare-life-sciences/hco-fhir-installed-components.html
release: australia
topic_type: reference
last_updated: "2026-06-16"
reading_time_minutes: 3
keywords: [installed components, roles, scheduled job, sync log]
breadcrumb: [EMR Provider Directory Sync, Healthcare Integrations, Healthcare and Life Sciences]
---

# Components installed with the EMR Provider Directory Sync

Several types of components are installed with the EMR Provider Directory Sync, including a user role, a sync log table, a scheduled job, flows, a business rule, flow actions, and a decision table.

## Roles installed

<table><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

HCO FHIR Integration Admin

 \[`sn_hco_intg_fhir.admin`\]

</td><td>

Operates the FHIR sync: triggers runs, edits the sync schedule and the organization classification decision table, and reads, creates, and updates FHIR Sync Log rows.

</td><td>

Inherited by users with `sn_hco.admin`.

</td></tr></tbody>
</table>## Tables installed

<table><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

FHIR Sync Log

 \[`sn_hco_intg_fhir_sync_log`\]

</td><td>

Records one row per resource type per sync run, with start and end times, processed and skipped counts, status, correlation ID, and a transport error message. For field details, see [FHIR Sync Log fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/healthcare-life-sciences/hco-fhir-sync-log-fields.md).

</td></tr></tbody>
</table>The application also writes to tables owned by other applications — including the Healthcare Organization, Location, and Practitioner tables, the business location tables, the user table, and the service organization member tables — but does not install them. See [FHIR-to-HCLS field mappings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/healthcare-life-sciences/hco-fhir-field-mappings.md).

## Scheduled jobs installed

<table><thead><tr><th>

Scheduled job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

FHIR Sync — Daily

</td><td>

Runs daily \(by default at 03:00 instance time\) and starts the **Import FHIR Resources** orchestration subflow. Admins can also run it on demand with **Execute Now**.

 Installed inactive. Set **Active** to true on the job record before first use.

</td></tr></tbody>
</table>## Flows and subflows installed

|Subflow|Description|
|-------|-----------|
|Import FHIR Resources|Orchestration subflow that sets a correlation ID and runs the four per-resource imports in dependency order, stopping if any fails.|
|Import Organizations|Imports FHIR Organizations into Healthcare Organization records and internal or external business locations.|
|Import Locations|Imports FHIR Locations into platform and Healthcare Location records and associates them with a managing organization.|
|Import Practitioners|Imports FHIR Practitioners into user and Healthcare Practitioner records and grants the care-team-member role.|
|Import PractitionerRoles|Imports FHIR PractitionerRoles into service organization member and responsibility records.|
|Start Sync Log Entry / End Sync Log Entry|Shared subflows that open and close a FHIR Sync Log row and provide the delta-sync watermark.|

Each per-resource import decomposes into additional child subflows — a per-record processor and a shared upsert subflow, plus a one-level parent-recovery subflow for Organizations and Locations.

## Business rules installed

|Business rule|Table|Description|
|-------------|-----|-----------|
|Stamp ended on status transition|`sn_hco_intg_fhir_sync_log`|Before update — stamps the `ended` timestamp when a sync log row transitions out of the Running status.|

## Flow actions installed

|Action|Description|
|------|-----------|
|Format FHIR Last-Updated Filter|Converts the previous run's timestamp into a FHIR `last updated` search filter for delta syncs.|
|Parse FHIR Reference|Strips the resource-type prefix from a FHIR reference to return the bare logical ID.|

## Decision tables installed

|Decision table|Description|
|--------------|-----------|
|`FhirOrgTypeToBusinessLocationClass`|Classifies an imported FHIR Organization as an internal or external business location based on its organization type. Editable by admins. See [Configure the organization classification decision table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/healthcare-life-sciences/hco-fhir-configure-decision-table.md).|

## Spoke components used

EMR Provider Directory Sync uses read-only actions from the [HL7 FHIR Spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown) to fetch provider-directory data. The following FHIR Spoke actions are called by the import subflows:

-   Look up Organization by ID
-   Look up Organizations Stream
-   Look up Location by ID
-   Look up Locations Stream
-   Look up Practitioner by ID
-   Look up Practitioners Stream
-   Look up PractitionerRole by ID
-   Look up PractitionerRoles Stream

All eight actions authenticate through the shared `HL7 FHIR` Connection &amp; Credential Alias defined in the HL7 FHIR Spoke. For setup details, see [HL7 FHIR Spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown).

## System properties installed

The application installs no system properties. The sync cadence is controlled by the scheduled job record, and the organization classification is controlled by the decision table.

