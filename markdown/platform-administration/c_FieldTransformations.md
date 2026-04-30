---
title: Transforms
description: Transforms update field values by applying a transformation definition to the field contents such as replace text, change case, or round value.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Field normalization and transformation, Administer, Field administration, Forms, fields, and lists, Configure core features, Administer]
---

# Transforms

Transforms update field values by applying a transformation definition to the field contents such as replace text, change case, or round value.

## Transform definitions

Transform definitions define the transformation actions available for a given field type. Administrators select a definition when they transform a field, and then provide the definition with the specific parameters that are applied to the transformation. For example, a definition can round up an integer or insert a value at a defined position in a string.

The system provides a number of definitions that are designed to meet the needs of most organizations, but administrators can create new definitions as needed. Transform definitions can be associated with existing Transform Categories or to new categories.

## Transform categories

Transform categories are used to group the transform definitions together appropriately to present to users when creating new field transforms. You can create new categories for existing definitions or change the default associations of categories to definitions.

Transform categories are associated with normalization field types to present the correct definition option list for the field being transformed. The base system provides two transform categories: Text and Numeric.

-   **Text**

    Definitions in the Text category transform string type field values. Included in the Text category are:

    -   Left
    -   Right
    -   Constant
    -   Trim
    -   Prefix
    -   Suffix
    -   Change Case
    -   Delete
    -   Insert
    -   Substring
    -   Replace
-   **Numeric**

    Definitions in the Numeric category arithmetically manipulate integer type field values. Included in the Numeric category are:

    -   Limit
    -   Round
    -   Constant

## Transformation testing mode

Transformation is a powerful tool that can cause data issues if used incautiously. Test all transformations before committing the changes to the CMDB.

All transformation records open in **Test** mode by default, which blocks administrators from running manual data jobs that apply changes to existing data. Only users with the normalization\_tester role can transform data when a record is in the **Test** mode. This is limited to new records opened by the tester or records in which the transformed field is updated by the tester.

To apply transformations to the CMDB after testing, change the mode to **Active** in the transformation record and run the appropriate data job. For information on testing transforms, see [Test a transform](../task/t_TransformAField.md#).

