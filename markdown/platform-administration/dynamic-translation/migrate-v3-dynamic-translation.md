---
title: Migrate customized Translator Configurations to v3 flows
description: Implement the contract with subflows using complex objects in the input and output fields for dynamic translation of text.
locale: en-US
release: australia
product: Dynamic Translation
classification: dynamic-translation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integration with other translation services, Dynamic Translation, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Migrate customized Translator Configurations to v3 flows

Implement the contract with subflows using complex objects in the input and output fields for dynamic translation of text.

## Before you begin

Role required: admin

## About this task

**Important:** With the Xanadu Patch 3 release, default Translator Configurations are automatically updated to v4 flows. For more information, see [Migrate customized Translator Configurations to v4 flows](migrate-v4-dynamic-translation.md).

The previous v3 flows are still supported as follows. However, Exclusion Framework functionality may not be available with v3.

After an upgrading to releases prior to Xanadu Patch 3, default translator configurations that are not customized are automatically updated to v3 flows.

You need to manually migrate to version v3 for the following translator configurations:

-   Translator configurations that are available by default but customized from New York onwards.
-   Custom translator configurations that you added to integrate with a third-party translation service provider.

For a translator configuration that you added to integrate with a translation service provider of your choice, implement Integration Hub subflows with complex objects in the input and output fields. These subflows are required to interact with the translation service provider for language detection and translation. For information on this implemention, see [Integrate with a translation service provider](integrate-translation-service-provider.md).

## Procedure

1.  Navigate to **All** &gt; **Dynamic Translation** &gt; **Translator Configurations**.

2.  Select a translator configuration.

3.  In the Translator Configuration form, update these fields.

<table id="table_nyc_xct_shb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active

</td><td>

Activates the translator configuration to integrate with Dynamic Translation.

</td></tr><tr><td>

Version

</td><td>

Version of the contract used in subflows. Select **v3**.

</td></tr><tr><td>

Choose a translate subflow

</td><td>

Integration Hub subflow with complex objects in the input and output fields to translate the input text.-   For the translator configurations that are available by default but customized, select Translate Text \[translate\_text\_v3\].
-   For a translator configuration that you added to integrate with a translation service provider of your choice, select the subflow that you implemented with complex objects. The contract now supports multiple texts in a single method call.


</td></tr><tr><td>

Choose a detect subflow

</td><td>

Integration Hub subflow with complex objects in the input and output fields to detect the language of the input text.-   For the translator configurations that are available by default but customized, select Detect Language \[detect\_language\_v3\].
-   For a translator configuration that you added to integrate with a translation service provider of your choice, select the subflow that you implemented with complex objects. The contract now supports multiple texts in a single method call.


</td></tr><tr><td>

Mark as default for translation

</td><td>

Marks the translator as the default configuration for dynamic translation of text.

</td></tr><tr><td>

Mark as default for detection

</td><td>

Marks the translator as the default configuration to detect language of the input text.

</td></tr></tbody>
</table>4.  Select **Update**.


**Parent Topic:**[Integration with other translation services](../concept/integration-with-other-translation-services.md)

