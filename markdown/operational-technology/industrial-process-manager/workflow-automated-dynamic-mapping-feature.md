---
title: Workflow for the automated mapping feature
description: The Industrial Process Manager includes an automated flow for the automated mapping feature.
locale: en-US
release: zurich
product: Industrial Process Manager
classification: industrial-process-manager
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Automated Mapping Across Zone-based IP Network Groups, Managing equipment models, Use, Industrial Process Manager, Operational Technology]
---

# Workflow for the automated mapping feature

The Industrial Process Manager includes an automated flow for the automated mapping feature.

A predefined flows is included with this feature that you can use to schedule the assignment of OT devices to equipment model entities.

By using [Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer&version=zurich&pubname=zurich-application-development&ft:locale=en-US), you can review and configure the predefined flow for your business needs.

## Flow available for this feature

The following table lists the predefined flow that is available with the Industrial Process Manager when installed with Operational Technology Manager.

|Application|Flow|
|-----------|----|
|Industrial Process Manager when installed with Operational Technology Manager|OT device mapping flow|

## General use cases for the automated mapping feature

These use cases typically apply for the automated mapping feature:

-   An OT manager has existing OT devices and wants to map individual OT devices​ on demand.
-   An OT admin wants to automatically map newly detected OT devices with valid IP addresses to an equipment model entity.

The following is a typical workflow for the automated mapping feature.

-   A system admin imports OT subnet data into the OT subnet mapping table from an Excel spreadsheet using [Easy Import](https://www.servicenow.com/docs/access?context=c_EasyImport&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US).
-   Either the Amazing admin reviews the imported data records and associates \(maps\) OT subnet mapping records to a site and/or the Equipment Model Entity within that site.
-   The Amazing admin activates or triggers the scheduled flow to automatically map OT devices for all sites on an instance.
-   The Amazing editor can update the records that belong to the sites that they have editing access to.

**Parent Topic:**[Automated Mapping Across Zone-based IP Network Groups](../task/automate-mappings-between-ot-assets-and-equipment-model-entity.md)

