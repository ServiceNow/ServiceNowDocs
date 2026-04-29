---
title: Tables installed with Service Applicant Program Management Plugin
description: This section describes the tables installed with the Service Applicant Program Management plugin and shows how they store and manage information.
locale: en-US
release: australia
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

**Parent Topic:**[Service Applicant Data Model](psds-data-model-service-applicant.md)

