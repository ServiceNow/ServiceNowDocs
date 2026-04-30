---
title: Define a regular expression for a variable
description: Define a regular expression \(regex\) to validate a variable value.
locale: en-US
release: xanadu
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Types of catalog items, Exploring Service Catalog, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Define a regular expression for a variable

Define a regular expression \(regex\) to validate a variable value.

## Before you begin

Role required: catalog\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Variables** &gt; **Variable Validation Regex**.

2.  Click **New**.

3.  On the form, fill the fields.

<table id="table_b1s_q5g_xfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the regular expression.

</td></tr><tr><td>

Validation message

</td><td>

Message that appears when the validation fails.

</td></tr><tr><td>

Active

</td><td>

Specifies if the regex is active.

</td></tr><tr><td>

Regular Expression

</td><td>

Sequence of characters that define the format of the variable value.For example:

-   Invalid Regex: /\(\(\(ftp\|http\|https\):\\/\\/\)\|\(www\\.\)\)\(\[-\\w\\.\\/\#$\\?=+@&amp;%\_:;\]+\)/i
-   Valid Regex: \(\(\(ftp\|http\|https\):\\/\\/\)\|\(www\\.\)\)\(\[-\\w\\.\\/\#$\\?=+@&amp;%\_:;\]+\)
 **Note:**

-   Ensure that the regex does not cause catastrophic backtracking.
-   You should not use embedded flag expressions.
-   Use the **Regex Flag** list for the ignore case.


</td></tr><tr><td>

Regex Flag

</td><td>

Character set that is considered while validating the regular expression.-   None: No regex flags are applied.
-   Case Insensitive: Enables case insensitive matching. Case insensitive matching assumes that only characters in the US-ASCII charset are being matched. Unicode-aware case-insensitive matching can be enabled by selecting **Both** as the regex flag.
-   Unicode Case: \(Reserved for future use\) Same behavior as **None**.
-   Both: Case insensitive matching is done in a manner consistent with the Unicode Standard.


</td></tr></tbody>
</table>4.  Click **Submit**.


**Parent Topic:**[Types of catalog items](../reference/r_ExtendedCatalogItemFunctions.md)

**Related topics**  


[Create a service catalog variable](t_CreateAVariableForACatalogItem.md)

