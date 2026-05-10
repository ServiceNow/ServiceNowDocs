---
title: Import security tag rules
description: You can import security tag rules from other tables in your deployment.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-05-09"
reading_time_minutes: 1
breadcrumb: [Set up security tag groups and tags, Security Operations common functionality, Security Operations]
---

# Import security tag rules

You can import security tag rules from other tables in your deployment.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Security Operations** &gt; **Security Tags** &gt; **Tags**.

2.  Choose or [create a security tag](create-class-group-and-tags.md).

3.  Select the **Import security tag rules** related link.

    ![Import security tag rules](../image/ImportSecTagRules.png)

4.  Fill in the fields on the form, as appropriate.

<table id="table_t4d_4bd_5s"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Target table

</td><td>

Choose the table to use to import rules.

</td></tr><tr><td>

Target field

</td><td>

Choose the field to use to import rules.

</td></tr><tr><td>

Type of Match

</td><td>

Choose how to match the imported rules to **Security Tags** from: -   Exact match \(default\)
-   Contains
-   Starts with
-   Ends with
-   Regular Expression


</td></tr><tr><td>

Import type

</td><td>

Choose: -   **From clipboard**

Copy a list of delimited values into the text area. The values are parsed into security tags.

-   **From file upload**

Upload a file with delimited values. The values are parsed into security tags.

 Add values for the security tag rules using new line, or pipe delimiters.

</td></tr></tbody>
</table>5.  Select **Submit**


**Parent Topic:**[Set up security tag groups and tags](create-class-group-and-tags.md)

