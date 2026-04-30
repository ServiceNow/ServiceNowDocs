---
title: Create a custom translator configuration
description: Configure Dynamic Translation for a third-party machine translation provider of your choice.
locale: en-US
release: xanadu
product: Dynamic Translation
classification: dynamic-translation
topic_type: task
last_updated: "2025-05-06"
reading_time_minutes: 3
breadcrumb: [Integrate with a translation service provider, Integration with other translation services, Dynamic Translation, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a custom translator configuration

Configure Dynamic Translation for a third-party machine translation provider of your choice.

## Before you begin

Ensure that the Dynamic Translation plugin \(com.glide.dynamic\_translation\) is activated.

Create subflows for your custom translation provider. See [Integrate with a translation service provider](integrate-translation-service-provider.md).

Create language code mappings as needed. For more information see [Language Code Mapping in Dynamic Translation](../concept/language-mapper-dt.md).

Role required: admin

## About this task

By default, Google and Microsoft translator configurations are available and ready for you to add your account details. Also by default the ServiceNow translator configuration, for language detection only, is available and active.

However, you can also configure a custom translator with the following procedure.

## Procedure

1.  Complete the prerequisites and confirm your application scope, then navigate to **All** &gt; **Dynamic Translation** &gt; **Translator Configurations**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_nyc_xct_shb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Identifier of the translator configuration.

</td></tr><tr><td>

Active

</td><td>

Option to activate the translator configuration.

</td></tr><tr><td>

Version

</td><td>

Version of the contract used in subflows.Version v3 is used in releases before Xanadu Patch 3. Version v4 is used in releases from Xanadu Patch 3.

</td></tr><tr class="sub-head"><td class="sub-head" colspan="2">

Preferences

</td></tr><tr><td>

Choose a translate subflow

</td><td>

Workflow Studio subflow that interacts with the translation service provider to translate the input text. Search for the subflow that you created in the previous procedure \([Integrate with a translation service provider](integrate-translation-service-provider.md)\).

</td></tr><tr><td>

Mark as default for translation

</td><td>

Option to mark the translator configuration as the default configuration for translation. When no translator configuration is specified while translating the text, the default configuration is used.

The ServiceNow translator configuration is for language detection only, so this check box is not available on that record.

-   The translator configuration must be active to be marked as default.
-   You can select only one translator configuration as default for translation.


</td></tr><tr><td>

Choose a detect subflow

</td><td>

Workflow Studio subflow that interacts with the machine translation provider to detect the language of the input text. Search for the subflow that you created in the previous procedure \([Integrate with a translation service provider](integrate-translation-service-provider.md)\).

</td></tr><tr><td>

Mark as default for detection

</td><td>

Option to mark the translator configuration as the default configuration for detection \(determining the language of the submitted text\). When no translator configuration is specified while detecting the text, the default configuration is used.

-   The translator configuration must be active to be marked as default.
-   You can select only one translator configuration as default for detection.


</td></tr><tr><td class="sub-head" colspan="2">

Language Code Mappings

</td></tr><tr><td>

Language code mappings

</td><td>

Mapping codes for languages to associate with the translator configuration record.Associate with the translator configuration record by selecting the magnifying glass icon \( ![Magnifying glass icon](../../localization-framework/image/magnifying_glass.png)\), then selecting the language code mapping.

-   Only languages for which the language code mapping was created are available for selection.
-   You can select only one language code mapping per language.
For more information, see [Create a language code mapping](create-language-code-mapping.md).

</td></tr></tbody>
</table>4.  Select **Submit**.


## What to do next

If you are on Xanadu Patch 3 or above, and want to use Exclusion Framework in Dynamic Translation, add your translation provider's exclusion tags. For more information, see [Add an Exclusion Provider Pattern](dyn-translation-exclusion-provider.md).

**Parent Topic:**[Integrate with a translation service provider](integrate-translation-service-provider.md)

