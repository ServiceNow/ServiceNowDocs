---
title: Monitor and troubleshoot FHIR sync runs
description: Review the FHIR Sync Log to confirm that sync runs complete, see how many records each run processed and skipped, and trace skipped records and failures to their cause.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/healthcare-life-sciences/hco-fhir-monitor-sync.html
release: australia
topic_type: task
last_updated: "2026-06-16"
reading_time_minutes: 1
keywords: [monitor, sync log, troubleshoot, correlation id]
breadcrumb: [Run the initial load, EMR Provider Directory Sync, Healthcare Integrations, Healthcare and Life Sciences]
---

# Monitor and troubleshoot FHIR sync runs

Review the FHIR Sync Log to confirm that sync runs complete, see how many records each run processed and skipped, and trace skipped records and failures to their cause.

## Before you begin

Role required: `sn_hco_intg_fhir.admin`.

## About this task

Each sync run records one FHIR Sync Log row per resource type. The four rows for a single run share a correlation ID. The status and record counts on each row tell you whether the run succeeded and how much data it moved. For the meaning of each field, see [FHIR Sync Log fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/healthcare-life-sciences/hco-fhir-sync-log-fields.md).

## Procedure

1.  Navigate to **All** &gt; **EMR Provider Directory Sync** &gt; **Sync Log**.

2.  Review the most recent rows, which are sorted by start time.

    Each run produces four rows — one each for Organization, Location, Practitioner, and PractitionerRole — that share a **Correlation ID**.

3.  Interpret the **Status** on each row:

    -   **Completed** — all records for the resource upserted successfully.
    -   **Completed with errors** — some records were skipped; check the **Records skipped** count.
    -   **Failed** — a transport, authentication, or system error stopped the import; check the **Error message** field.
4.  To investigate skipped records, copy the run's **Correlation ID** and open the platform system log.

    Filter the system log for entries that contain the correlation ID. Each skipped record is logged with its resource type, FHIR ID, and a reason, in the form `[FHIR Sync] cid=<id> type=<resource> fhir_id=<id> skipped reason=<reason>`.


## Result

You can confirm sync health at a glance and trace any skipped or failed records to their cause.

## What to do next

Common situations:

-   If the run stops after the Organization import, the Organization row is likely **Failed** — verify that the FHIR server and the HL7 FHIR Spoke connection are reachable, then rerun with **Execute Now**.
-   If locations import but some organization associations are missing, those locations referenced an organization that could not be resolved; the locations still upsert. Rerun after the missing organizations are imported.
-   If imported practitioners cannot sign in, set their password or configure SSO — the integration enables login but does not set credentials.

