---
title: Resolve entitlement import errors by using ServiceNow Otto for Software Asset Management \(SAM\)
description: Reduce manual effort when reviewing entitlement import errors in the Software Asset Workspace using ServiceNow Otto for SAM AI skills.Triggers and inputs to determine when the Software normalization skill runs and which data it uses to resolve unmatched Publisher and Product values.Triggers and inputs to determine how and when the Product match reviewer skill is used and which data it uses to select the right product match.Triggers and inputs to determine how and when the Publisher search tags generation skill is used. An input identifies the data that the skill uses, such as the raw publisher name and sample product names. A trigger initiates the skill, such as when an entitlement import error with an unresolved publisher is created.Triggers and inputs to determine how and when the Publisher match review skill is used. An input identifies the data that the skill uses, such as the candidate publisher matches in the SAM Publisher Mapping Result table. A trigger initiates the skill, such as when the matching logic creates a candidate publisher match.Triggers and inputs to determine how and when the Product search tags generation skill is used. An input identifies the data that the skill uses, such as the raw or custom product name along with its publisher name. A trigger initiates the skill, such as when a publisher is resolved.Triggers and inputs to determine how and when the Product match review skill is used. An input identifies the data that the skill uses, such as the candidate product matches in the SAM Product Mapping Result table. A trigger initiates the skill, such as when the matching logic creates a candidate product match.Triggers and inputs to determine when the Product resolution skill is used. An input identifies the data the skill uses, such as the raw product name and candidate SAM product details. A trigger initiates the skill, such as when more than one product passes Product Match Review for a raw product.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-asset-management/software-asset-management/resolve-entitlement-import-error.html
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 12
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
-   Content library portal \(sn-itam-contlookup\) - 4.0.3

</td></tr><tr><td>

Australia Patch 3 or later patches

</td><td>

Software Asset Management Professional \[com.snc.samp\]

</td><td>

-   ServiceNow Otto for Software Asset Management \(SAM\) \[sn\_now\_assist\_sam\] - 8.0.1 or later
-   Software Asset Workspace \[sn\_sam\_workspace\] - 11.0.9 or later
-   Software Asset Management AI Advance \(sn-ai-sam-advanced\) - 2.0.1
-   Content library portal \(sn-itam-contlookup\) - 4.1.0

</td></tr></tbody>
</table>Before using these skills, install the plugin and store app that match your platform release version. The skills are Publisher Search Tags Generation, Publisher Match Review, Product Search Tags Generation, Product Match Review, and Product Resolution.

|Platform release|Plugin|Store app|
|----------------|------|---------|
|Zurich Patch 13 or later patches|Software Asset Management Professional \[com.snc.samp\]|ServiceNow Otto for Software Asset Management \(SAM\) \[sn\_now\_assist\_sam\] - 13.0.0 or later|
|Australia Patch 8 or later patches|Software Asset Management Professional \[com.snc.samp\]|ServiceNow Otto for Software Asset Management \(SAM\) \[sn\_now\_assist\_sam\] - 13.0.0 or later|

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

    |Skill|Details|
    |-----|-------|
    |Software normalization|Helps you identify standardized publisher and product value from your discovered software data. This skill uses large language model \(LLM\)-driven knowledge to standardize raw, incomplete, or unrecognized publisher and product values submitted during entitlement import.|
    |Product match reviewer|Helps you confirm the correct product by analyzing search results and matching them to a predicted product name. The Product match reviewer skill is triggered after the Software normalization skill only when the Software normalization skill can’t find the correct product match.|

    **Note:** For ServiceNow Otto for SAM version 13.0.0 and later, the following skills run in sequence to provide correction suggestions for unresolved publisher or product data.

<table id="table_pqq_vnc_mjc"><thead><tr><th>

Skill

</th><th>

Details

</th></tr></thead><tbody><tr><td>

Publisher Search Tags Generation

</td><td>

Generates search tags for software publishers: normalized aliases \(acronyms, tickers, rebrands, acquisitions\) and distinctive keywords. These tags help match a publisher to its correct entry in the Content Library.

</td></tr><tr><td>

Publisher Match Review

</td><td>

Reviews candidate publisher matches from the SAM Content Library and determines whether each of them is a match or not against the source publisher, with reasoning.

</td></tr><tr><td>

Product Search Tags Generation

</td><td>

Generates search tags for software products: normalized aliases \(acronyms, short forms, renamed products\) and distinctive keywords. These tags help match a product to its correct entry in the SAM Content Library.

</td></tr><tr><td>

Product Match Review

</td><td>

Reviews candidate product matches from the SAM Content Library and determines whether each of them is a match or not against the source product, with reasoning.

</td></tr><tr><td>

Product Resolution

</td><td>

Selects the correct product for a given source product from a list of candidate SAM Content Library products.**Note:** The skill runs only when multiple products from SAM Content Library matches with the candidate product.

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

## Software normalization skill - Triggers and Inputs

Triggers and inputs to determine when the Software normalization skill runs and which data it uses to resolve unmatched Publisher and Product values.

### Triggers for the Software normalization skill

The following table lists the trigger for the Software normalization skill.

<table id="table_triggers_stns"><thead><tr><th>

Trigger

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Standard Excel import**Note:** Triggers only when the source entitlement import Excel file contains an unresolved error for a Publisher or Product value and the standard content match process has failed to resolve it.

</td><td>

The Product and Publisher data in the source Excel file don't match the Content Library data.

</td></tr></tbody>
</table>### Inputs for the Software normalization skill

The following table lists the input for the Software normalization skill.

|Input|Description|
|-----|-----------|
|Raw Publisher and Product value from source Excel file|Publisher and Product value given in standard Excel that are unresolved through standard Content Library match.|

## Product match reviewer skill - Triggers and Inputs

Triggers and inputs to determine how and when the Product match reviewer skill is used and which data it uses to select the right product match.

### Triggers for the Product match reviewer skill

The following table lists the trigger for the Product match reviewer skill.

|Trigger|Description|
|-------|-----------|
|When normalization skill doesn't have right content match|The Product match reviewer skill performs an AI-powered search and selects the correct product match. If no reliable match is found, the skill returns an empty result.|

### Inputs for the Product match reviewer skill

The following table lists the input for the Product match reviewer skill.

|Input|Description|
|-----|-----------|
|Multiple products predicted from AI-powered search|Confirmed product match from the AI-based content search result.|

## Publisher search tags generation skill - Triggers and inputs

Triggers and inputs to determine how and when the Publisher search tags generation skill is used. An input identifies the data that the skill uses, such as the raw publisher name and sample product names. A trigger initiates the skill, such as when an entitlement import error with an unresolved publisher is created.

### Triggers for the Publisher search tags generation skill

The following table lists the trigger for the Publisher search tags generation skill.

|Trigger|Description|
|-------|-----------|
|Auto-triggered|Search tags are generated automatically for a raw publisher, as the first step when an entitlement import error with unresolved publisher error is created. For custom publishers \(samp\_custom\_sw\_publisher\) created, the daily SAM - Generate Search Tags for custom Publishers and Products job generates them for new or updated records.|

### Inputs for the Publisher search tags generation skill

The following table lists the input for the Publisher search tags generation skill.

|Input|Description|
|-----|-----------|
|Software Raw Publisher \[samp\_raw\_publisher\]|The skill reads the raw publisher name and a few sample product names taken from the publisher's raw products \[samp\_raw\_product\].|
|Custom Publisher \[samp\_custom\_sw\_publisher\]|For custom publishers, the skill reads the publisher name, webpage and sample product names from the publisher's custom products \[samp\_custom\_sw\_product\].|

## Publisher match review - Triggers and inputs

Triggers and inputs to determine how and when the Publisher match review skill is used. An input identifies the data that the skill uses, such as the candidate publisher matches in the SAM Publisher Mapping Result table. A trigger initiates the skill, such as when the matching logic creates a candidate publisher match.

### Triggers for the Publisher match review skill

The following table lists the trigger for the Publisher match review skill.

|Trigger|Description|
|-------|-----------|
|Auto-triggered|Candidate publisher matches are reviewed automatically once the matching logic creates them in SAM Publisher Mapping Results table. The skill accepts or rejects each match.|

### Inputs for the Publisher match review skill

The following table lists the input for the Publisher match review skill.

|Input|Description|
|-----|-----------|
|SAM Publisher Mapping Result \[samp\_publisher\_mapping\_result\]|The skill reads each candidate match: the raw publisher name and its sample products, and the SAM publisher's name, webpage and sample products \[samp\_sw\_publisher\] and responds if its a match or not.|

## Product search tags generation skill - Triggers and inputs

Triggers and inputs to determine how and when the Product search tags generation skill is used. An input identifies the data that the skill uses, such as the raw or custom product name along with its publisher name. A trigger initiates the skill, such as when a publisher is resolved.

### Triggers for the Product search tags generation skill

The following table lists the trigger for the Product search tags generation skill.

|Trigger|Description|
|-------|-----------|
|Auto-triggered|Search tags are generated automatically for a raw products of a publisher once that publisher match passes Publisher Match Review or if publisher is already resolved. For custom products \(samp\_custom\_sw\_product\) created, the daily SAM - Generate Search Tags for custom Publishers and Products job generates them for new or updated records.|

### Inputs for the Product search tags generation skill

The following table lists the input for the Product search tags generation skill.

|Input|Description|
|-----|-----------|
|Software Raw Product \[samp\_raw\_product\]|The skill reads the raw product name along with the name of the publisher it belongs to.|
|Custom Product \[samp\_custom\_sw\_product\]|For custom products, the skill reads the product name along with the name of its publisher.|

## Product match review skill - Triggers and Inputs

Triggers and inputs to determine how and when the Product match review skill is used. An input identifies the data that the skill uses, such as the candidate product matches in the SAM Product Mapping Result table. A trigger initiates the skill, such as when the matching logic creates a candidate product match.

### Triggers for the Product match review skill

The following table lists the trigger for the Product match review skill.

|Trigger|Description|
|-------|-----------|
|Auto-triggered|Candidate product matches are reviewed automatically once the matching logic creates them in SAM Product Mapping Results table. The skill accepts or rejects each match.|

### Inputs for the Product match review skill

The following table lists the input for the Product match review skill.

|Input|Description|
|-----|-----------|
|SAM Product Mapping Result \[samp\_product\_mapping\_result\]|The skill reads each candidate match: the raw product name, and the SAM product's name, description and publisher name \[samp\_sw\_product\] and responds if its a match or not.|

## Product resolution skill - Triggers and inputs

Triggers and inputs to determine when the Product resolution skill is used. An input identifies the data the skill uses, such as the raw product name and candidate SAM product details. A trigger initiates the skill, such as when more than one product passes Product Match Review for a raw product.

### Triggers for the Product resolution skill

The following table lists the trigger for the Product resolution skill.

|Trigger|Description|
|-------|-----------|
|Auto-triggered|The skill runs automatically when more than one product passes Product Match Review for a single raw product. If only one product passes, the skill is not called.|

### Inputs for the Product resolution skill

The following table lists the input for the Product resolution skill.

<table id="table_inputs_stns"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Software Raw Product \[samp\_raw\_product\]

 SAM Product \[samp\_sw\_product\]

</td><td>

The skill reads the raw product name as the source product, along with the name and description of each candidate SAM product that passed Product Match Review.

</td></tr></tbody>
</table>