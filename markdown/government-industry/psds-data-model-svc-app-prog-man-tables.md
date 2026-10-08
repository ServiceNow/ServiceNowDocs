---
title: Tables installed with Service Applicant Program Management Plugin
description: This section describes the tables installed with the Service Applicant Program Management plugin and shows how they store and manage information.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/government-industry/psds-data-model-svc-app-prog-man-tables.html
release: zurich
topic_type: concept
last_updated: "2025-11-17"
reading_time_minutes: 1
breadcrumb: [Service Applicant, Data Model, Reference, Public Sector Digital Services \(PSDS\)]
---

# Tables installed with Service Applicant Program Management Plugin

This section describes the tables installed with the Service Applicant Program Management plugin and shows how they store and manage information.

|Table|Description|Extends Table|
|-----|-----------|-------------|
|Budget Allocation|Contains budget assignments and fund tracking for programs, including allocation amounts, spending categories, and allocation percentage.|N/A|
|Applicant Program Resource Mapping|Contains mappings between resources and any records. The resource can be a link, a document, or a knowledge article.|N/A|
|Grant Program|Contains grant-specific program details, including award amounts, award type, and total award budget allocated.|Applicant Program|
|Applicant Program|Contains program definitions for applicant-facing initiatives, including descriptions, objectives, eligibility criteria, and application configurations.|Planning Item|
|Funding Program|Contains portfolio-level funding program definitions used to organize, govern, and track grant funding across one or more grant programs. Stores program details including the funding organization, program timeline, total program budget, and category.|N/A|
|Funding Program M2M Grant Program|Contains the many-to-many relationship mappings between funding programs and grant programs. Each record links exactly one funding program to one grant program.|N/A|

**Parent Topic:**[Service Applicant Data Model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/government-industry/psds-data-model-service-applicant.md)

