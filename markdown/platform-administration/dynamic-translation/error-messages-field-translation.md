---
title: Error messages in Dynamic Translation
description: You must be aware of a few error scenarios while using Dynamic Translation.
locale: en-US
release: australia
product: Dynamic Translation
classification: dynamic-translation
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference for Dynamic Translation, Dynamic Translation, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Error messages in Dynamic Translation

You must be aware of a few error scenarios while using Dynamic Translation.

## Error messages on forms and activity streams

Error messages are displayed when the text cannot be dynamically translated on forms activity streams.

<table id="table_fbh_j24_wpb"><thead><tr><th>

Scenario

</th><th>

Error message

</th></tr></thead><tbody><tr><td>

Field has no value.**Note:** This scenario is applicable only for fields on the form.

</td><td>

No text to translate.

</td></tr><tr><td>

Text to be translated is already in the logged-in user's preferred language.

</td><td>

This content is written in your preferred language. No need to translate.

</td></tr><tr><td>

Text cannot be translated to the user's preferred language by the default translation service provider.

</td><td>

Text cannot be translated to your preferred language.

</td></tr><tr><td>

Credentials configured for the translation service provider under **Connections &amp; Credentials** are not valid.

</td><td>

Credentials are missing or invalid. Contact your administrator.

</td></tr><tr><td>

Text to be translated has exceeded the maximum length supported by the default translation service provider.​

</td><td>

Text has exceeded the maximum length.

</td></tr><tr><td>

Error during translation. Possible reasons are:-   Credentials configured for the translation service provider under the **Connections &amp; Credentials** sub module are missing.
-   Translation got timed out.
-   Any other issue with the translation service provider. For example, the exhaustion of credentials for more transactions.

</td><td>

Unable to translate.

</td></tr></tbody>
</table>## Error messages on translator configuration

|Scenario|Error message|
|--------|-------------|
|When there is no valid subflow associated with the translator configuration.|Either a detect or a translate subflow is required for a valid translator configuration.|
|When multiple language code mappings are selected for the same language code|Multiple language code mappings cannot be selected for the same language code\(s\): xx.|

**Parent Topic:**[Reference for Dynamic Translation](reference-for-dynamic-translation.md)

