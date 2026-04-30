---
title: Dynamic Translation properties
description: Use the Dynamic Translation properties to customize, configure, and control the translation features.
locale: en-US
release: xanadu
product: Dynamic Translation
classification: dynamic-translation
topic_type: reference
last_updated: "2024-11-12"
reading_time_minutes: 1
breadcrumb: [Reference for Dynamic Translation, Dynamic Translation, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Dynamic Translation properties

Use the Dynamic Translation properties to customize, configure, and control the translation features.

Navigate to **Dynamic Translation** &gt; **Properties** to view and edit these properties.

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

</td></tr><tr><td>

Exclusion Frameworksn\_dt.dynamic\_framework.enable\_exclusion\_framework

</td><td>

Enables [Exclusion Framework](../concept/dyn-translation-exclusion-framework.md) on the instance. Defaults to enabled when Dynamic Translation is activated.

On a domain-separated instance, this property applies to all of the domains. It is not possible to enable Exclusion Framework on a per-domain basis.

</td></tr></tbody>
</table>