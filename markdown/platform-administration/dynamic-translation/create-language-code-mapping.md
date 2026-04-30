---
title: Create a language code mapping
description: Create a language code mapping to map the ServiceNow language codes with the language codes of the translation service providers.
locale: en-US
release: xanadu
product: Dynamic Translation
classification: dynamic-translation
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Language Code Mapping in Dynamic Translation, Translating with Dynamic Translation, Dynamic Translation, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a language code mapping

Create a language code mapping to map the ServiceNow® language codes with the language codes of the translation service providers.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Dynamic Translation** &gt; **Language Code Mappings**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_zpb_dt5_mpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Language code

</td><td>

Language for which a ServiceNow® language code mapping record is being created.

</td></tr><tr><td>

Mapped language code

</td><td>

Translation service provider's language code with which the ServiceNow® language code is being mapped.

</td></tr><tr><td>

Name

</td><td>

Identifier for the language and the mapping code.The name is auto-filled using the language code and the mapped language code in the "language code -&gt; mapped language code" format.

 For example, fq -&gt; fr-CA.

 Users can edit the fields if required.

</td></tr></tbody>
</table>4.  Click **Submit**.

    **Note:** After creating the language code mapping, associate it with a corresponding translator configuration to map the existing ServiceNow® language code.


