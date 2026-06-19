---
title: Tables installed with Service Applicant Program Management Plugin
description: This section describes the tables installed with the Service Applicant Program Management plugin and shows how they store and manage information.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/government-industry/public-sector-digital-services/psds-data-model-svc-app-prog-man-tables.html
release: australia
product: Public Sector Digital Services
classification: public-sector-digital-services
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Service Applicant, Data Model, Reference, Public Sector Digital Services \(PSDS\)]
---

# Tables installed with Service Applicant Program Management Plugin

This section describes the tables installed with the Service Applicant Program Management plugin and shows how they store and manage information.

|Table|Description|Extends Table|
|-----|-----------|-------------|
|Budget Allocation \(sn\_svc\_appl\_pgm\_mg\_budget\_allocation\)|Contains budget assignments and fund tracking for programs, including allocation amounts, spending categories, and allocation percentage.|N/A|
|Applicant Program Resource Mapping \(sn\_svc\_appl\_pgm\_mg\_resource\_mapping\)|Contains mappings between resources and any records. The resource can be a link, a document, or a knowledge article.|N/A|
|Grant Program \(sn\_svc\_appl\_pgm\_mg\_grant\_program\)|Contains grant-specific program details, including award amounts, award type, and total program budget.|Applicant Program \(sn\_svc\_appl\_pgm\_mg\_applicant\_program\)|
|Applicant Program \(sn\_svc\_appl\_pgm\_mg\_applicant\_program\)|Contains program definitions for applicant-facing initiatives, including descriptions, objectives, eligibility criteria, and application configurations.|Planning Item \(sn\_align\_core\_planning\_item\)|
|Funding Program \(sn\_svc\_appl\_pgm\_mg\_m2m\_funding\_program\)|Contains portfolio-level funding program definitions used to organize, govern, and track grant funding across one or more grant programs. Stores program details including the funding organization, program timeline, total program budget, and category.|N/A|
|Funding Program M2M Grant Program \(sn\_svc\_appl\_pgm\_mg\_m2m\_funding\_program\_to\_grant\_program\)|Contains the many-to-many relationship mappings between funding programs and grant programs. Each record links exactly one funding program to one grant program.|N/A|

**Parent Topic:**[Service Applicant Data Model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-data-model-service-applicant.md)

