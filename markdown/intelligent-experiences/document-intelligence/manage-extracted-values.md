---
title: Manage field values
description: View the field values gathered from your processed document tasks. Review the values and add any additional information.
locale: en-US
release: australia
product: Document Intelligence
classification: document-intelligence
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Document Intelligence, Enable AI experiences]
---

# Manage field values

View the field values gathered from your processed document tasks. Review the values and add any additional information.

**Important:** Starting with the Zurich release, Document Intelligence is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details, see the Deprecation Process article \[[KB0867184](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184)\] in the Now Support Knowledge Base. Instead, you can extract information from documents using the Now Assist in Document Intelligence application. For more information, see [Now Assist in Document Intelligence](../concept/docintel-nowassist-landing.md).

## Before you begin

Role required: sn\_docintel.admin or sn\_docintel.manager

## About this task

When your document task completes, the extracted data or classifications appear in the Field Values list. The field value form includes more information about the value.

## Procedure

1.  For document data extraction fields, navigate to **All** &gt; **Document Intelligence** &gt; **Document Data Extraction** &gt; **Field Values**.

    For document classification fields or classes, navigate to **All** &gt; **Document Intelligence** &gt; **Document Classification** &gt; **Field Values**.

2.  Select the name of the value \(data\).

3.  On the form, review the fields.

<table id="table_tvt_jst_g5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Data

</td><td>

The field value extracted from the document.

</td></tr><tr><td>

Is Reviewed

</td><td>

Indicates whether this field value has been reviewed by a user.

</td></tr><tr><td>

Candidate ID \(Recommendation ID\)

</td><td>

Internal system ID for the selected recommendation.

</td></tr><tr><td>

Index

</td><td>

For fields that are part of a field group: the order of the field value in reference to other field values for the same field.

 For regular fields, the index is always 0.

</td></tr><tr><td>

Exact Match of Candidate \(Recommendation\)

</td><td>

Indicates whether the field value exactly matches the AI's top recommendation.

</td></tr><tr><td>

Field

</td><td>

Field from the use case that the value belongs to.

</td></tr><tr><td>

Candidate \(Recommendation\) Rank

</td><td>

Rank that the AI assigned to the selected recommendation.

</td></tr><tr><td>

Is Flagged

</td><td>

Whether a user has flagged this field value in the Document Intelligence workspace.

</td></tr><tr><td>

Document task

</td><td>

Document task with the attached document from which the data value was extracted.

</td></tr><tr><td>

Availability

</td><td>

Indicates whether this field value was available or missing in the document.

</td></tr><tr><td>

Keystrokes

</td><td>

Number of keystrokes that were needed to extract this field value.

</td></tr><tr><td>

Target Record

</td><td>

The record where the field value is used.

</td></tr><tr><td>

Metadata

</td><td>

The metadata associated with the field value.

</td></tr><tr><td>

Target Table

</td><td>

The table that stores the field values.

</td></tr><tr><td>

Domain

</td><td>

Domain linked to this field value.

 See [Domain separation and Document Intelligence](../reference/domain-separation-and-doc-intel.md).

</td></tr></tbody>
</table>4.  Select **Update**.


