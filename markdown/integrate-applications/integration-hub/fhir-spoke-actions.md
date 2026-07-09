---
title: HL7 FHIR Spoke actions reference
description: The HL7 FHIR Spoke provides eight read-only Workflow Studio actions — a look-up-by-ID action and a stream action for each of the four FHIR R4 provider-directory resources. This reference lists the key inputs and outputs of each action.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/integration-hub/fhir-spoke-actions.html
release: australia
product: Integration Hub
classification: integration-hub
topic_type: reference
last_updated: "2026-06-16"
reading_time_minutes: 2
keywords: [FHIR actions, inputs, outputs, FHIR search parameters]
breadcrumb: [HL7 FHIR Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# HL7 FHIR Spoke actions reference

The HL7 FHIR Spoke provides eight read-only Workflow Studio actions — a look-up-by-ID action and a stream action for each of the four FHIR R4 provider-directory resources. This reference lists the key inputs and outputs of each action.

## Outputs common to all actions

Every action returns an action status \(a code and a message\). Look-up-by-ID actions also expose a **Don't treat as error** option that lets a flow continue when a resource is not found. Stream actions additionally return page and item counts and transport **status code**, **error code**, and **error message** outputs.

Stream-action search inputs map directly to FHIR R4 search parameters. For the complete parameter set and prefix syntax, see the [HL7 FHIR R4 search specification](https://hl7.org/fhir/R4/search.html).

## Organization actions

|Action|Key inputs|Key outputs|
|------|----------|-----------|
|Look up Organization by ID|Organization ID \(required\)|id, active, name, alias, type code and display, telecom, address, part of, contact|
|Look up Organizations Stream|Page size \(required\); optional: name, active, type, identifier, part of, address fields, last updated, and other FHIR R4 search parameters|Per-item Organization fields \(as above\); page count, item count, count|

## Location actions

|Action|Key inputs|Key outputs|
|------|----------|-----------|
|Look up Location by ID|Location ID \(required\)|id, name, description, status, operational status, mode, physical type, type, telecom, address, latitude, longitude, managing organization, part of|
|Look up Locations Stream|Page size \(required\); optional: name, status, operational status, location type, identifier, managing organization, part of, near, address fields, and other FHIR R4 search parameters|Per-item Location fields \(as above\); page count, item count, count|

## Practitioner actions

|Action|Key inputs|Key outputs|
|------|----------|-----------|
|Look up Practitioner by ID|Practitioner ID \(required\)|id, name text, family, given, prefix, suffix, gender, birth date, active, telecom, address, communication language, qualification code and display and issuer|
|Look up Practitioners Stream|Page size \(required\); optional: name, given name, family name, identifier, active, gender, communication language, email, phone, address fields, and other FHIR R4 search parameters|Per-item Practitioner fields \(as above\); page count, item count, count|

## PractitionerRole actions

|Action|Key inputs|Key outputs|
|------|----------|-----------|
|Look up PractitionerRole by ID|PractitionerRole ID \(required\)|id, role code and display, specialty code and display, active, practitioner reference, organization reference, location reference, period start and end, telecom, availability exception|
|Look up PractitionerRoles Stream|Page size \(required\); optional: practitioner, organization, location, role, specialty, identifier, active, date, phone, email, and other FHIR R4 search parameters|Per-item PractitionerRole fields \(as above\); page count, item count, count|

