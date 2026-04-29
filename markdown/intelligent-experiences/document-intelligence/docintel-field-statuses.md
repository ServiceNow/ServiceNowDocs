---
title: Document field statuses
description: The following is a list of the statuses for fields in DocIntel document tasks. These statuses apply to fields for both document classification and data extraction.
locale: en-US
release: australia
product: Document Intelligence
classification: document-intelligence
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reference, Document Intelligence, Enable AI experiences]
---

# Document field statuses

The following is a list of the statuses for fields in DocIntel document tasks. These statuses apply to fields for both document classification and data extraction.

**Important:** Starting with the Zurich release, Document Intelligence is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details, see the Deprecation Process article \[[KB0867184](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184)\] in the Now Support Knowledge Base. Instead, you can extract information from documents using the Now Assist in Document Intelligence application. For more information, see [Now Assist in Document Intelligence](../concept/docintel-nowassist-landing.md).

<table id="table_tgt_czn_ncc"><thead><tr><th>

Status

</th><th>

Icon

</th><th>

Description

</th></tr></thead><tbody><tr><td>

To complete

</td><td>

![To complete icon.](../image/icon-docintel-tocomplete.png)

</td><td>

The field must be filled in with a value or marked as missing in the document.

</td></tr><tr><td>

Completed

</td><td>

![Completed icon.](../image/icon-docintel-completed.png)

</td><td>

The field is filled in with a value or marked as missing in the document.

</td></tr><tr><td>

To review

</td><td>

![To review icon.](../image/icon-docintel-tocomplete.png)

</td><td>

The field is auto-filled and needs review by a user.

</td></tr><tr><td>

Reviewed

</td><td>

![Reviewed icon.](../image/icon-docintel-completed.png)

</td><td>

The auto-filled field has been reviewed by a user.

</td></tr><tr><td>

In progress

</td><td>

![In progress icon.](../image/icon-docintel-inprogress.png)

</td><td>

The field is in the process of being filled in or reviewed.

</td></tr><tr><td>

Needs attention

</td><td>

![Needs attention icon.](../image/icon-docintel-warning.png)

</td><td>

The auto-filled field has triggered a warning. The causes for a warning include:

-   A required field must be filled in or marked as missing in the document.
-   An extracted value has a low confidence score and should be reviewed.
-   An extracted value is ambiguous and should be verified.

</td></tr></tbody>
</table>**Parent Topic:**[Document Intelligence references](docintel-references.md)

**Related topics**  


[Components installed with Document Intelligence](installed-with-document-intelligence.md)

[Confidence scores](../concept/docintel-confidence-scores.md)

[Data extraction modes](data-extraction-modes.md)

[Data normalization](../concept/data-normalization.md)

[Document Intelligence forms](document-intelligence-forms.md)

[Document Intelligence properties](document-intelligence-properties.md)

[Document Intelligence roles](document-intelligence-user-roles.md#)

[Document Intelligence terminology](../concept/docintel-terminology.md#)

[Document task statuses](docintel-task-statuses.md)

[Domain separation and Document Intelligence](domain-separation-and-doc-intel.md)

[Languages supported by Document Intelligence](../concept/languages-supported-by-document-intelligence.md)

[Limitations in Document Intelligence](hard-limits-in-doc-intel.md)

