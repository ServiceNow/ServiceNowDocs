---
title: Healthcare Integrations
description: Connect ServiceNow Healthcare and Life Sciences with external clinical systems. Two integration approaches are available — a standards-based HL7 FHIR integration and a message-based HL7 v2.x native integration — so you can choose the approach that matches your source system and data needs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/healthcare-life-sciences/healthcare-integrations-overview.html
release: australia
topic_type: concept
last_updated: "2026-06-17"
reading_time_minutes: 1
breadcrumb: [Healthcare and Life Sciences]
---

# Healthcare Integrations

Connect ServiceNow Healthcare and Life Sciences with external clinical systems. Two integration approaches are available — a standards-based HL7 FHIR integration and a message-based HL7 v2.x native integration — so you can choose the approach that matches your source system and data needs.

Healthcare systems exchange patient, practitioner, organizational, and clinical data through established interoperability standards. ServiceNow Healthcare and Life Sciences supports two complementary integration approaches. Both bring external healthcare data onto the platform; they differ in the standard they use, how data is transported, and the source systems they suit.

## HL7 FHIR Integration

The [Healthcare Operations HL7 FHIR Integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/healthcare-life-sciences/hco-fhir-landing.md) reads HL7 FHIR R4 provider-directory resources — Organization, Location, Practitioner, and PractitionerRole — from a FHIR R4-conformant server and loads them into the Healthcare Operations data model on a schedule. Use this approach when your source system exposes a modern FHIR R4 API and you want structured, resource-oriented synchronization built in Workflow Studio.

This integration builds on the HL7 FHIR Spoke, which provides the underlying Integration Hub actions that read FHIR resources.

## HL7 v2.x Native Integration

The [Healthcare Interoperability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/healthcare-life-sciences/hl7-integration-overview.md) feature provides native HL7 v2.x messaging — connecting to an integration engine, parsing inbound messages such as ADT events, and tracking them through a message log. Use this approach when your source systems exchange traditional HL7 v2.x messages rather than FHIR resources.

