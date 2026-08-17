---
title: EMR Provider Directory Sync Sync release notes
description: The ServiceNow EMR Provider Directory Sync application keeps Healthcare Operations organization, location, practitioner, and care-team data in sync with a FHIR R4 server on a schedule. EMR Provider Directory Sync is a new application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/hco-fhir-release-notes-rn.html
release: australia
topic_type: reference
last_updated: "2026-06-16"
reading_time_minutes: 2
keywords: [Healthcare Operations, FHIR, FHIR R4, HCLS, release notes]
breadcrumb: [Healthcare and Life Sciences release notes, Features and changes by product, Release notes for upgrading from Zurich, Learn about the Australia release, Australia release notes]
---

# EMR Provider Directory Sync Sync release notes

The ServiceNow® EMR Provider Directory Sync application keeps Healthcare Operations organization, location, practitioner, and care-team data in sync with a FHIR R4 server on a schedule. EMR Provider Directory Sync is a new application.

## EMR Provider Directory Sync highlights

-   Keep Healthcare Operations organizations, business locations, practitioners, and care-team memberships in sync with a FHIR R4 server without manual maintenance.
-   Import FHIR Organization, Location, Practitioner, and PractitionerRole resources on a configurable daily schedule, with delta syncs after the first full load.
-   Track every sync run in a FHIR Sync Log, with per-resource status and record counts correlated by run.
-   Classify imported organizations as internal or external business locations using an editable decision table.

See EMR Provider Directory Sync for more information.

## EMR Provider Directory Sync features

-   **How the FHIR sync works**

    A scheduled job runs an orchestration subflow that imports the four FHIR resources in dependency order and upserts them into the Healthcare Operations data model, keyed on the FHIR resource ID.

-   **Run the initial load**

    After the initial full load, each run uses the previous successful run's timestamp as a watermark to import only resources changed since then.

-   **Monitor and troubleshoot FHIR sync runs**

    Each run records one FHIR Sync Log row per resource type, with status, processed and skipped counts, and a shared correlation ID, so admins can monitor and troubleshoot syncs.


## Activation information

Install EMR Provider Directory Sync by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

This application depends on the HL7 FHIR Spoke and on the Healthcare Operations and Healthcare and Life Sciences data-model applications. For the full list, see Prerequisites for the FHIR integration.

## Plugin information

-   **New plugins**

    The following plugins are new in Australia:

    EMR Provider Directory Sync \(`sn_hcls_emr_sync`\): Keeps Healthcare Operations organization, location, practitioner, and care-team data in sync with a FHIR R4 server on a configurable schedule.


## Related ServiceNow applications and features

-   **HL7 FHIR Spoke**

    Provides the read-only FHIR R4 Flow Designer actions that this application calls to read provider-directory data.


**Parent Topic:**[Healthcare and Life Sciences release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/healthcare-life-sciences-rn-landing.md)

