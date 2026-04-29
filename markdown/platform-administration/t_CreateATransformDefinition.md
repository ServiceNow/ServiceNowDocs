---
title: Create a transform definition
description: The following example describes the procedure for creating a new transform definition. In this example, we create a definition that transforms a number field to an odd or even integer. The transform category is Numeric and the normalization field type is Integer.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Default transform definitions, Field normalization and transformation, Administer, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a transform definition

The following example describes the procedure for creating a new transform definition. In this example, we create a definition that transforms a number field to an odd or even integer. The transform category is **Numeric** and the normalization field type is **Integer**.

## Procedure

1.  Navigate to **All** &gt; **Field Normalization** &gt; **Administration** &gt; **Transform Definitions**.

2.  Click **New** in the record list.

3.  Enter a name for this definition.

    **Note:** In this example, we enter `Odd/Even`.

4.  Enter a brief description of the action, such as, `Transforms an integer to an odd or even value`.

    This information appears in the definition choice list when a user selects a new transform.

5.  Right-click in the header bar and select **Save** in the context menu.

    Two Related Lists appear in the form.

    -   Transform Categories: Click **Edit** and select **Numeric** as the category to which this definition belongs. Currently, field transformation supports two categories: **Numeric** and **Text**. The **Integer** normalization field type is already associated with this category.
    -   Transform Variables: Define any variables required by this transform definition to perform an action on a field value. Variables are not necessary if a script can perform the action alone.

