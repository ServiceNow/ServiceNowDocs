---
title: HL7 FHIR Spoke release notes
description: The ServiceNow HL7 FHIR Spoke application lets Workflow Studio authors read HL7 FHIR R4 provider-directory resources from any FHIR R4-conformant server without writing custom REST, scripting, or pagination code. HL7 FHIR Spoke is a new application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/fhir-spoke-release-notes-rn.html
release: australia
topic_type: reference
last_updated: "2026-06-16"
reading_time_minutes: 2
keywords: [HL7 FHIR Spoke, FHIR, FHIR R4, Integration Hub, release notes]
breadcrumb: [Healthcare and Life Sciences release notes, Features and changes by product, Release notes for upgrading from Zurich, Learn about the Australia release, Australia release notes]
---

# HL7 FHIR Spoke release notes

The ServiceNow® HL7 FHIR Spoke application lets Workflow Studio authors read HL7 FHIR R4 provider-directory resources from any FHIR R4-conformant server without writing custom REST, scripting, or pagination code. HL7 FHIR Spoke is a new application.

## HL7 FHIR Spoke highlights

-   Read FHIR R4 Organization, Location, Practitioner, and PractitionerRole resources from any FHIR R4-conformant server using eight pre-built Integration Hub actions.
-   Retrieve a single resource by its logical ID, or search and stream multiple resources with pagination handled automatically.
-   Configure connectivity once through a shared Connection &amp; Credential Alias that uses OAuth 2.0 authorization code flow with PKCE.
-   Build FHIR integrations entirely in Workflow Studio — no custom REST messages, script includes, or JSON parsing required.

See HL7 FHIR Spoke for more information.

**Important:** HL7 FHIR Spoke is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## HL7 FHIR Spoke features

-   **HL7 FHIR Spoke actions reference**

    Look up a single FHIR Organization, Location, Practitioner, or PractitionerRole by its logical ID and receive every resource field as a typed Workflow Studio data pill, along with an action status that lets you handle "not found" without aborting the flow.

-   **HL7 FHIR Spoke actions reference**

    Search any of the four resources with optional FHIR R4 search parameters and stream one resource per item. The spoke walks each FHIR Bundle `next` link automatically until the server stops paging.

-   **Configure the HL7 FHIR connection and credentials**

    All eight actions authenticate through a single `HL7 FHIR` Connection &amp; Credential Alias, so you bind the FHIR server URL and OAuth credentials once and reuse them everywhere.


## Activation information

Install HL7 FHIR Spoke by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

Before deploying the spoke, the following platform plugins must be active: Workflow Studio \(com.glide.hub\), Flow Designer Action Step — CORE \(com.glide.hub.action\_step.core\), the REST step type \(com.glide.hub.action\_step.rest\), and the Integration Hub Action Template — Data Stream \(com.glide.hub.action\_type.datastream\).

## Plugin information

-   **New plugins**

    The following plugins are new in Australia:

    HL7 FHIR Spoke \(`sn_hl7_fhir_spoke`\): Provides read-only FHIR R4 Flow Designer actions for reading Organization, Location, Practitioner, and PractitionerRole resources from any FHIR R4-conformant server.


## Related ServiceNow applications and features

-   **EMR Provider Directory Sync**

    Consumes the HL7 FHIR Spoke actions to import FHIR provider-directory data into the Healthcare Operations data model on a schedule.


**Parent Topic:**[Healthcare and Life Sciences release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/healthcare-life-sciences-rn-landing.md)

