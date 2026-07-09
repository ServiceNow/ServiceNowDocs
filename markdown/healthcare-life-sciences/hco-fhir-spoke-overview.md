---
title: HL7 FHIR Spoke
description: The HL7 FHIR Spoke is an Integration Hub action pack that gives Workflow Studio authors read-only access to HL7 FHIR R4 provider-directory resources. The EMR Provider Directory Sync builds on this spoke to import provider data into the Healthcare Operations data model.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/healthcare-life-sciences/hco-fhir-spoke-overview.html
release: australia
topic_type: concept
last_updated: "2026-07-01"
reading_time_minutes: 1
keywords: [HL7 FHIR Spoke, FHIR integration, IntegrationHub, Healthcare Operations]
breadcrumb: [Healthcare and Life Sciences]
---

# HL7 FHIR Spoke

The HL7 FHIR Spoke is an Integration Hub action pack that gives Workflow Studio authors read-only access to HL7 FHIR R4 provider-directory resources. The EMR Provider Directory Sync builds on this spoke to import provider data into the Healthcare Operations data model.

## What the HL7 FHIR Spoke provides

The HL7 FHIR Spoke connects ServiceNow to any HL7 FHIR R4-conformant server. It exposes eight read-only Workflow Studio actions — a look-up-by-ID action and a search-and-stream action for each of the four FHIR R4 provider-directory resources: Organization, Location, Practitioner, and PractitionerRole. The spoke returns raw FHIR field values as data pills; it does not map them to any ServiceNow data model.

## Relationship to the EMR Provider Directory Sync

The [EMR Provider Directory Sync](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/healthcare-life-sciences/hco-fhir-landing.md) uses the HL7 FHIR Spoke as its FHIR transport layer. The spoke handles the FHIR server connection, OAuth authentication, pagination, and raw data retrieval; the EMR Provider Directory Sync owns all HCLS field mapping, upsert-key strategy, and dependency ordering. This separation keeps the spoke reusable across any flow that needs FHIR data while concentrating all Healthcare Operations logic in one place.

You must install and activate the HL7 FHIR Spoke before you can use the EMR Provider Directory Sync. See the spoke documentation for activation and connection setup steps.

## Full spoke documentation

For activation instructions, connection setup, and a complete action reference, see [HL7 FHIR Spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown) in the Integration Hub Spokes documentation.

