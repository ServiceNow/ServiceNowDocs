---
title: Document Intelligence properties
description: Document Intelligence \(DocIntel\) system properties control the behavior of the Document Intelligence application.
locale: en-US
release: xanadu
product: Document Intelligence
classification: document-intelligence
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Document Intelligence references, Document Intelligence, Enable AI experiences]
---

# Document Intelligence properties

Document Intelligence \(DocIntel\) system properties control the behavior of the Document Intelligence application.

The DocIntel Manager \(sn\_docintel.manager\) can modify the system properties for DocIntel.

**Note:**

Document Intelligence 3.0 includes new and updated system properties. For more detail about the upgrade, see [Upgrade to Document Intelligence 3.0 or later from version 2.4 or earlier](upgrade-to-document-intelligence-3-0.md).

## Document Intelligence 2.4- system properties

<table id="table_vn2_2v2_g5b"><thead><tr><th>

Property name

</th><th>

Description

</th><th>

Values

</th></tr></thead><tbody><tr><td>

sn\_docintel.default\_field\_sidebar\_width

</td><td>

The default sidebar width for the document fields panel in the Document Intelligence workspace.

</td><td>

Allowed: Format of `[integer]px`

 Default: 416px

</td></tr><tr><td>

sn\_docintel.default\_image\_fit

</td><td>

The default image fit for the document panel viewer in the Document Intelligence workspace.

</td><td>

Allowed: fit\_to\_page, fit\_to\_width

 Default: fit\_to\_page

</td></tr><tr><td>

sn\_docintel.default\_thumbnail\_sidebar\_width

</td><td>

The default thumbnail sidebar width for the navigation panel in the Document Intelligence workspace.

</td><td>

Allowed: Format of `[integer]px`

 Default: 167px

</td></tr><tr><td>

sn\_docintel.field\_sidebar\_layout\_position

</td><td>

The layout position for the document fields panel in the Document Intelligence workspace, in relation to the document fields panel sidebar.

</td><td>

Allowed: right, left

 Default: right

</td></tr><tr><td>

sn\_docintel.show\_exact\_match\_option

</td><td>

Show the exact match option for each field in the document fields panel in the Document Intelligence workspace.

</td><td>

Allowed: true, false

 Default: true

</td></tr><tr><td>

sn\_docintel.show\_candidate\_score

</td><td>

Show confidence scores on the recommendations selection menu in the document fields panel in the Document Intelligence workspace.

</td><td>

Allowed: true, false

 Default: true

</td></tr><tr><td>

sn\_docintel.warning\_score\_threshold

</td><td>

Threshold used to show the warning icon for low-score recommendations in the document fields panel in the Document Intelligence workspace.

</td><td>

Allowed: Number between 0.0 and 1.0

 Default: 0.7

</td></tr><tr><td>

sn\_docintel.autofill\_threshold

</td><td>

Minimum score threshold required to auto-fill recommendations.

</td><td>

Allowed: Number between 0.0 and 1.0

 Default: 0.0

</td></tr><tr><td>

sn\_docintel.straight\_through\_processing\_threshold

</td><td>

Minimum score threshold required for straight-through processing of a document task.

</td><td>

Allowed: Number between 0.0 and 1.0

 Default: 1.0

</td></tr></tbody>
</table>## Document Intelligence 3.0+ system properties

<table id="table_hfc_qqh_2yb"><thead><tr><th>

Property name

</th><th>

Description

</th><th>

Values

</th></tr></thead><tbody><tr><td>

glide.platform\_ml\_di.doc\_classifier. days\_between\_trainings

</td><td>

Document classifier property

 Minimum number of days between trainings for a given document classifier use case.

</td><td>

Default: 30

</td></tr><tr><td>

glide.platform\_ml\_di.doc\_data\_extractor. warning\_score\_threshold

</td><td>

Document extraction property

 Threshold used to show the warning icon for low-score recommendations in the document fields panel in the Document Intelligence workspace.

</td><td>

Allowed: Number between 0.0 and 1.0

 Default: 0.7

</td></tr><tr><td>

glide.platform\_ml\_di.doc\_data\_extractor. straight\_through\_processing\_threshold

</td><td>

Document extraction property

 Minimum score threshold required for straight-through processing of a document task.

</td><td>

Allowed: Number between 0.0 and 1.0

 Default: 1.0

</td></tr><tr><td>

glide.platform\_ml\_di.doc\_data\_extractor. show\_exact\_match\_option

</td><td>

Document extraction property

 Show the exact match option for each field in the document fields panel in the Document Intelligence workspace.

</td><td>

Allowed: true, false

 Default: true

</td></tr><tr><td>

glide.platform\_ml\_di.doc\_data\_extractor. show\_candidate\_score

</td><td>

Document extraction property

 Show confidence scores on the recommendations selection menu in the document fields panel in the Document Intelligence workspace.

</td><td>

Allowed: true, false

 Default: true

</td></tr><tr><td>

glide.platform\_ml\_di.doc\_data\_extractor. field\_sidebar\_layout\_position

</td><td>

Document extraction property

 The layout position for the document fields panel in the Document Intelligence workspace, in relation to the document fields panel sidebar.

</td><td>

Allowed: right, left

 Default: right

</td></tr><tr><td>

glide.platform\_ml\_di.doc\_data\_extractor. default\_thumbnail\_sidebar\_width

</td><td>

Document extraction property

 The default thumbnail sidebar width for the navigation panel in the Document Intelligence workspace.

</td><td>

Allowed: Format of \[integer\]px

 Default: 167px

</td></tr><tr><td>

glide.platform\_ml\_di.doc\_data\_extractor. default\_image\_fit

</td><td>

Document extraction property

 The default image fit for the document panel viewer in the Document Intelligence workspace.

</td><td>

Allowed: fit\_to\_page, fit\_to\_width

 Default: fit\_to\_page

</td></tr><tr><td>

glide.platform\_ml\_di.doc\_data\_extractor. default\_field\_sidebar\_width

</td><td>

Document extraction property

 The default sidebar width for the document fields panel in the Document Intelligence workspace.

</td><td>

Allowed: Format of \[integer\]px

 Default: 416px

</td></tr><tr><td>

glide.platform\_ml\_di.doc\_data\_extractor. autofill\_threshold

</td><td>

Document extraction property

 Minimum score threshold required to auto-fill recommendations.

</td><td>

Allowed: Number between 0.0 and 1.0

 Default: 0.01

</td></tr><tr><td>

glide.platform\_ml\_di.doc\_data\_extractor. draw\_tool\_enable

</td><td>

This property is used to enable or disable draw tool features for table extraction.

</td><td>

Allowed: true, false

 Default: true

</td></tr></tbody>
</table>**Parent Topic:**[Document Intelligence references](docintel-references.md)

**Related topics**  


[Components installed with Document Intelligence](installed-with-document-intelligence.md)

[Confidence scores](../concept/docintel-confidence-scores.md)

[Data extraction modes](data-extraction-modes.md)

[Data normalization](../concept/data-normalization.md)

[Document field statuses](docintel-field-statuses.md)

[Document Intelligence forms](document-intelligence-forms.md)

[Document Intelligence roles](document-intelligence-user-roles.md#)

[Document Intelligence terminology](../concept/docintel-terminology.md#)

[Document task statuses](docintel-task-statuses.md)

[Domain separation and Document Intelligence](domain-separation-and-doc-intel.md)

[Languages supported by Document Intelligence](../concept/languages-supported-by-document-intelligence.md)

[Limitations in Document Intelligence](hard-limits-in-doc-intel.md)

