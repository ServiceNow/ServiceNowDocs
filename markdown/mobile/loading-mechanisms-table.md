---
title: Loading mechanisms for input form UI elements
description: Use this table to see which loading mechanisms support specific UI elements in an input form.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Loading mechanisms for input form screens, Configure an input form screen, Input form screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Loading mechanisms for input form UI elements

Use this table to see which loading mechanisms support specific UI elements in an input form.

For more information, refer to the following topics:

-   For inputs, see [Input form screen attributes for inputs](parameter-screen-var-attr.md).
-   For input actions, see [Configure input form actions in an input form screen](../task/input-actions-configure.md).
-   For descriptive elements, see [Configure descriptive elements for input form screens](../task/descriptive-elements-script.md).

<table id="table_bdv_hvb_p2c"><thead><tr><th>

UI element

</th><th>

Type

</th><th>

Autofill variable

</th><th>

Data source

</th><th>

Comment

</th></tr></thead><tbody><tr><td>

Input

</td><td>

String

</td><td>

Yes

</td><td>

Yes

</td><td>

-

</td></tr><tr><td>

Input

</td><td>

Number

</td><td>

Yes

</td><td>

Yes

</td><td>

-

</td></tr><tr><td>

Input

</td><td>

Choice

</td><td>

Yes

</td><td>

Yes

</td><td>

-   For autofill variables: Applies to choice inputs of single choice only.
-   For data sources: Applies to choice inputs of both single choice and multiple choices.

</td></tr><tr><td>

Input

</td><td>

Date/Time

</td><td>

Yes

</td><td>

Yes

</td><td>

Applies to both inputs data and date time.

</td></tr><tr><td>

Input

</td><td>

Boolean

</td><td>

Yes

</td><td>

Yes

</td><td>

-

</td></tr><tr><td>

Input

</td><td>

Reference

</td><td>

Yes

</td><td>

Yes

</td><td>

-   For autofill variables: Applies to single reference inputs only.
-   For data sources: Applies to both single reference and list of references inputs.

</td></tr><tr><td>

Input

</td><td>

Attachment

</td><td>

-

</td><td>

Yes

</td><td>

Must be mapped to the sys\_id of the record.

</td></tr><tr><td>

Input

</td><td>

Screen

</td><td>

-

</td><td>

Yes

</td><td>

-

</td></tr><tr><td>

Input

</td><td>

Bar code

</td><td>

-

</td><td>

Yes

</td><td>

-

</td></tr><tr><td>

Input

</td><td>

Ranking

</td><td>

-

</td><td>

Yes

</td><td>

-

</td></tr><tr><td>

Input

</td><td>

Custom map

</td><td>

-

</td><td>

-

</td><td>

-

</td></tr><tr><td>

Input

</td><td>

Signature

</td><td>

-

</td><td>

-

</td><td>

-

</td></tr><tr><td>

Input action

</td><td>

Comment

</td><td>

-

</td><td>

Yes

</td><td>

-

</td></tr><tr><td>

Input action

</td><td>

Attachments

</td><td>

-

</td><td>

Yes

</td><td>

Must be mapped to the sys\_id of the record.

</td></tr><tr><td>

Input action

</td><td>

Navigation function

</td><td>

-

</td><td>

Yes

</td><td>

Relates to a function with a Record context. By default, the context of the navigation function is the input form’s context. You can override it with any custom context.

</td></tr><tr><td>

Descriptive element

</td><td>

Image

</td><td>

-

</td><td>

Yes

</td><td>

Must be mapped to an image field type column.

</td></tr><tr><td>

Descriptive element

</td><td>

HTML \(Rich text\)

</td><td>

-

</td><td>

Yes

</td><td>

Must be mapped to an HTML field type column.

</td></tr><tr><td>

Descriptive element

</td><td>

Plain text

</td><td>

-

</td><td>

Yes

</td><td>

Must be mapped to a string or string \(UTF-8\) field type column.

</td></tr><tr><td>

Descriptive element

</td><td>

Card

</td><td>

-

</td><td>

Yes

</td><td>

For configuration of mobile cards, see [Mobile Card Builder](../concept/mobile-card-builder.md).

</td></tr></tbody>
</table>