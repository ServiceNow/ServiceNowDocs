---
title: Exclusion Framework in Dynamic Translation
description: Preserve text such as product names or technical terms during machine translation. With Exclusion Framework in Dynamic Translation, you can specify words and patterns that should not be translated.
locale: en-US
release: australia
product: Dynamic Translation
classification: dynamic-translation
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configuring Dynamic Translation, Dynamic Translation, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Exclusion Framework in Dynamic Translation

Preserve text such as product names or technical terms during machine translation. With Exclusion Framework in Dynamic Translation, you can specify words and patterns that should not be translated.

Exclusion Framework is a set of rules ensuring that your designated text bypasses the machine translation process and appears unchanged in the resulting output. Dynamic Translation applies Exclusion Framework rules to your text before submitting the request to your machine translation provider. Two types of rules are supported: Exact Match \(specific terms\) and Pattern Match \(regex\).

## Examples of text to consider for exclusion from machine translation

In response to your organization's business requirements, you can create Exclusion Framework rules for text strings such as the following.

<table id="table_cqf_zfy_cdc"><thead><tr><th>

Rule type

</th><th>

Examples

</th></tr></thead><tbody><tr><td>

Exact match

</td><td>

-   Product or company names
-   Acronyms, stock ticker symbols
-   Technical terms or identifiers
-   Terminology that has unique meaning in your organization

</td></tr><tr><td>

Pattern match

</td><td>

-   Case numbers, incident numbers
-   KB article numbers
-   Sys IDs

</td></tr></tbody>
</table>Review your organization's glossaries and taxonomies to identify candidates for exclusion.

## Activating Exclusion Framework

An upgrade to Xanadu Patch 3 or higher, when Dynamic Translation is active, includes activation of Exclusion Framework by default.

**Note:** Dynamic Translation requires a Professional or above subscription. For information see [Activate Dynamic Translation](../task/activate-dynamic-translation.md).

An upgrade to Xanadu Patch 3 or higher also converts the Dynamic Translation flows from v3 to v4. The v4 flows contain subflows for working with Exclusion Framework. Translator configurations available by default are automatically upgraded to v4. For more information, see [Migrate customized Translator Configurations to v4 flows](../task/migrate-v4-dynamic-translation.md).

A system property in **All** &gt; **Dynamic Translation** &gt; **Properties** enables you to activate or deactivate Exclusion Framework: sn\_dt.dynamic\_framework.enable\_exclusion\_framework.

Exclusion Framework appears as a module under Dynamic Translation.

![In the navigation pane, the module for Exclusion Framework in Dynamic Translation is displayed.](../image/dyn-translation-exclusion-framework1X.png "The Exclusion Framework module")

By default Exclusion Framework provides several exclusion rules, and you can add your own rules during configuration. ![The Dynamic Translation table of Exclusion rules](../image/dyn-translation-exclusion-framework2X.png)

## Configuring Exclusion Framework

Because Exclusion Framework is activated by default you can complete its configuration as follows.

1.  Ensure that your third-party machine translation service has an active record in the Exclusion Provider Pattern \[sn\_dt\_provider\_exclusion\_pattern\] table. If you have chosen a custom translator service you must input their exclusion tags. For information see [Add an Exclusion Provider Pattern](../task/dyn-translation-exclusion-provider.md).
2.  Review any existing records in the Exclusion Rules \[sn\_dt\_exclusion\_rules\] table to check whether they are appropriate for your needs. Rules that are provided by default can be deactivated by clearing the Active check box, but they can't be edited.
3.  Add more exclusion rules according to your organizational requirements. For information see [Add new rules to Exclusion Framework](../task/dyn-translation-add-exclusion-rule.md).

## Exclusion Framework's operational process

After configuration, Exclusion Framework's subflows operate within Dynamic Translation. The Exclusion Framework process is outlined as follows.

1.  Exclusion Framework searches the original text \(before translation\) to find any matches to terms and patterns that are active in the Exclusion Rules table.
2.  Any matches are wrapped in exclusion tags. These tags are pulled from the relevant record in the Exclusion Provider Pattern table.
3.  The tagged text is submitted to your machine translation provider.

Text that is wrapped in the exclusion tags is shielded from translation. It is written into the translation results in its original language, so the output contains unmodified text embedded in translated text.

## Domain separation support in Exclusion Framework

Exclusion Framework supports domain separation. Each domain on an instance can have its own set of Exclusion Framework rules, so the rules apply at the domain level. Within a domain, each rule must be unique. Create rules in the domain where you want them to operate.

When multiple domains exist on one instance, Exclusion Framework is activated on all domains. Deactivating Exclusion Framework on a per-domain basis isn't supported. As an alternative, deactivate every rule in a domain where you want Exclusion Framework to be inactive.

-   **[Add new rules to Exclusion Framework](../task/dyn-translation-add-exclusion-rule.md)**  
Add terms and patterns that shouldn't be machine translated to the Exclusion Rules table. You can create either exact match rules or pattern match rules, and you can edit your rules later.
-   **[Test Exclusion Rule](../task/dyn-translation-test-exclusion-rule.md)**  
Test Exclusion Rule in Dynamic Translation enables you to test your exclusion pattern manually. You can check whether the pattern accurately excludes a text string from translation.
-   **[Add an Exclusion Provider Pattern](../task/dyn-translation-exclusion-provider.md)**  
As part of the configuration of Exclusion Framework in Dynamic Translation, enter the tags used by your translation provider to mark text that should not be machine translated.

**Parent Topic:**[Configuring Dynamic Translation](configuring-dynamic-translation.md)

