---
title: Document intelligence for utility invoices
description: The AI-driven document intelligence for utility invoices feature is designed to automate metric data collection. It automates the metric data collection by extracting utility bill data such as consumption, billing dates, amounts, and units of measurement within the Operational Sustainability Workspace.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Explore, Now Assist, Use, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Document intelligence for utility invoices

The AI-driven document intelligence for utility invoices feature is designed to automate metric data collection. It automates the metric data collection by extracting utility bill data such as consumption, billing dates, amounts, and units of measurement within the Operational Sustainability Workspace.

## Document intelligence overview

Document Intelligence for Utility Invoices automates utility bill data extraction and processing, removing manual entry for metric reporting. It streamlines the data collection process, improving accuracy and efficiency while reducing the burden on data owners. This capability addresses the challenges of manual data collection, aggregation, and entry from diverse utility bill formats and languages. It promotes consistent and reliable operational sustainability reporting.

The AI-extracted fields are clearly marked for verification, and you can override and justify changes to confirm data integrity. The original bill is attached to the metric data task for traceability and audit. After the extraction is completed, the extracted data is mapped to the correct metric definitions and entities using configurable mapping tables. The system extracts units of measurement from invoices and attempts to match them to existing units in the Metric Unit \(sn\_grc\_metric\_unit\) table. If a matching unit is found, the unit reference is populated in the Metric Data record. If no matching unit is found, the Metric Data record is created without a unit reference, the extraction status shows **Completed with Errors**, and a warning message appears on the Invoice Detail record. Data owners can review, validate, or override extracted data as needed. If the extraction process fails, you can correct the errors and rerun the extraction by selecting reprocess option.

**Note:** The sn\_esg\_gen\_ai.docintel\_user role is required to view the option to document intelligence for utility bills. This role must be manually assigned to an ESG user.

To understand how you can extract details from the utility bills, refer to [Extract data from utility invoices](extract-data-from-utility-invoices.md).

**Note:** The fields extracted by AI on the Metric Data task page must be verified for accuracy before use.

## Metric definition date restriction

When using Document Intelligence with manual metric definitions, the system only processes documents that cover standard monthly periods—where the start date is the first day of the month and the end date is the last day of the same month.

If your source documents cover irregular date ranges, use automated metric definitions instead. Automated definitions can map and process data for any date range without the first/last day restriction, providing flexibility for irregular billing cycles or custom periods. This limitation ensures consistency with operational sustainability reporting standards that require standard monthly periods for manual metric entries.

## Benefits of document intelligence for utility invoices

-   Reduces manual workload and errors in operational sustainability data collection.
-   Promotes consistency and accuracy in operational sustainability metric reporting.
-   Enhances auditability and compliance with evidence management.
-   Scales to handle diverse document types and languages.
-   Supports manual uploads and can be extended to integrate with email or other intake flows.

## Viewing extracted data summary

After the extraction and data mapping you can view the following:

-   The extracted key details from the utility bill, such as consumption, billing dates, bill amount, and units of measurement, mapped to the relevant operational sustainability metric data task.
-   The state of the extraction process \(for example, complete or failed\).
-   AI-extracted fields clearly marked for user review.
-   The option to review extracted data in the document intelligence review screen.
-   The ability to override extracted data and provide justification if needed.
-   The original utility bill attached as evidence for audit and compliance.

**Parent Topic:**[Exploring Now Assist for Operational Sustainability \(formerly ESG\)](exploring-now-assist-for-esg.md)

**Related topics**  


[Activate the document intelligence for utility invoices skill](activate-the-document-intelligence-for-utility-invoices-skill.md)

[Using Now Assist for Operational Sustainability \(formerly ESG\) skills](using-now-assist-for-esg-skills.md)

