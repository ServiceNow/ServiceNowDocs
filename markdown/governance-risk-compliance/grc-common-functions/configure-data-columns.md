---
title: Configure data columns
description: Configure data columns to include table fields or scripted content in your report. Format scripted content as text or HTML.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/grc-common-functions/configure-data-columns.html
release: zurich
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-09-03"
reading_time_minutes: 1
breadcrumb: [Create content configurations, Configure document templates using Document Designer, Microsoft Word based audit report templates using Document designer, Common GRC features, Governance, Risk, and Compliance]
---

# Configure data columns

Configure data columns to include table fields or scripted content in your report. Format scripted content as text or HTML.

## Before you begin

Role required: sn\_grc\_doc\_design.admin or sn\_audit.admin

## Procedure

1.  Navigate to the **Data columns** related list.

2.  Select **New**.

3.  Review the **Content configuration** field.

    This read-only field contains the name of the associated content configuration. To preview the record, select the information icon.

4.  In the **Type** field, select **Column** or **Script**.

5.  If you selected **Column**, in the **Column** field, select the field that you want to include.

    A tree view displays the fields available from the selected table. Expand the folders as needed and select the required field.

6.  If you selected **Script**, configure the scripted column.

    1.  In the **Content type** field, select the format of the content.

        |Selection|Result|
        |---------|------|
        |Text|Returns the scripted content as text. This value is selected by default. Existing scripted data columns continue to return text. For example: `return targetRecordGr.getDisplayValue();`|
        |HTML|Returns the scripted content as HTML. For example: `return `<h1>${targetRecordGr.getDisplayValue()}</h1>`;`|

        **Important:**

        HTML scripted data columns are supported only when the content configuration is used in a content block. They aren't available when the content configuration is used in a table.

    2.  In the **Column name** field, enter a name for the scripted data column.

    3.  In the **Script** field, enter a script that returns the content.

7.  Select **Submit**.


## What to do next

To continue configuring your report, see [Configure intermediate filters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/grc-common-functions/configure-intermediate-filters.md).

