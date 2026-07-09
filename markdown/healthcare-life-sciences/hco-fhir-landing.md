---
title: EMR Provider Directory Sync
description: The EMR Provider Directory Sync imports HL7 FHIR R4 Organization, Location, Practitioner, and PractitionerRole resources from a FHIR server into the ServiceNow Healthcare Operations data model on a configurable schedule, keeping organizations, business locations, practitioners, and care-team memberships in sync without manual maintenance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/healthcare-life-sciences/hco-fhir-landing.html
release: australia
topic_type: reference
last_updated: "2026-06-16"
reading_time_minutes: 3
breadcrumb: [Healthcare Integrations, Healthcare and Life Sciences]
---

# EMR Provider Directory Sync

The EMR Provider Directory Sync imports HL7 FHIR R4 Organization, Location, Practitioner, and PractitionerRole resources from a FHIR server into the ServiceNow Healthcare Operations data model on a configurable schedule, keeping organizations, business locations, practitioners, and care-team memberships in sync without manual maintenance.

The Healthcare Operations \(HCO\) data model depends on accurate organization, location, and practitioner records. This application ingests four FHIR R4 resources from a FHIR server on a configurable schedule and upserts them into the corresponding Healthcare Operations tables, identifying records across runs by the FHIR resource ID stored as an external identifier on each target.

The integration is one-way \(FHIR server to ServiceNow\), admin-operated, and scheduled. It builds on the [HL7 FHIR Spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown), which provides the read-only FHIR actions, and owns all FHIR-to-HCLS field mapping, upsert keys, and dependency ordering.

## Get started

-   [What EMR Provider Directory Sync does](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/healthcare-life-sciences/hco-fhir-overview.md)
-   [How the FHIR sync works](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/healthcare-life-sciences/hco-fhir-how-it-works.md)
-   [Prerequisites for the FHIR integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/healthcare-life-sciences/hco-fhir-prerequisites.md)
-   [Activate the FHIR sync schedule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/healthcare-life-sciences/hco-fhir-activate.md)
-   [Change the sync schedule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/healthcare-life-sciences/hco-fhir-configure-schedule.md)
-   [Configure the organization classification decision table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/healthcare-life-sciences/hco-fhir-configure-decision-table.md)
-   [Run the initial load](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/healthcare-life-sciences/hco-fhir-run-initial-load.md)
-   [Monitor and troubleshoot FHIR sync runs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/healthcare-life-sciences/hco-fhir-monitor-sync.md)
-   [Components installed with EMR Provider Directory Sync](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/healthcare-life-sciences/hco-fhir-installed-components.md)
-   [FHIR Sync Log fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/healthcare-life-sciences/hco-fhir-sync-log-fields.md)
-   [FHIR-to-HCLS field mappings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/healthcare-life-sciences/hco-fhir-field-mappings.md)

## Helpful resources

Some ServiceNow resources that can provide helpful information:

-   **\[Omitted image "dcx-icon-community.svg"\]ServiceNow Community**

    Connect with other Healthcare Operations users in the [Healthcare and Life Sciences community](https://www.servicenow.com/community/healthcare-life-sciences/ct-p/healthcare-life-sciences).

-   **\[Omitted image "dcx-icon-learning.svg"\]ServiceNow University**

    Access training and certification resources on [ServiceNow University](https://learning.servicenow.com).


