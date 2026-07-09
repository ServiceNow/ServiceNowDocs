---
title: HL7 FHIR Spoke
description: Integrate ServiceNow with any HL7 FHIR R4-conformant server. The HL7 FHIR Spoke gives Workflow Studio authors a typed, paginated, error-handled way to read FHIR R4 provider-directory resources — Organization, Location, Practitioner, and PractitionerRole — from your ServiceNow instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/integration-hub/fhir-spoke-landing.html
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-06-16"
reading_time_minutes: 4
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# HL7 FHIR Spoke

Integrate ServiceNow with any HL7 FHIR R4-conformant server. The HL7 FHIR Spoke gives Workflow Studio authors a typed, paginated, error-handled way to read FHIR R4 provider-directory resources — Organization, Location, Practitioner, and PractitionerRole — from your ServiceNow instance.

The HL7 FHIR Spoke is an Integration Hub action pack that exposes eight read-only Workflow Studio actions — a look-up-by-ID action and a search-and-stream action for each of the four FHIR R4 provider-directory resources. Health systems expose practitioner, organizational, and location data through HL7 FHIR R4 APIs, but Workflow Studio has no native way to query those endpoints. Without this spoke, workflow builders write custom REST messages, script includes, and JSON parsers. The HL7 FHIR Spoke closes that gap.

The spoke is FHIR-agnostic: it returns raw FHIR field values as Workflow Studio data pills and does not map them to any ServiceNow data model. Downstream applications, such as the Healthcare Operations HL7 FHIR Integration, compose these actions inside their own flows to persist FHIR data into ServiceNow tables.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Supported versions

This spoke was built for HL7 FHIR R4 and connects to any FHIR R4-conformant server. A connection attribute named `api_version` selects the FHIR R4 URL fragment \(default `baseR4`\), so you can re-point all actions to a different API path without re-authoring any flow.

## Spoke requirements

-   Access to an HL7 FHIR R4-conformant server and its base URL.
-   OAuth 2.0 client credentials registered for your instance: the authorization, token, and revoke-token endpoint URLs and the client ID and client secret. The provider uses the authorization code grant with PKCE \(`S256`\).

## Spoke dependencies

If you're having trouble installing the app, ensure that these dependent plugins are active:

-   Workflow Studio \(com.glide.hub\)
-   Flow Designer Action Step — CORE \(com.glide.hub.action\_step.core\)
-   REST step type \(com.glide.hub.action\_step.rest\)
-   Integration Hub Action Template — Data Stream \(com.glide.hub.action\_type.datastream\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The HL7 FHIR Spoke provides actions to read FHIR R4 provider-directory resources from your ServiceNow instance. For each resource, a look-up-by-ID action retrieves a single resource by its FHIR logical ID, and a stream action searches the resource with optional FHIR R4 search parameters and streams one resource per item, following each FHIR Bundle `next` link automatically until the server stops paging. Available actions include:

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

All actions are read-only \(HTTP GET\). Write operations, real-time event triggers such as CDS Hooks or FHIR subscriptions, and FHIR resources beyond the four provider-directory resources are out of scope. For the inputs and outputs of each action, see [HL7 FHIR Spoke actions reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/fhir-spoke-actions.md).

**Note:** Spoke actions return raw FHIR field values; the consuming flow owns all persistence and field mapping.

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/r-credentials.md).

All eight actions route through a single Connection &amp; Credential Alias named `HL7 FHIR`, so the FHIR server URL and OAuth credentials are bound once at install time and reused by every action.

For information about setting up the spoke, see [Activate the HL7 FHIR Spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/fhir-spoke-activate.md).

