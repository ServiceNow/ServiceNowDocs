---
title: Components installed with the HL7 FHIR Spoke
description: Several types of components are installed with the HL7 FHIR Spoke, including Workflow Studio actions, a Connection &amp; Credential Alias and configuration template, script includes, and application menu modules. The spoke installs no custom tables or roles.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/integration-hub/fhir-spoke-installed-components.html
release: australia
product: Integration Hub
classification: integration-hub
topic_type: reference
last_updated: "2026-06-16"
reading_time_minutes: 2
keywords: [installed components, FHIR actions, connection alias]
breadcrumb: [HL7 FHIR Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Components installed with the HL7 FHIR Spoke

Several types of components are installed with the HL7 FHIR Spoke, including Workflow Studio actions, a Connection &amp; Credential Alias and configuration template, script includes, and application menu modules. The spoke installs no custom tables or roles.

## Flow Designer actions installed

The spoke installs eight read-only actions, grouped into four Integration Hub categories. For each action's inputs and outputs, see [HL7 FHIR Spoke actions reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/fhir-spoke-actions.md).

|Category|Actions|
|--------|-------|
|Organization Management|Look up Organization by ID; Look up Organizations Stream|
|Location Management|Look up Location by ID; Look up Locations Stream|
|Practitioner Management|Look up Practitioner by ID; Look up Practitioners Stream|
|PractitionerRole Management|Look up PractitionerRole by ID; Look up PractitionerRoles Stream|

## Connection and credential records installed

<table><thead><tr><th>

Record

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

HL7 FHIR

</td><td>

Connection &amp; Credential Alias

</td><td>

Shared connectivity point for all eight actions. Stores the FHIR server base URL. Includes an `api_version` connection attribute \(default `baseR4`\) that selects the FHIR R4 URL fragment.

</td></tr><tr><td>

FHIR Connection Configuration

</td><td>

Configuration template

</td><td>

Attached to the `HL7 FHIR` alias to provide the guided **Add Connection** setup. Creates the HTTP connection and an OAuth 2.0 credential \(`FHIR Spoke Credential`, with application registry `FHIR Spoke OAuth`\) that use the authorization code grant with PKCE \(`S256`\). The client ID, client secret, and endpoint URL are supplied by the customer during guided setup.

</td></tr></tbody>
</table>## Script includes installed

The spoke installs four script includes that perform input validation, FHIR R4 response parsing, and stream query-string assembly for the actions. These classes support the actions internally and are not intended for direct use by other applications; their method signatures may change between releases.

|Script include|Description|
|--------------|-----------|
|`OrganizationLookUpUtil`|Pre- and post-processing for the Organization actions.|
|`LocationLookUpUtil`|Pre- and post-processing for the Location actions.|
|`PractitionerLookUpUtil`|Pre- and post-processing for the Practitioner actions.|
|`PractitionerRoleLookUpUtil`|Pre- and post-processing for the PractitionerRole actions.|

## Application menu and modules installed

The spoke adds a **FHIR App** application menu, visible to users with the `snc_internal` role, with two modules: **FHIR App Registry** \(a list of FHIR-related OAuth providers\) and **Connection Alias** \(a list of FHIR-related Connection &amp; Credential Aliases\). These modules are for administrative inspection during installation and troubleshooting.

