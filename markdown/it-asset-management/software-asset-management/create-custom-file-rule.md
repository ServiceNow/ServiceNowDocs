---
title: Create a custom file rule to manually define file sets
description: Create custom rules to manually define file sets and normalize data not recognized by the SAM API. After you have created custom rules, custom file sets can be discovered with File Signature Normalization and software records can be generated.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Software Asset Management administration, Software Asset Management, IT Asset Management]
---

# Create a custom file rule to manually define file sets

Create custom rules to manually define file sets and normalize data not recognized by the SAM API. After you have created custom rules, custom file sets can be discovered with File Signature Normalization and software records can be generated.

## Before you begin

Role required: sam\_admin

## About this task

File Signature Normalization identifies software installation packages based on file attributes in a configuration item. The input is then sent to the SAM API. If there are files properties discovered that are not associated with the File Signature Normalization rule, you can manually normalize the data and send the input to the API to create a software installation record.

**Note:** File signature rules discovered in the content service library take precedence over custom file signature rules.

## Procedure

1.  Navigate to **All** &gt; **Software Asset** &gt; **Administration** &gt; **Custom File Normalization Rules** and create a new record \(see table for field descriptions\).

<table id="table_gy3_bhf_43b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Publisher

</td><td>

Publisher of the software. You can use the lookup list provided.**Note:** Publisher is a reference to the company \[core\_company\] table. Only companies you are using internally are shown.

</td></tr><tr><td>

Product

</td><td>

Software product name. The same lookup list provided on the Software Discovery Models form. You can create a custom product from the lookup list, if desired. **Note:** If the relationship between the software publisher \[samp\_sw\_publisher\] table and the company \[core\_company\] table is not correct, products for that publisher may not be shown.

</td></tr><tr><td>

Version

</td><td>

Version of the software product.Required if version condition value is **\[starts with\]** or **\[is-\]**.

</td></tr><tr><td>

Edition

</td><td>

Edition of the software product to use when searching for the normalized discovery model.Required if edition condition value is **\[starts with\]** or **\[is\]**.

</td></tr><tr><td>

Platform

</td><td>

Platform of the software product to use when searching for the normalized discovery model.The default is **Anything** for Windows, macOS, UNIX.

</td></tr><tr><td>

Language

</td><td>

Language of the software product to use when searching for the normalized discovery model, which is populated once it has been normalized or added manually.The default is **Anything**.

</td></tr><tr><td>

Exclude from content service

</td><td>

Option to exclude file set rule from being included in content service library.

</td></tr><tr><td>

File name

</td><td>

Name of file associated with software installation as it exists in the system.

</td></tr><tr><td>

File size

</td><td>

Size of file name file in bytes.

</td></tr><tr><td>

File version

</td><td>

Version of file name file.

</td></tr></tbody>
</table>2.  Click **Submit**.


## Result

The custom rule is added to the Unidentified File Sets list.

**Parent Topic:**[Software Asset Management administration](../concept/c_SAMAdministration.md)

