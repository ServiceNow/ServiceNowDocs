---
title: Resolve entitlement import errors by using ServiceNow Otto for Software Asset Management \(SAM\)
description: Reduce manual effort when reviewing entitlement import errors in the Software Asset Workspace using ServiceNow Otto for SAM AI skills.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-asset-management/software-asset-management/resolve-entitlement-import-error.html
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 8
keywords: [Software Normalization skill, Product Match Reviewer skill, resolve entitlement import errors,]
breadcrumb: [Use generative AI skills, Using AI in Software Asset Management, Software Asset Management, IT Asset Management, Asset Management]
---

# Resolve entitlement import errors by using ServiceNow Otto for Software Asset Management \(SAM\)

Reduce manual effort when reviewing entitlement import errors in the Software Asset Workspace using ServiceNow Otto for SAM AI skills.

## Before you begin

Before you use the Product match reviewer and Software normalization skills, install the following plugin and the store apps that match your platform release version.

<table id="table_contract_ent_plugins"><thead><tr><th>

Platform release

</th><th>

Plugin

</th><th>

Store apps

</th></tr></thead><tbody><tr><td>

Zurich Patch 10 or later patches

</td><td>

Software Asset Management Professional \[com.snc.samp\]

</td><td>

-   ServiceNow Otto for Software Asset Management \(SAM\) \[sn\_now\_assist\_sam\] - 8.0.1 or later
-   Software Asset Workspace \[sn\_sam\_workspace\] - 10.0.13 or later

</td></tr><tr><td>

Australia Patch 3 or later patches

</td><td>

Software Asset Management Professional \[com.snc.samp\]

</td><td>

-   ServiceNow Otto for Software Asset Management \(SAM\) \[sn\_now\_assist\_sam\] - 8.0.1 or later
-   Software Asset Workspace \[sn\_sam\_workspace\] - 11.0.9 or later

</td></tr></tbody>
</table>Before using these skills, install the plugin and store app that match your platform release version. The skills are Publisher Search Tags Generation, Publisher Match Review, Product Search Tags Generation, Product Match Review, and Product Resolution.

|Platform release|Plugin|Store app|
|----------------|------|---------|
|Zurich Patch 13 or later patches|Software Asset Management Professional \[com.snc.samp\]|ServiceNow Otto for Software Asset Management \(SAM\) \[sn\_now\_assist\_sam\] - 13.0.0 or later|
|Australia Patch 8 or later patches|Software Asset Management Professional \[com.snc.samp\]|ServiceNow Otto for Software Asset Management \(SAM\) \[sn\_now\_assist\_sam\] - 13.0.0 or later|
|Brazil Patch 2 or later patches|Software Asset Management Professional \[com.snc.samp\]|ServiceNow Otto for Software Asset Management \(SAM\) \[sn\_now\_assist\_sam\] - 13.0.0 or later|

Role required: sam\_user or sam\_admin

## About this task

**Important:** This generative AI skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

**Note:** The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.

Starting with the Australia Patch 4 release, AWS Claude is the default model provider for the Product match reviewer. For the Software normalization AI skill, Google Gemini is the default model provider.

Starting with the Zurich Patch 13 release, Australia Patch 8 release, and Brazil Patch 2 release, AWS Claude is the default model provider for the skill used for normalize publishers and products.

When you import software entitlements using the [Import bulk entitlements in the Software Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/import-entitlements-workspace.md) feature, some rows may contain publisher or product data that standard content matching can't resolve. Unresolved publisher or product data prevents the entitlement import from completing successfully.

After the file import completes, the skills check publisher and product names. If any name is misspelled, incomplete, or unrecognized, they run automatically to identify the correct value and provide a correction.

## Procedure

1.  Navigate to **All** &gt; **Software Asset** &gt; **Software Asset Workspace**.

2.  Select **Create entitlement**.

3.  In the Create new entitlement dialog box, select **Import multiple entitlements from an Excel file**.

4.  Select **Next**.

5.  Upload a Microsoft Excel file.

    For more information about importing multiple entitlements, see [Import bulk entitlements in workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/import-entitlements-workspace.md).

    **Note:** The error resolution for the **Product** and **Publisher** fields applies only when the **Import Type** field value is selected as **Standard Import document**.

    **Note:** The following skills are available for ServiceNow Otto for SAM versions before 13.0.0. These skills run in sequence to provide correction suggestions for unresolved publisher or product data.

<table id="table_aqq_jw3_clc"><thead><tr><th>

Skill

</th><th>

Details

</th></tr></thead><tbody><tr><td>

Software normalization

</td><td>

Helps you identify standardized publisher and product value from your discovered software data. This skill uses large language model \(LLM\)-driven knowledge to standardize raw, incomplete, or unrecognized publisher and product values submitted during entitlement import.For information on triggers and inputs for Software normalization skill, see [Software normalization skill - Triggers and Inputs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/software-normalization-triggers-inputs.md).

</td></tr><tr><td>

Product match reviewer

</td><td>

Helps you confirm the correct product by analyzing search results and matching them to a predicted product name. The Product match reviewer skill is triggered after the Software normalization skill only when the Software normalization skill can’t find the correct product match.For information on triggers and inputs for Software normalization skill, see [Product match reviewer skill - Triggers and Inputs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/product-match-reviewer-triggers-inputs.md).

</td></tr></tbody>
</table>    **Note:** For ServiceNow Otto for SAM version 13.0.0 and later, the following skills run in sequence to provide correction suggestions for unresolved publisher or product data.

<table id="table_pqq_vnc_mjc"><thead><tr><th>

Skill

</th><th>

Details

</th></tr></thead><tbody><tr><td>

Publisher Search Tags Generation

</td><td>

Generates search tags for software publishers: normalized aliases \(acronyms, tickers, rebrands, acquisitions\) and distinctive keywords. These tags help match a publisher to its correct entry in the Content Library.For information on triggers and inputs for Publisher Search Tags Generation skill, see [Publisher search tags generation skill - Triggers and inputs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/publisher-search-tags-generation-triggers-inputs.md).

</td></tr><tr><td>

Publisher Match Review

</td><td>

Reviews candidate publisher matches from the SAM Content Library and determines whether each of them is a match or not against the source publisher, with reasoning.For information on triggers and inputs for Publisher Match Review skill, see [Publisher match review - Triggers and inputs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/publisher-match-review-triggers-inputs.md).

</td></tr><tr><td>

Product Search Tags Generation

</td><td>

Generates search tags for software products: normalized aliases \(acronyms, short forms, renamed products\) and distinctive keywords. These tags help match a product to its correct entry in the SAM Content Library.For information on triggers and inputs for Product Search Tags Generation skill, see [Product search tags generation skill - Triggers and inputs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/product-search-tags-generation-triggers-inputs.md).

</td></tr><tr><td>

Product Match Review

</td><td>

Reviews candidate product matches from the SAM Content Library and determines whether each of them is a match or not against the source product, with reasoning.For information on triggers and inputs for Product Match Review skill, see [Product match review skill - Triggers and Inputs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/product-match-review-triggers-inputs.md).

</td></tr><tr><td>

Product Resolution

</td><td>

Selects the correct product for a given source product from a list of candidate SAM Content Library products.**Note:** The skill runs only when multiple products from SAM Content Library matches with the candidate product.

For information on triggers and inputs for Product Resolution skill, see [Product resolution skill - Triggers and inputs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/product-resolution-triggers-inputs.md).

</td></tr></tbody>
</table>6.  Select the **Errors** tab.

    The **Errors** tab displays all entitlement import error records that require human attention. These records fall into the following categories:

    -   Records where the AI skills have provided a suggested correction that requires your review. In the Error status column, the Otto icon \[Omitted image "icon-otto-outline-24.svg"\] Alt text: indicates that the record contains an AI suggestion.
    -   Records where the AI skills were unable to resolve the import error and provide a correction. Review these records and manually update the publisher or product values to resolve the error.
7.  Select the number link to open the import error record.

    If the import error record contains an AI-suggested value, an Otto icon \[Omitted image "icon-otto-outline-24.svg"\] Alt text: Otto icon is displayed on the field. The icon shows both the AI-corrected value and the original value from the import file.

8.  Review the AI-corrected value for each field.

9.  Select **Import** to save and import the reviewed record.


## Result

-   After the import is complete, an entitlement record is created and displayed on the **Entitlements** tab.
-   The import error record is removed from the **Errors** tab.
-   The Entitlement creation widget in the AI activity section of the Software Asset overview page is updated. The widget displays the number of entitlement import errors requiring review. Select the link to view the Entitlement Import Error list.

    \[Omitted image "import-errors-require-review.png"\] Alt text: Import errors to review


**Parent Topic:**[Using generative AI skills in ServiceNow Otto for Software Asset Management \(SAM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/using-now-assist-sam.md)

**Related topics**  


[Import bulk entitlements in workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/import-entitlements-workspace.md)

