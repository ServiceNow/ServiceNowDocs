---
title: Code generation properties
description: You can adjust how code generation functions on an instance using several advanced properties.
locale: en-US
release: xanadu
product: Scripts
classification: scripts
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Code generation reference, Now Assist for code generation, Scripting, Building pro-code applications, Developing your application, Building applications]
---

# Code generation properties

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
-   Learn more: You can also enable code generation from Now Assist Admin. For more information, see [Activate a Now Assist skill](https://www.servicenow.com/docs/access?context=configure-a-now-assist-skill&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

</td></tr><tr><td>

sn\_now\_assist\_code.enable\_prompt\_modal

</td><td>

Enables using the Code with Now Assist dialog box to provide text prompts.

 -   Type: true \| false
-   Default value: true
-   Location: System Property \[sys\_properties\] table
-   Learn more: [Generate scripts from text](../concept/generate-code.md#)

</td></tr><tr><td>

sn\_now\_assist\_code.enable\_code\_edit

</td><td>

Enables editing code with Now Assist.

 -   Type: true \| false
-   Default value: true
-   Location: System Property \[sys\_properties\] table
-   Learn more: [Edit code with Now Assist](../concept/edit-code-now-assist.md)

</td></tr><tr><td>

sn\_now\_assist\_code.show\_ai\_code\_line\_marker

</td><td>

Enables tracking which lines of code are AI-generated. This code is indicated by a line next to the lines of code in a script editor. If you edit AI-generated code, the line indicator doesn’t appear for those lines of code.

 -   Type: true \| false
-   Default value: true
-   Location: System Property \[sys\_properties\] table
-   Learn more: [Tracking AI-generated code](../concept/tracking-ai-generated-code.md#)

</td></tr><tr><td>

sn\_now\_assist\_code.collect\_schema\_for\_code\_assist

</td><td>

Specifies whether to collect the data schema of the table a business rule or client script runs on when using code generation. If you set this property to false, you can receive code suggestions quicker but may get less contextual suggestions.

 -   Type: true \| false
-   Default value: true
-   Location: System Property \[sys\_properties\] table

</td></tr></tbody>
</table>**Parent Topic:**[Code generation reference](../concept/now-assist-code-reference.md)

