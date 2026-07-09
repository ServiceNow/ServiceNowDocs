---
title: How the FHIR sync works
description: A scheduled job runs an orchestration subflow that imports the four FHIR resources in dependency order, upserts each into the Healthcare Operations data model — matching primary records on the FHIR resource ID — and records the outcome in the FHIR Sync Log.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/healthcare-life-sciences/hco-fhir-how-it-works.html
release: australia
topic_type: concept
last_updated: "2026-06-16"
reading_time_minutes: 2
keywords: [FHIR sync, subflow, delta sync, upsert]
breadcrumb: [What the EMR Provider Directory Sync does, EMR Provider Directory Sync, Healthcare Integrations, Healthcare and Life Sciences]
---

# How the FHIR sync works

A scheduled job runs an orchestration subflow that imports the four FHIR resources in dependency order, upserts each into the Healthcare Operations data model — matching primary records on the FHIR resource ID — and records the outcome in the FHIR Sync Log.

## Scheduled orchestration

A scheduled job named **FHIR Sync — Daily** runs each day \(by default at 03:00 instance time\) and starts the **Import FHIR Resources** orchestration subflow. The orchestration subflow generates a correlation ID for the run and then runs the four per-resource import subflows in order. You can also start a run on demand with the scheduled job's **Execute Now** action.

## Dependency order

The four resources are imported in an order that respects cross-resource references, and the run stops if an earlier resource fails:

1.  **Organizations** — must exist before locations and practitioner roles can reference them.
2.  **Locations** — reference their managing organization.
3.  **Practitioners** — become users that practitioner roles reference.
4.  **PractitionerRoles** — reference both an organization and a practitioner, so they import last.

## Idempotent upsert

Each FHIR resource is matched to its primary Healthcare record by its FHIR logical ID, stored as `external_id` on the Healthcare \(HCLS\) Organization, Location, and Practitioner tables. Related records that have no `external_id` column — business locations, users, and service organization memberships — are matched on their natural keys instead, such as a user by email or a membership by its organization-and-user pair. Re-importing the same resource updates the existing records rather than creating duplicates, so repeated runs are safe. For the full field-by-field mapping, see [FHIR-to-HCLS field mappings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/healthcare-life-sciences/hco-fhir-field-mappings.md).

## Initial load and delta sync

The first run performs a full load of all four resources. Each subsequent run reads the timestamp of the previous successful run from the FHIR Sync Log and requests only resources changed since then, so routine syncs transfer only deltas.

## Logging and error handling

Each run writes one FHIR Sync Log row per resource type, all sharing the run's correlation ID. A row records the start and end times, processed and skipped counts, and a final status of Completed, Completed with errors, or Failed. Per-record skips — such as a resource missing a required field or an unresolvable reference — are logged to the system log with the correlation ID and FHIR ID, while transport or authentication failures set the row status to Failed and stop the run. For details, see [Monitor and troubleshoot FHIR sync runs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/healthcare-life-sciences/hco-fhir-monitor-sync.md).

