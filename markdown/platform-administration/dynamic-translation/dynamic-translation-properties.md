---
title: Dynamic Translation properties
description: Use the Dynamic Translation properties to customize, configure, and control the translation features.
locale: en-US
release: australia
product: Dynamic Translation
classification: dynamic-translation
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference for Dynamic Translation, Dynamic Translation, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Dynamic Translation properties

Use the Dynamic Translation properties to customize, configure, and control the translation features.

Using the admin role, navigate to **Dynamic Translation** &gt; **Properties** to view and edit these properties.

**Note:** Some properties, such as Virtual Agent properties, appear in this module only when related plugins are activated.

<table id="table_cmc_hbh_fbb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Activity Stream

</td></tr><tr><td>

Allow list tablessn.dt.activity\_stream.allow\_list

</td><td>

List of tables \(comma-separated\) for which the option to translate the content is enabled on the activity streams \(work notes and comments\). Example: `sn_hr_core_case,task`.

-   Type: string
-   Default value: none

</td></tr><tr><td>

Block list tablessn.dt.activity\_stream.block\_list

</td><td>

List of tables \(comma-separated\) for which the option to translate the content is inactive on the activity stream \(work notes and comments\).Example: `change_request,sn_hr_core_case_payroll`.

-   Type: string
-   Default value: none

</td></tr><tr><td class="sub-head" colspan="2">

Exclusion Framework

</td></tr><tr><td>

Exclusion Frameworksn\_dt.dynamic\_framework.enable\_exclusion\_framework

</td><td>

Enables [Exclusion Framework](../concept/dyn-translation-exclusion-framework.md) on the instance. Defaults to enabled when Dynamic Translation is activated.

 On a domain-separated instance, this property applies to all of the domains. It is not possible to enable Exclusion Framework on a per-domain basis.

</td></tr><tr><td class="sub-head" colspan="2">

Virtual Agent

</td></tr><tr><td>

Enables dynamic translation for htmlcom.glide.cs.dynamic.translation.enable.html

</td><td>

Enables dynamic translation for html, including Output Text controls that contain html, in Virtual Agent. For more information see Default input and output rich controls for a custom chat integration.Installed with the Dynamic Translation for Virtual Agent plugin \(com.glide.cs.dynamic.translation.virtual\_agent\). For information see Using language detection and dynamic machine translation in Virtual Agent enhanced chat conversations.

</td></tr><tr><td>

Enables dynamic translation for messages that contain urls com.glide.cs.dynamic.translation.enable.translating.message.containing.urls

</td><td>

Enables dynamic translation for messages that contain URLs.Installed with the Dynamic Translation for Virtual Agent plugin \(com.glide.cs.dynamic.translation.virtual\_agent\). For information see Using language detection and dynamic machine translation in Virtual Agent enhanced chat conversations.

</td></tr></tbody>
</table>**Parent Topic:**[Reference for Dynamic Translation](reference-for-dynamic-translation.md)

