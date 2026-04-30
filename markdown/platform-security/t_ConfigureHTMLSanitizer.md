---
title: Configuring HTML sanitizer
description: You must modify a script include to make configuration changes to the HTML sanitizer.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [HTML sanitizer, Platform Security]
---

# Configuring HTML sanitizer

You must modify a script include to make configuration changes to the HTML sanitizer.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Script Includes**.

2.  Open **HTMLSanitizerConfig**.

3.  To add items to the exclusion list, use the HTML\_BLACKLIST class.

    To add items to the inclusion list, use the HTML\_WHITELIST class.

    Use this format:

    ```
    HTML_XXXXLIST :{
            globalAttributes :{ 
     
                attribute:[attribute-name1,...],
                attributeValuePattern:{ attribute-name2:attribute-value-regex-pattern,...}
     
            },<html-element-name>:{// Same as Above},----}
    ```

    -   **globalAttributes** contains attribute or attributeValuePattern items that are applicable globally for all the HTML elements.
    -   **attribute** is a comma-separated list of attributes.
    -   **attributeValuePattern** is a dictionary of attribute to attribute-value-regex-pattern pairs. The attribute-value-regex-pattern is a regular expression which has to match the attribute value.

## Example

Consider the following example:

```
HTML_WHITELIST:{
        globalAttributes:{
            attribute:["id","name"],},
        img:{
            attribute:["style","align"],
            attributeValuePattern:{src:".*jpeg"}}, 
        iframe:{},}
```

It adds the following items to the inclusion list:

-   The global attributes id and name. This is a list of strings that can be applied globally to all the elements.
-   The img element where the attributes are style and align.
-   The img element where the source attribute of the image is a file with the .jpeg extension. This is an example of a regular expression pattern that matches an attribute value.
-   The iframe element.

