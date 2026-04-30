---
title: Create a copy of a Knowledge Graph schema
description: Create a copy of a Knowledge Graph schema and duplicate it for further customization.
locale: en-US
release: xanadu
product: Knowledge Graph
classification: knowledge-graph
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using Knowledge Graph Designer, Knowledge Graph, Now Assist, Enable AI experiences]
---

# Create a copy of a Knowledge Graph schema

Create a copy of a Knowledge Graph schema and duplicate it for further customization.

## Before you begin

Verify that you have not selected a ServiceNow prebuilt Knowledge Graph schema that is non-editable.

Verify that the scope selected when creating a Knowledge Graph schema is the same as the scope of the existing Knowledge Graph schema.

Role required: kg\_admin

## Procedure

1.  Navigate to **All** &gt; **Knowledge Graph** &gt; **Knowledge Graph Designer**.

    The UI displays a list of all the Knowledge Graph schemas on the landing page.

2.  Select a Knowledge Graph schema.

3.  Select the more icon \(![More icon.](../../now-assist-admin/image/naa-more-options-icon.png)\).

4.  Select **Copy Graph**.

    Verify that the scope of the existing Knowledge Graph schema is the same as the new schema.

5.  On the form, fill in the fields.

    |Field|Value|
    |-----|-----|
    |Display Name|Existing name of the Knowledge Graph schema.|
    |Name|Name of the cloned Knowledge Graph schema.|
    |Scope|Scope under which you want to create the Knowledge Graph schema.|
    |Description|Knowledge Graph schema overview for users.|
    |Mark as default|Check box to select the cloned Knowledge Graph schema as a fallback schema. The default schema is used if the system fails to reach the assigned schema.|

    ![Copy Knowledge Graph schema.](../Images/create-copy-of-kg-schema.png)

6.  Assign the new schema as a fallback schema by selecting the **Mark as Default** option.

    **Note:**

    -   If the specified Knowledge Graph schema isn't available, the system uses the fallback schema.
    -   If you select this option, the system overrides the existing selection.
7.  Select **Create**.


