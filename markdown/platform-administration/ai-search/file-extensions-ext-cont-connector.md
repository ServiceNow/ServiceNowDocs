---
title: Binary file extensions supported in External Content Connectors
description: Connector administrators can restrict the binary file types an external content connector retrieves by specifying file extensions in inclusion or exclusion filters.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: reference
last_updated: "2025-10-28"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Reference, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Binary file extensions supported in External Content Connectors

Connector administrators can restrict the binary file types an external content connector retrieves by specifying file extensions in inclusion or exclusion filters.

<table id="table_ink_3mv_sdc"><thead><tr><th>

Binary file type

</th><th>

Supported file extensions

</th></tr></thead><tbody><tr><td>

Comma-Separated Values

</td><td>

`.csv`

</td></tr><tr><td>

Extensible Markup Language

</td><td>

`.xml`

</td></tr><tr><td>

Hypertext Markup Language

</td><td>

-   `.htm`
-   `.html`

</td></tr><tr><td>

Microsoft Excel

</td><td>

-   `.xls`
-   `.xlsm`
-   `.xlsx`
-   `.xltx`

</td></tr><tr><td>

Microsoft PowerPoint

</td><td>

-   `.potx`
-   `.pps`
-   `.ppsx`
-   `.ppt`
-   `.pptm`
-   `.pptx`

</td></tr><tr><td>

Microsoft Word

</td><td>

-   `.doc`
-   `.docm`
-   `.docx`
-   `.dotx`

</td></tr><tr><td>

Plain Text

</td><td>

`.txt`

</td></tr><tr><td>

Portable Document Format

</td><td>

`.pdf`

</td></tr><tr><td>

Rich Text Format

</td><td>

`.rtf`

</td></tr></tbody>
</table>**Note:** Some external content connectors include support for indexing searchable content and metadata from additional content formats, such as video transcriptions or source-specific native document formats. Examples of source-specific native document formats include `.aspx` pages in Microsoft SharePoint Online and Wiki pages in Atlassian Confluence Cloud.

For details on defining file-extension inclusion and exclusion filters for external content connectors, see [Configuring crawl settings for external content connectors](../concept/cfg-crawl-settings-ext-cont-connector.md).

Binary files may be retrieved as content items, or as attachments found on content items. The exact behavior depends on the connector type.

**Important:** The maximum file size for binary files is 25 MB. Keyword indexing processes up to the first 1MB of text. Use semantic search to index data containing between 1MB and 25 MB of text.

**Parent Topic:**[External Content Connectors reference](../concept/reference-ext-cont-connectors.md)

