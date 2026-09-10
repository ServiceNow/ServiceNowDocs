---
title: Update the Word template with a collaboration block
description: Use the Block feature in Document designer to add a repeating collaboration section, including a nested action items table, to a customized event Microsoft Word template.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/add-collaboration-block-docudesigner.html
release: zurich
topic_type: task
last_updated: "2026-08-04"
reading_time_minutes: 1
breadcrumb: [Generating reports using Document designer, Configure, Business Continuity Management, Governance, Risk, and Compliance]
---

# Update the Word template with a collaboration block

Use the Block feature in Document designer to add a repeating collaboration section, including a nested action items table, to a customized event Microsoft Word template.

## Before you begin

Role required: sn\_bcm.admin, sn\_bcm.manager

## About this task

The base version template already includes a **Collaboration threads** section in tabular form. This task customizes that section into a block with a nested action items table. Complete the steps in [Save Microsoft Word document as a template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/create-bcm-word-temp-using-docudesigner.md) up to inserting a block before you begin this task.

## Procedure

1.  In the Microsoft Word document open for template design, place the cursor where the collaboration section is displayed and select **Block** on the ribbon.

2.  In the **Content block source** field, select **Collaboration**.

3.  Select **Add content block**.

4.  To display the collaboration fields, select **Data**, choose **Name**, **Description**, **Impacted assets**, **Recovery team**, and **State**, then select **Add**.

5.  To include the action items related to the collaboration as a table inside the block, select **Table**, choose the **Action items** table element, then select **Add**.

6.  Save the template and upload it to your instance.

    The collaboration block, with its nested action items table, is available in Microsoft Word reports generated from this template. For more information on generating the report, see [Generate reports for BIAs, BCPs, and events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/generate-word-doc-of-bia-bcp-event.md).


