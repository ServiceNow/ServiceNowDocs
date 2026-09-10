---
title: Add sections and questions to a question bank
description: Add sections and questions to a question bank in the Smart Assessment Engine application so that template managers can reuse the questions in assessment templates.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/smart-assessment-engine/sae-asmnt-question-bank-populate.html
release: australia
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: task
last_updated: "2026-09-03"
reading_time_minutes: 4
breadcrumb: [Question bank, Use template designer, Manage, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Add sections and questions to a question bank

Add sections and questions to a question bank in the Smart Assessment Engine application so that template managers can reuse the questions in assessment templates.

## Before you begin

Role required: sn\_smart\_asmt.question\_bank\_manager or sn\_smart\_asmt.assessment\_admin

## About this task

**Important:** Question bank questions don't support conditional visibility or response automation. Justification conditions are supported. For more information, see [Question bank](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/question-bank.md).

## Procedure

1.  Open a question bank for updates.

    |Option|Description|
    |------|-----------|
    |**Existing question bank**|On the question bank hub, select an existing question bank.|
    |**New question bank**|When you create a question bank and select **Save**, the question bank opens on the content tree. For more information see, [Create a question bank](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/sae-asmnt-question-bank-create.md).|

    The Details page on the **General** tab displays the information that you provided to create the question bank.

2.  Select the **Questions** tab.

3.  Add a section that can hold questions by selecting **Create section**.

    A section can contain either subsections or questions, but not both. A subsection can contain only questions, not additional subsections. A new subsection is added directly after the currently selected subsection. If no subsection is selected in the section, the new subsection is added at the end of the section. To reorder sections, subsections, and questions, drag them within the content tree.

4.  Enter a name and description for the section and then select **Save**.

5.  Select a section or subsection in the list and then select **Add question**.

    Configure a question bank question the same way that you configure a template question, except that conditional visibility and response automation aren't available. For information about configuring each question type, see one of the following topics.

    |Description|Location|
    |-----------|--------|
    |Create and configure text type questions.|[Create a text question](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/sae-q-text-create.md)|
    |Create and configure drop-down list type questions.|[Create a drop-down list question](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/sae-q-drop-down-create.md)|
    |Create and configure radio button type questions.|[Create a radio button question](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/sae-q-radio-button-create.md)|
    |Create and configure check box type questions.|[Create a check box question](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/sae-q-check-box-create.md)|
    |Create and configure number type questions.|[Create a number question](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/sae-q-number-create.md)|
    |Create and configure reference type questions.|[Create a reference question](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/sae-q-reference-create.md)|
    |Create and configure attachment type questions.|[Create an attachment question](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/sae-q-attachment-create.md)|
    |Create and configure date type questions.|[Create a date question](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/sae-q-date-create.md)|
    |Create and configure code type questions.|[Create a code question](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/sae-q-code-create.md)|


## What to do next

New questions are created in the **Draft** state. For information about moving a question through its lifecycle, see [Publish questions in a question bank](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/sae-asmnt-question-bank-publish.md).

