---
title: Components installed with Document Intelligence
description: Several types of components are installed with activation of the Document Intelligence plugin, including tables and user roles.
locale: en-US
release: yokohama
product: Document Intelligence
classification: document-intelligence
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Document Intelligence references, Document Intelligence, Enable AI experiences]
---

# Components installed with Document Intelligence

Several types of components are installed with activation of the Document Intelligence plugin, including tables and user roles.

## Roles installed with Document Intelligence

For more information on roles, see [Document Intelligence roles](document-intelligence-user-roles.md#).

<table id="table_u1h_ffw_mtb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

DocIntel Admin

 \[sn\_docintel.admin\]

</td><td>

Has full access to the Document Intelligence application, except for modifying a subset of system properties, and the billing and internal tables.

</td><td>

-   platform\_ml\_di.admin
-   action\_designer
-   flow\_designer
-   sn\_ace.ace\_user
-   canvas\_user
-   usage\_admin

</td></tr><tr><td>

DocIntel Viewer

 \[sn\_docintel.viewer\]

</td><td>

Has view-only access on Document Intelligence document tasks that they are authorized to view.

</td><td>

-   snc\_read\_only
-   platform\_ml\_di.viewer

</td></tr><tr><td>

DocIntel Extraction Agent

 \[sn\_docintel.extraction\_agent\]

</td><td>

Extracts data and text from documents using the Document Intelligence workspace.

</td><td>

platform\_ml\_di.extraction\_agent

</td></tr><tr><td>

DocIntel Creation Agent

 \[sn\_docintel.creation\_agent\]

</td><td>

Extracts information from documents using the Document Intelligence workspace. Also enables users to create Document Intelligence document tasks and submit them for processing.

</td><td>

platform\_ml\_di.creation\_agent

</td></tr><tr><td>

DocIntel Manager

 \[sn\_docintel.manager\]

</td><td>

Creates and edits use cases, fields, field groups, and document tasks. Views, measures, and analyzes the usage and effectiveness of Document Intelligence using the Platform Document Intelligence Usage dashboard. Grants access to submit document tasks and interact with the Document Intelligence workspace.

</td><td>

-   platform\_ml\_di.manager
-   action\_designer
-   flow\_designer
-   sn\_ace.ace\_user
-   canvas\_user
-   usage\_admin

</td></tr></tbody>
</table>## Tables installed with Document Intelligence

**Note:** Starting in Document Intelligence 3.0, DocIntel uses ServiceNow AI Platform database tables \(sys\_di\_\) in place of the scoped application tables \(di\_\). See [Upgrade to Document Intelligence 3.0 or later from version 2.4 or earlier](upgrade-to-document-intelligence-3-0.md).

<table id="table_y1h_ffw_mtb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Billable Event

 \[sys\_di\_billable\_event\]

</td><td>

Contains all the billable events for the instance. A billable event corresponds to pages that have been processed using Document Intelligence.

</td></tr><tr><td>

Recommendation Meta Info

 \[sys\_di\_candidate\_meta\_info\]

</td><td>

\[Internal table\] Contains the data returned by the AI for field group extraction and for missing value prediction.

</td></tr><tr><td>

Recommendation Score

 \[sys\_di\_candidate\_score\]

</td><td>

\[Internal table\] Contains the scores for each recommendation calculated by the AI. There’s one record per field, for each page of a document.

</td></tr><tr><td>

Field Value

 \[sys\_di\_extracted\_value\]

</td><td>

Contains all the data extracted in the instance, across all document tasks.

</td></tr><tr><td>

Image

 \[sys\_di\_image\]

</td><td>

\[Internal table\] Contains information about each page of a document. There’s one record per document page.

</td></tr><tr><td>

Integration Setup

 \[sys\_di\_integration\_setup\]

</td><td>

Contains DocIntel use case integrations.

</td></tr><tr><td>

Field

 \[sys\_di\_key\]

</td><td>

Contains all the fields created in the instance, across all use cases. A field corresponds to a recommendation to be extracted from documents.

</td></tr><tr><td>

Field Group

 \[sys\_di\_key\_group\]

</td><td>

Contains all the field groups created in the instance, across all use cases. A field group is usually created to help extract data from tables and lists.

</td></tr><tr><td>

Lock

 \[sys\_di\_lock\]

</td><td>

Contains an index of locked task solution definitions. Used to improve the performance of scheduled jobs.

</td></tr><tr><td>

DocIntel Aggregated Metrics

 \[sys\_di\_metrics\_aggregated\]

</td><td>

\[Internal table\] Contains aggregated metrics. Aggregation may happen multiple times per day, based on system properties.

</td></tr><tr><td>

DocIntel Daily Metrics

 \[sys\_di\_metrics\_daily\]

</td><td>

\[Internal table\] Contains the metrics aggregated daily. There’s one record per aggregated metric.

</td></tr><tr><td>

DocIntel Metrics Job Log

 \[sys\_di\_metrics\_job\_log\]

</td><td>

\[Internal table\] Contains a log of the metrics daily aggregation jobs that happened in the instance.

</td></tr><tr><td>

DocIntel Raw Metrics

 \[sys\_di\_metrics\_raw\]

</td><td>

\[Internal table\] Contains a list of raw metrics collected by Document Intelligence. The records are deleted when metrics aggregation happens.

</td></tr><tr><td>

DocIntel OCR Input

 \[sys\_di\_ocr\_input\]

</td><td>

\[Internal table\] Contains image data to be sent to the OCR module for processing. The records are deleted when processing is complete.

</td></tr><tr><td>

PDF

 \[sys\_di\_pdf\]

</td><td>

\[Internal table\] Contains a list of PDF files stored across tasks.

</td></tr><tr><td>

DocIntel PDF Input

 \[sys\_di\_pdf\_input\]

</td><td>

\[Internal table\] Contains PDF data to be sent to the PDF module for processing. The records are deleted when processing is complete.

</td></tr><tr><td>

DocIntel Prediction Input

 \[sys\_di\_prediction\_input\]

</td><td>

\[Internal table\] Contains the data needed to make suggestions across all fields for a given document task. There’s one record per document page.

</td></tr><tr><td>

Document Task

 \[sys\_di\_task\]

</td><td>

Contains all the document tasks created in the instance, across all use cases. A document task contains one or more documents from which fields must be extracted.

</td></tr><tr><td>

Task Solution Definition

 \[sys\_di\_task\_def\_solution\_def\]

</td><td>

Contains the solution definitions related to DocIntel use cases.

</td></tr><tr><td>

DocIntel Use Case

 \[sys\_di\_task\_definition\]

</td><td>

Contains all the document processing use cases created in the instance. A use case defines what and how data should be extracted from a set of documents.

</td></tr><tr><td>

DocIntel Training Input

 \[sys\_di\_training\_input\]

</td><td>

\[Internal table\] Contains the data needed to improve the AI models.

</td></tr></tbody>
</table>**Parent Topic:**[Document Intelligence references](docintel-references.md)

**Related topics**  


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

[Limitations in Document Intelligence](hard-limits-in-doc-intel.md)

