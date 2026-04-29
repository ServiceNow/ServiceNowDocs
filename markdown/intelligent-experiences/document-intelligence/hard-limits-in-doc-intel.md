---
title: Limitations in Document Intelligence
description: There are several important limitations to be aware of when you’re using Document Intelligence.
locale: en-US
release: australia
product: Document Intelligence
classification: document-intelligence
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Reference, Document Intelligence, Enable AI experiences]
---

# Limitations in Document Intelligence

There are several important limitations to be aware of when you’re using Document Intelligence.

**Important:** Starting with the Zurich release, Document Intelligence is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details, see the Deprecation Process article \[[KB0867184](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184)\] in the Now Support Knowledge Base. Instead, you can extract information from documents using the Now Assist in Document Intelligence application. For more information, see [Now Assist in Document Intelligence](../concept/docintel-nowassist-landing.md).

For a list of the important limitations in Now Assist in Document Intelligence that differ from the limitations in Document Intelligence, see [Limitations in Now Assist in Document Intelligence](now-assist-document-intelligence-limitations.md).

The following table is a list of the important limitations in Document Intelligence.

<table id="table_rfk_lpm_htb"><thead><tr><th>

Limit

</th><th>

Description

</th></tr></thead><tbody><tr><td>

File formats

</td><td>

The supported file formats are JPEG, PNG, and PDF.

</td></tr><tr><td>

File size limits

</td><td>

The file size limit is 10 MB.

</td></tr><tr><td>

Page count limit per document task

</td><td>

Document Intelligence supports a 10-page count limit for JPEG and PNG.For PDFs, the page count limit is 25.

</td></tr><tr><td>

Supported languages

</td><td>

For information on supported languages, see [Languages supported by Document Intelligence](../concept/languages-supported-by-document-intelligence.md).

</td></tr><tr><td>

Document rotation

</td><td>

Document Intelligence supports rotating in 90-degree increments.

</td></tr><tr><td>

Text alignment

</td><td>

The text must be aligned horizontally within the document.

</td></tr><tr><td>

Minimum character size

</td><td>

The minimum character size is 15 pixels.

</td></tr><tr><td>

Character type

</td><td>

Document Intelligence supports only printed character types in a document.

</td></tr><tr><td>

Character set

</td><td>

Document Intelligence detects the following characters:-   a-z, A-Z, 0–9
-   á à â ä ã å ß ç é è ê ë î ï í ñ ó ò ô ö õ ú ù ü û œ
-   Á À Â Ä Ã Å ẞ Ç É È Ê Ë Î Ï Í Ñ Ó Ò Ô Ö Õ Ú Ù Ü Û Œ
-   , : ; . ‘ \\ ” ! ? ¿ ¡ + - \* \( \) \[ \] \} \{ &amp; % @ \# / \| ~ ^ &lt; &gt; \` ± = \_ $ £ ¢ €

</td></tr><tr><td>

Sync/async operations

</td><td>

Async

</td></tr><tr><td>

Maximum number of document tasks processed per instance per day

</td><td>

The maximum number of document tasks processed per instance per day is 2000.

</td></tr><tr><td>

Maximum number of fields per use case

</td><td>

The maximum number of fields per document extraction use case is 50.

 The maximum number of fields \(categories\) per document classification use case is 30.

</td></tr></tbody>
</table>**Parent Topic:**[Document Intelligence references](docintel-references.md)

**Related topics**  


[Components installed with Document Intelligence](installed-with-document-intelligence.md)

[Confidence scores](../concept/docintel-confidence-scores.md)

[Data extraction modes](data-extraction-modes.md)

[Data normalization](../concept/data-normalization.md)

[Document field statuses](docintel-field-statuses.md)

[Document Intelligence forms](document-intelligence-forms.md)

[Document Intelligence properties](document-intelligence-properties.md)

[Document Intelligence roles](document-intelligence-user-roles.md#)

[Document Intelligence terminology](../concept/docintel-terminology.md#)

[Document task statuses](docintel-task-statuses.md)

[Domain separation and Document Intelligence](domain-separation-and-doc-intel.md)

[Languages supported by Document Intelligence](../concept/languages-supported-by-document-intelligence.md)

