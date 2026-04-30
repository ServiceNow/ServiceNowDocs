---
title: Pattern matching
description: Pattern matching in Field Normalization uses special characters differently from regular expressions to create patterns that the platform recognizes when transforming field values.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Regular expressions and patterns in field normalization rules, Field normalization and transformation, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Pattern matching

Pattern matching in Field Normalization uses special characters differently from regular expressions to create patterns that the platform recognizes when transforming field values.

Pattern matching can be used only in condition statements. When using pattern matching characters in a condition statement, make sure to select the **matches pattern** operator.

Use the following special characters to create patterns for searches.

-   The asterisk in a search string \(\*\) matches any number \(including zero\) of any character.
-   The question mark \(?\) in a search string matches one of any character.
-   Everything else in a search string matches itself.

## Examples

-   **the story** matches **the story** but not **that story**.
-   **\*story** matches **the story** and **that story**, but not **that story is the best**.
-   **st?ry** matches **story** and **stxry**, but not **my story** or **stairy**.
-   **\*b?gus\*** matches **bogus**, **my bogus story**, and **His bagus machine**, but not **my bgus story** or **my baigus story**.

**Parent Topic:**[Regular expressions and patterns in field normalization rules](c_RegExpsAndPattFldNormalizeRls.md)

