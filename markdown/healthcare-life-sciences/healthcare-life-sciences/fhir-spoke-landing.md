---
title: HL7 FHIR Spoke
description: Integrate with any HL7 FHIR R4-conformant server. The HL7 FHIR Spoke gives authors a typed, paginated, error-handled way to read FHIR R4 provider-directory resources — Organization, Location, Practitioner, and PractitionerRole — from your instance.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-06-16"
reading_time_minutes: 3
---

# HL7 FHIR Spoke

Integrate  with any HL7 FHIR R4-conformant server. The HL7 FHIR Spoke gives  authors a typed, paginated, error-handled way to read FHIR R4 provider-directory resources — Organization, Location, Practitioner, and PractitionerRole — from your  instance.

The HL7 FHIR Spoke is an  action pack that exposes eight read-only  actions — a look-up-by-ID action and a search-and-stream action for each of the four FHIR R4 provider-directory resources. Health systems expose practitioner, organizational, and location data through HL7 FHIR R4 APIs, but  has no native way to query those endpoints. Without this spoke, workflow builders write custom REST messages, script includes, and JSON parsers. The HL7 FHIR Spoke closes that gap.

The spoke is FHIR-agnostic: it returns raw FHIR field values as  data pills and does not map them to any  data model. Downstream applications, such as the Healthcare Operations HL7 FHIR Integration, compose these actions inside their own flows to persist FHIR data into  tables.

##  subscription



## Supported versions

This spoke was built for HL7 FHIR R4 and connects to any FHIR R4-conformant server. A connection attribute named `api_version` selects the FHIR R4 URL fragment \(default `baseR4`\), so you can re-point all actions to a different API path without re-authoring any flow.

## Spoke requirements

-   Access to an HL7 FHIR R4-conformant server and its base URL.
-   OAuth 2.0 client credentials registered for your instance: the authorization, token, and revoke-token endpoint URLs and the client ID and client secret. The provider uses the authorization code grant with PKCE \(`S256`\).

## Spoke dependencies

If you're having trouble installing the app, ensure that these dependent plugins are active:

-    \(com.glide.hub\)
-   Flow Designer Action Step — CORE \(com.glide.hub.action\_step.core\)
-   REST step type \(com.glide.hub.action\_step.rest\)
-    Action Template — Data Stream \(com.glide.hub.action\_type.datastream\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The HL7 FHIR Spoke provides actions to read FHIR R4 provider-directory resources from your  instance. For each resource, a look-up-by-ID action retrieves a single resource by its FHIR logical ID, and a stream action searches the resource with optional FHIR R4 search parameters and streams one resource per item, following each FHIR Bundle `next` link automatically until the server stops paging. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Organization Management|Look up Organization by ID|Retrieves a single FHIR Organization resource by its logical ID.|
|Look up Organizations Stream|Searches and streams Organization resources with automatic pagination.|
|Location Management|Look up Location by ID|Retrieves a single FHIR Location resource by its logical ID.|
|Look up Locations Stream|Searches and streams Location resources with automatic pagination.|
|Practitioner Management|Look up Practitioner by ID|Retrieves a single FHIR Practitioner resource by its logical ID.|
|Look up Practitioners Stream|Searches and streams Practitioner resources with automatic pagination.|
|PractitionerRole Management|Look up PractitionerRole by ID|Retrieves a single FHIR PractitionerRole resource by its logical ID.|
|Look up PractitionerRoles Stream|Searches and streams PractitionerRole resources with automatic pagination.|

All actions are read-only \(HTTP GET\). Write operations, real-time event triggers such as CDS Hooks or FHIR subscriptions, and FHIR resources beyond the four provider-directory resources are out of scope. For the inputs and outputs of each action, see [HL7 FHIR Spoke actions reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown).

**Note:** Spoke actions return raw FHIR field values; the consuming flow owns all persistence and field mapping.

## Connection and credential alias requirements

All eight actions route through a single Connection &amp; Credential Alias named `HL7 FHIR`, so the FHIR server URL and OAuth credentials are bound once at install time and reused by every action.

 [Activate the HL7 FHIR Spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown).

