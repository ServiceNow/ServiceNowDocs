---
title: Regular expressions and patterns in field normalization rules
description: Field Transformation definitions support the use of regular expressions \(referred to in the platform as regex\) and pattern matching for determining the position of characters in a string.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Field normalization and transformation, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Regular expressions and patterns in field normalization rules

Field Transformation definitions support the use of regular expressions \(referred to in the platform as **regex**\) and pattern matching for determining the position of characters in a string.

After identifying the target characters, field transformation can replace or delete the identified characters or insert other characters at that position.

## Regex

Regular expressions can be used in transform parameters and in condition statements to determine which characters in a field value are transformed.

Regular expressions used as parameters to locate characters in transformed field values must begin with **/regex/**. Everything after that is a regular expression that is used to calculate character position.

## Example

The computer names in an organization's Windows network are expressed as domain\\machine name, such as **development\\devlab01**. The network administrator wants to simplify these names by removing the domain name and backslash. He creates a transformation record for the Computer \[cmdb\_ci\_computer\] table and selects the **Name** field to transform.

![](../image/TransformationRegex1.png "Transformation regex example")

The network contains several domains, and each domain contains numerous computers. The only character common to each name is the backslash. To delete the domain name, the administrator decides to use a regular expression to replace the entire raw value in the field with the characters that appear after the backslash \(the actual machine name\). He creates a new Transform using **Replace** as the Transform Type and enters the following values:

-   Find:**/regex/.\*\\\\\(.\*\)**
-   Replace with:**$1**

![](../image/TransformationRegex2.png "Transformation regex example")

The regular expression **.\*\\\\\(.\*\)** represents the entire raw value in the **Name** field - in this example **development\\devlab01**. The first part of the expression, **.\***, represents everything before the backslash \(the **development** domain name\). The backslash by itself is the escape character in regular expressions and requires special syntax to retain its function in the computer name. The administrator must escape it by using another backslash \(\\\\ means \\\). The part of the expression after the backslash, **\(.\*\)**, represents the computer name \(**devlab01**\) and is grouped within parentheses for reference. The value in the **Replace with** field, **$1**, references this group and replaces the entire raw value of the field with the contents of the group, **devlab01**.

The administrator clicks **Test transforms** in the transformation record and enters `development\devlab01` in the **Raw data** field. He then clicks **OK** to apply the transform to the test value. The transform replaces **development\\devlab01** with **devlab01**.

![](../image/TransformationRegex3.png "Transformation Regex 3")

When the transforms for this field are tested successfully, the administrator changes the **Mode** in the transformation record to **Active** and runs the Transformation application data job to apply this transformation to existing records in the database.

-   **[Pattern matching](c_PatternMatching.md)**  
Pattern matching in Field Normalization uses special characters differently from regular expressions to create patterns that the platform recognizes when transforming field values.

**Parent Topic:**[Field normalization and transformation](c_FieldNormalization.md)

