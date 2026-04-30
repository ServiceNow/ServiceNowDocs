---
title: Migrate customized Translator Configurations to v4 flows
description: Migrate your customized translator configurations to v4 flows. Version 4 flows for Dynamic Translation are available from the Xanadu Patch 3 release.
locale: en-US
release: xanadu
product: Dynamic Translation
classification: dynamic-translation
topic_type: task
last_updated: "2025-01-21"
reading_time_minutes: 1
breadcrumb: [Integration with other translation services, Dynamic Translation, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Migrate customized Translator Configurations to v4 flows

Migrate your customized translator configurations to v4 flows. Version 4 flows for Dynamic Translation are available from the Xanadu Patch 3 release.

## Before you begin

Role required: admin

## About this task

After upgrading to Xanadu Patch 3 or above, the update to v4 flows is automatically applied to default translator configurations that are not customized.

You must manually migrate custom or customized translator configurations.

Using v4 flows ensures that the functionality of [Exclusion Framework in Dynamic Translation](../concept/dyn-translation-exclusion-framework.md) is available.

## Procedure

1.  Navigate to **All** &gt; **Dynamic Translation** &gt; **Translator Configurations**.

2.  Select the translator configuration that you want to migrate to v4 flows.

3.  In the Translator Configurations form, update the fields according to the following guidance.

<table id="table_kyl_vm3_zdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active

</td><td>

Activates the translator configuration.

</td></tr><tr><td>

Version

</td><td>

Version of the contract used in subflows. Select v4.

</td></tr><tr><td>

Choose a translate subflow

</td><td>

The subflow to translate the input text.For default translator configurations that were customized, select Translate Text .

</td></tr><tr><td>

Choose a detect subflow

</td><td>

The subflow to detect the input text.For default translator configurations that were customized, select Detect Language .

</td></tr><tr><td>

Mark as default for translation

</td><td>

Marks the translator as the default provider for dynamic translation of text.

</td></tr><tr><td>

Mark as default for detection

</td><td>

Marks the translator as the default provider for detection of the language of the input text.

</td></tr></tbody>
</table>4.  Select **Update**.


**Parent Topic:**[Integration with other translation services](../concept/integration-with-other-translation-services.md)

