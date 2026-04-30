---
title: Document intelligence for utility invoices
description: The AI-driven document intelligence for utility invoices feature is designed to automate metric data collection. It automates the metric data collection by extracting utility bill data, such as consumption, billing dates, and amounts, within the Operational Sustainability Workspace.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-09-05"
reading_time_minutes: 2
breadcrumb: [Explore, Now Assist for Operational Sustainability, Use, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Document intelligence for utility invoices

The AI-driven document intelligence for utility invoices feature is designed to automate metric data collection. It automates the metric data collection by extracting utility bill data, such as consumption, billing dates, and amounts, within the Operational Sustainability Workspace.

## Document Intelligence overview

Document Intelligence for utility invoices automates utility bill data extraction and processing. By streamlining the data collection process, including data collection, aggregation, and entry, this feature helps improve accuracy and efficiency while easing the burden on data owners.

The AI-extracted fields are marked so you can verify, override, or justify changes. The original bill is attached to the metric data task. After it's extracted, the data, including consumption, billing dates, and bill amount, is mapped to the correct metric definitions and entities using configurable mapping tables. Data owners can review, validate, or override extracted data as needed. If the extraction process fails, you can correct the errors and rerun the extraction by selecting the reprocess option.

**Note:** The sn\_esg\_gen\_ai.docintel\_user role is required to view the option to document intelligence for utility bills. This role must be manually assigned to an ESG user.

For instructions on extracting details from utility bills, refer to [Extract data from utility invoices](extract-data-from-utility-invoices.md).

**Note:** The fields extracted by AI on the Metric Data task page must be verified for accuracy before use.

## Restriction on manual metric definition dates

When using Document Intelligence with manual metric definitions, the system only processes documents that cover standard monthly periods—where the start date is the first day of the month and the end date is the last day of the same month.

If your source documents cover irregular date ranges, you can use automated metric definitions, which can map and process data for any date range.

**Parent Topic:**[Exploring Now Assist for Operational Sustainability](exploring-now-assist-for-esg.md)

**Related topics**  


[Activate the document intelligence for utility invoices skill](activate-the-document-intelligence-for-utility-invoices-skill.md)

[Using Now Assist for Operational Sustainability skills](using-now-assist-for-esg-skills.md)

