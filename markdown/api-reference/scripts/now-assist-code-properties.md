---
title: Now Assist for Code properties
description: You can adjust how code generation functions on an instance using several advanced properties.
locale: en-US
release: zurich
product: Scripts
classification: scripts
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Now Assist for Code reference, Now Assist for Code, Scripting, API implementation, API implementation and reference]
---

# Now Assist for Code properties

You can adjust how code generation functions on an instance using several advanced properties.

**Note:** To open the System Properties \[sys\_properties\] table, enter `sys_properties.list` in the navigation filter.

<table id="table_dsp_1h2_tyb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_now\_assist\_code.enable\_code\_assist

</td><td>

Enables using code generation in supported script editors.

 -   Type: true \| false
-   Default value: true
-   Location: System Property \[sys\_properties\] table
-   Learn more: You can also enable code generation from Now Assist Admin. For more information, see [Activate a Now Assist skill](https://www.servicenow.com/docs/access?context=configure-a-now-assist-skill&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

</td></tr><tr><td>

sn\_now\_assist\_code.enable\_promptless\_experience

</td><td>

Enables using code completion in the script editor.

 -   Type: true \| false
-   Default value: false
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_now\_assist\_code.enable\_prompt\_modal

</td><td>

Enables using the Code with Now Assist dialog box to provide text prompts.

 -   Type: true \| false
-   Default value: true
-   Location: System Property \[sys\_properties\] table
-   Learn more: [Generate code with AI-powered code generation](../task/generate-scripts-from-text.md)

</td></tr><tr><td>

sn\_now\_assist\_code.show\_ai\_code\_line\_marker

</td><td>

Enables tracking which lines of code are AI-generated. In a script editor, the AI-generated codes are indicated by a line next to the line numbers. However, if you edit any AI-generated code, the indicator doesn’t appear for the modified lines.

 -   Type: true \| false
-   Default value: true
-   Location: System Property \[sys\_properties\] table
-   Learn more: [Tracking AI-generated code](../concept/tracking-ai-generated-code.md#)

</td></tr><tr><td>

sn\_now\_assist\_code.collect\_schema\_for\_code\_assist

</td><td>

Specifies whether to collect the data schema of the table, a business rule, or client script runs when using code generation. If you set this property to false, you can receive code suggestions faster but may get fewer contextual suggestions.

 -   Type: true \| false
-   Default value: true
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_now\_assist\_code.log\_edited\_response

</td><td>

Enables logging of the full script content after you accept a suggestion from Now Assist in script editors.

 When enabled, the system captures the entire script body immediately after you accept an AI-generated suggestion and saves it in the sys\_generative\_ai\_log.edited\_response field.

 This property is useful for auditing, troubleshooting, or reviewing how suggestions were added to the final script.

 -   Type: true \| false
-   Default value: true
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_now\_assist\_code.async\_max\_payload\_size

</td><td>

Specifies the maximum payload size for autocomplete messages sent over the Asynchronous Message Bus \(AMB\). The current platform limit for AMB payloads is 8 KB, and it shouldn’t be exceeded.

 Adjusting this setting helps optimize performance and help prevent errors caused by oversized payloads.

 -   Type: integer
-   Default value: 7056
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_now\_assist\_code.enable\_auto\_complete

</td><td>

Enables AI-driven code generation and autocomplete within Now Assist. Activate this property to enable Now Assist to provide intelligent, context-aware code suggestions as you write scripts.

 -   Type: true \| false
-   Default value: true
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_now\_assist\_code.disable\_snowsk8s\_autocomplete

</td><td>

Stops Now Assist from using SnowSkates for autocomplete. Set this property to true if you prefer a different code-suggestion provider or want to restrict SnowSkates-based processing.

 -   Type: true \| false
-   Default value: false
-   Location: System Property \[sys\_properties\] table

</td></tr></tbody>
</table>**Note:**

Users with access to the system property table can modify system properties. However, updating the following system properties requires the now\_assist\_code\_admin role:

-   sn\_now\_assist\_code.log\_edited\_response
-   sn\_now\_assist\_code.async\_max\_payload\_size
-   sn\_now\_assist\_code.enable\_auto\_complete
-   sn\_now\_assist\_code.disable\_snowsk8s\_autocomplete

**Parent Topic:**[Now Assist for Code reference](../concept/now-assist-code-reference.md)

