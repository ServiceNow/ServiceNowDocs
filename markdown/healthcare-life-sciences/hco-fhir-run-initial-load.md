---
title: Run the initial load
description: Run the FHIR import on demand to perform the first full load of Organization, Location, Practitioner, and PractitionerRole data into the Healthcare Operations data model.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/healthcare-life-sciences/hco-fhir-run-initial-load.html
release: australia
topic_type: task
last_updated: "2026-06-16"
reading_time_minutes: 1
keywords: [initial load, full sync, execute now]
breadcrumb: [EMR Provider Directory Sync, Healthcare Integrations, Healthcare and Life Sciences]
---

# Run the initial load

Run the FHIR import on demand to perform the first full load of Organization, Location, Practitioner, and PractitionerRole data into the Healthcare Operations data model.

## Before you begin

Role required: `sn_hco_intg_fhir.admin`.

The **FHIR Sync — Daily** job must be configured. See [Activate the FHIR sync schedule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/healthcare-life-sciences/hco-fhir-activate.md).

## About this task

The first time the sync runs, it performs a full load of all four FHIR resources because there is no previous run watermark. You can wait for the scheduled run or trigger the load immediately to validate your configuration.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs** and open the **FHIR Sync — Daily** record.

2.  Click **Execute Now**.

    The orchestration subflow runs the four imports in order: Organizations, Locations, Practitioners, and then PractitionerRoles. A large initial load can take several minutes.

3.  Verify the results in the FHIR Sync Log.

    See [Monitor and troubleshoot FHIR sync runs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/healthcare-life-sciences/hco-fhir-monitor-sync.md).


## Result

The Healthcare Operations data model is populated with the imported FHIR data. Subsequent scheduled runs import only resources changed since the last successful run.

**Note:** Imported practitioners are created as active platform users, but login is not enabled automatically. An administrator provisions each practitioner's password or SSO out of band before they can sign in.

