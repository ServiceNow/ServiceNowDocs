---
title: Categorize discovered browser extensions
description: Group discovered browser extensions in your environment by business relevance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/agent-client-collector/acc-categorize-browser-extensions.html
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-09-02"
reading_time_minutes: 2
keywords: [browser extension categorization, browser extension signatures, ACC-VC]
breadcrumb: [Browser extension discovery and categorization, ACC deployment - endpoints, Agent Client Collector, IT Operations Management]
---

# Categorize discovered browser extensions

Group discovered browser extensions in your environment by business relevance.

## Before you begin

Role required: discovery\_admin

## About this task

Browser extension discovery finds the extensions on your endpoints and maps the category to which each extension belongs, along with the devices where it is installed. For an extension to appear in the inventory, create a signature and assign it a category to classify the matching extensions.

**Important:** If the system property sn\_acc\_vis\_content.full\_browser\_extension\_discovery is set to True, all browser extensions will be discovered, but those that don't have a matching user-defined signature will not have a category assigned to them. If this system property is set to False, only browser extensions that are matched with signatures will be discovered.

## Procedure

1.  Create a category.

    1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

    2.  Open the **Entity Categories** \(sn\_acc\_vis\_content\_entity\_category\) table.

    3.  Under related links, select **Show List**.

    4.  Select **New**.

    5.  On the form, fill in the fields.

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The display name of the category. This field is required.For example: Adobe Acrobat, AI Tools, or Microsoft.

</td></tr><tr><td>

Description

</td><td>

Brief description of the category.

</td></tr><tr><td>

Active

</td><td>

When selected, activates the category. **Note:** You can also activate a saved category later from the **Entity Categories** table.

</td></tr></tbody>
</table>    6.  Select **Submit**.

    7.  View the saved categories in the **Entity Categories** table.

        **Note:** You can activate saved categories from this table by setting Active=true for the relevant categories.

2.  Create a signature.

    The signature is a rule that matches extensions to a category based on the extension ID or name.

    1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

    2.  Open the **Browser Extension Signature** \(sn\_acc\_vis\_content\_browser\_extension\_signature\) table.

    3.  Under related links, select **Show List**.

    4.  Select **New**.

    5.  On the form, fill in the fields.

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The display name of the signature. This field is required.For example: ChatGPT.

</td></tr><tr><td>

Extension ID

</td><td>

The extension ID that matches the extension ID that is unique across vendors.

</td></tr><tr><td>

Extension name condition

</td><td>

Matching condition for the extension name. Options are: Exact match, Contains, Starts with, and Ends with.

</td></tr><tr><td>

Extension name

</td><td>

The pattern to match against the extension name.For example: ChatGPT.

</td></tr><tr><td>

Version condition

</td><td>

Matching condition for the version. Options are: Any version, Exact match, Starts with, Ends with, Contains, Less than, Greater than, Not empty, and Empty.

</td></tr><tr><td>

Version

</td><td>

Pattern to match against the version.**Note:** If you don't specify a version, the signature matches any version.

</td></tr><tr><td>

Category

</td><td>

Category assigned to matching browser extensions.

</td></tr><tr><td>

Description

</td><td>

Brief description of the signature.For example: Extensions related to ChatGPT.

</td></tr><tr><td>

Active

</td><td>

When selected, activates the signature.

</td></tr></tbody>
</table>    6.  Select **Submit**.

    Submitting the signature triggers evaluation of browser extensions against it and categorization of any matches.

3.  Fetch metadata of the discovered browser extensions.

    1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

    2.  Set the system property `sn_acc_vis_content.collect_extended_browser_extension_metadata` to True to collect the metadata.

    3.  Review the fetched metadata.

        1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.
        2.  Open the **Browser Extension Metadata** \(sn\_acc\_vis\_content\_browser\_extension\_metadata\) table.
        3.  Review the metadata.

## Result

The categorized browser extensions in your environment appear in the **Browser Extension Catalogs** \(sn\_acc\_vis\_content\_browser\_extension\_catalog\) table. Each entry in the table shows the browser extension, its assigned category, extension ID, version, and the signature that matched. Filter by category to see all the browser extensions in the group.

The **Device Browser Extensions** \(sn\_acc\_vis\_content\_device\_browser\_extension\) table shows the mapping of the discovered browser extensions for each browser and device, and their profile and status.

