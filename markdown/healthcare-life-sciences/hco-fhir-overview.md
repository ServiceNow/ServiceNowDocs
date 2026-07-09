---
title: What the EMR Provider Directory Sync does
description: The EMR Provider Directory Sync imports provider-directory data from a FHIR R4 server into the Healthcare Operations data model on a schedule, so that organizations, locations, practitioners, and care-team memberships stay current without manual maintenance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/healthcare-life-sciences/hco-fhir-overview.html
release: australia
topic_type: concept
last_updated: "2026-06-16"
reading_time_minutes: 1
keywords: [FHIR integration, Healthcare Operations, provider directory, data sync]
breadcrumb: [EMR Provider Directory Sync, Healthcare Integrations, Healthcare and Life Sciences]
---

# What the EMR Provider Directory Sync does

The EMR Provider Directory Sync imports provider-directory data from a FHIR R4 server into the Healthcare Operations data model on a schedule, so that organizations, locations, practitioners, and care-team memberships stay current without manual maintenance.

Healthcare Operations workflows in ServiceNow depend on accurate organization hierarchy, facility, and practitioner data. When that data is maintained manually, it drifts from the customer's EMR, which is the operational source of truth. This application closes that gap by importing four FHIR R4 provider-directory resources on a schedule and upserting them into the Healthcare Operations data model.

## What it imports

The integration imports four FHIR R4 resources and writes them to the Healthcare Operations data model:

-   FHIR Organizations become Healthcare Organization records and internal or external business locations.
-   FHIR Locations become Healthcare Location records and platform location records, optionally associated with a managing organization.
-   FHIR Practitioners become user records and Healthcare Practitioner records, each granted the care-team-member role.
-   FHIR PractitionerRoles become service organization membership records that place a practitioner on a care team for an organization.

## Relationship to the HL7 FHIR Spoke

This application builds on the [HL7 FHIR Spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown). The spoke provides the read-only FHIR actions and returns raw FHIR field values; this application owns the EMR-to-HCLS field mapping, the upsert key strategy \(the FHIR resource ID as the external identifier\), and the dependency ordering. This separation keeps the spoke reusable while concentrating all Healthcare Operations logic in one place.

## What is out of scope

The integration is read-only against the FHIR server — it does not write back to the EMR. Real-time, event-driven sync \(such as CDS Hooks or FHIR subscriptions\) and FHIR resources beyond the four provider-directory resources are out of scope. There is no user-facing portal; the application is operated by Healthcare Operations administrators.

