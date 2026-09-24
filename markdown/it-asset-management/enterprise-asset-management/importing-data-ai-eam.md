---
title: Importing enterprise models and assets using AI assistance
description: You can import enterprise models and assets with minimal human intervention by using AI-assisted import.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/enterprise-asset-management/importing-data-ai-eam.html
release: brazil
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Bulk import of your enterprise models and assets, Managing enterprise models and assets, Enterprise Asset Management, Asset Management]
---

# Importing enterprise models and assets using AI assistance

You can import enterprise models and assets with minimal human intervention by using AI-assisted import.

AI-assisted import simplifies and streamlines the import process by automatically recommending mapping strategies between your external model and asset data and the corresponding Enterprise Asset Management tables and data model components. AI-assisted import can also help you identify import errors automatically.

## AI-assisted import stages

The AI-assisted import process consists of the following stages:

1.  Import details: Define general details for the import, including the import name and import source file.
2.  Column mapping: Define the column mappings that you want to apply to your imports.
3.  Value mapping: Define the value mappings that you want to apply to your imports.
4.  Review and import: Review and resolve all import data errors and then initiate the import.
5.  Summary: Review the summary of your import results.

Throughout the import process, the Enterprise Asset Management application leverages various skills to help you complete each stage.

-   During the Column mapping and Value mapping stages, the application leverages the ServiceNow AI Lens skill to generate AI suggestions. You can accept these suggestions, override them manually, or run additional passes to refine them.
-   During the Review and import stage, the application leverages the ServiceNow AI Lens skill to automatically identify import data errors. You can review and resolve these errors as needed.
-   During the Review and import stage for your enterprise model imports, the application leverages the populate model category skill to populate missing model categories for your enterprise models. The application also leverages the populate classification skill to populate missing classifications for your enterprise models, based on the Enterprise Asset Management data model. For more information on the Enterprise Asset Management data model and model categories, see [Enterprise Asset Management data model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/enterprise-asset-management/eam-data-model.md).

For more information on the ServiceNow AI Lens skill, see [ServiceNow AI Lens skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/servicenow-lens-skill.md).

## Benefits

AI-assisted import can help provide the following benefits:

-   Reduces manual effort by handling initial column and value mappings, identifying import data errors, and enabling you to reuse templates from previous imports.
-   Improves data consistency by standardizing variations in your table columns and data values. Your data is more reliable for cost tracking, asset life-cycle analysis, and strategic decision-making.

-   **[Import enterprise models and assets using AI assistance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/enterprise-asset-management/import-data-ai-eam.md)**  
Import enterprise models and assets with minimal human intervention by using AI-assisted import.

**Parent Topic:**[Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/asset-management/asset-management-landing-page.md)

