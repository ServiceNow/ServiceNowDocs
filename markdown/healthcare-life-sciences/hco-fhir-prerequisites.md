---
title: Prerequisites for the FHIR integration
description: Before you activate the EMR Provider Directory Sync, confirm that its dependent applications are installed and that the HL7 FHIR Spoke connection to your FHIR server is configured.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/healthcare-life-sciences/hco-fhir-prerequisites.html
release: australia
topic_type: task
last_updated: "2026-06-16"
reading_time_minutes: 1
keywords: [prerequisites, dependencies, FHIR spoke]
breadcrumb: [EMR Provider Directory Sync, Healthcare Integrations, Healthcare and Life Sciences]
---

# Prerequisites for the FHIR integration

Before you activate the EMR Provider Directory Sync, confirm that its dependent applications are installed and that the HL7 FHIR Spoke connection to your FHIR server is configured.

## Before you begin

Role required: admin

## About this task

The EMR Provider Directory Sync writes to tables owned by several Healthcare Operations and platform applications and calls the HL7 FHIR Spoke to read from the FHIR server. All of these must be present before the sync can run.

## Procedure

1.  Install the **EMR Provider Directory Sync** \(`sn_hcls_emr_sync`\) plugin from the ServiceNow Store.

2.  Confirm that the following applications are installed on your instance:

    -   HL7 FHIR Spoke \(`sn_hl7_fhir_spoke`\) — provides the FHIR R4 actions.
    -   Healthcare Operations core \(`sn_hco_core`\) — provides the base administrator role and the care-team-member role and responsibility.
    -   Healthcare and Life Sciences data model \(`sn_hcls`\) — owns the Healthcare Organization, Location, and Practitioner tables.
    -   Business Location \(`sn_bus_loc`\) — owns the business location tables.
    -   Service Organization \(`sn_service_org`\) — owns the service organization member tables.
    -   Customer Service Management \(`sn_customerservice`\) — owns the related-party configuration used for the care-team-member responsibility.
3.  Confirm that the HL7 FHIR Spoke's `HL7 FHIR` Connection &amp; Credential Alias is configured with valid credentials for your FHIR server.

    See [Configure the HL7 FHIR connection and credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown).

4.  Confirm that the administrator who will operate the sync has the `sn_hco.admin` role, which grants the `sn_hco_intg_fhir.admin` role through inheritance.


## Result

With the prerequisites in place, you can activate the sync schedule. See [Activate the FHIR sync schedule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/healthcare-life-sciences/hco-fhir-activate.md).

