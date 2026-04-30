---
title: Configure a translation provider
description: Set up translation providers as part of configuring Localization Workspace. For each target language you can configure multiple translation providers with their pricing.
locale: en-US
release: yokohama
product: Localization Workspace
classification: localization-workspace
topic_type: task
last_updated: "2025-06-18"
reading_time_minutes: 3
breadcrumb: [Configuring Localization Workspace, Localization Workspace, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure a translation provider

Set up translation providers as part of configuring Localization Workspace. For each target language you can configure multiple translation providers with their pricing.

## Before you begin

Configure at least one target non-English [language](../../localization/concept/exploring-system-localization.md) on your instance.

Configure at least one [Translation Management System](../../localization-framework/concept/tms-configuration.md) \(TMS\) in Localization Framework, or one [machine translator configuration](../../dynamic-translation/concept/integration-with-other-translation-services.md) in Dynamic Translation.

Role required: localization\_admin or admin

## About this task

In Localization Workspace, a translation provider is a record that combines:

-   a third-party translation service
-   a target language
-   a rate per unit \(the price your translation service charges per word or character translated\)

The translation provider record provides granular control over the execution of each task in your translation project, and supports the possibility of more than one service provider per target language.

This record also enables the calculation of the informational cost estimate.![The modal for Add new translation provider in Localization Workspace.](../image/lw-configure-translation-provider1.png)

## Procedure

1.  Navigate to **All** &gt; **Localization Workspace** &gt; **Translation Provider**.

2.  Select **New**.

3.  In the **Add new translation provider** window, enter the following information.

<table id="choicetable_az3_wjw_bfc"><thead><tr><th align="left" id="d228568e162">

Field

</th><th align="left" id="d228568e165">

Value

</th></tr></thead><tbody><tr><td id="d228568e171">

**Label**

</td><td>

Enter a descriptive name. This label is displayed in the **Translation Providers** list.

</td></tr><tr><td id="d228568e183">

**Language**

</td><td>

Enter a language. You can search from among the languages you have configured on the instance.

</td></tr><tr><td id="d228568e192">

**Provider Type**

</td><td>

From the list, choose TMS \(Translation Management System\) or MT \(Machine Translation\). These provider types are available after you preconfigure them on your instance.

</td></tr><tr><td id="d228568e201">

**Rate**

</td><td>

Enter the base rate charged by your translation provider per word or character, without any volume discounts or overages. For more information see [Request translations in Localization Workspace: Estimate](lw-estimate.md).You can choose a currency that is not in your user preferences. However, the informational cost estimate is displayed in the currency of the translation requester's user session.

**Note:** When displayed on the Home page of Localization Workspace, the **Rate** is rounded up to the decimal place that is set in your **Display Value Currency** field. However, the calculation of the informational cost estimate uses the actual rate that you have configured in Localization Workspace. The calculation does not use the currency's display value. For more information, see [Identify the FX Currency field and its display parameters](../../currency/task/fx-currency-display-parameters.md).

</td></tr><tr><td id="d228568e241">

**TMS \(or MT\) Configuration**

</td><td>

This field is dependent on your selection for **Provider Type**. Select from available providers that you have configured.For example, if you selected TMS as the Provider Type, and you have configured the XTM third-party provider, then **XTM** is available in the list.

</td></tr><tr><td id="d228568e258">

**Unit**

</td><td>

The Unit count multiplied by the Rate equals the informational cost estimate. Choose from **Word** or **Character**, according to the billing policy of your third-party translation service.The term Character in Localization Workspace corresponds to Unicode code point, which is the unit commonly used by machine translation services.

Check your service provider's documentation to confirm the unit used for pricing. For details about the pricing of Google Cloud Translator Service, see [https://cloud.google.com/translate/pricing](https://cloud.google.com/translate/pricing). For details about Microsoft Azure Translator, see [https://azure.microsoft.com/en-us/pricing/details/cognitive-services/translator/](https://azure.microsoft.com/en-us/pricing/details/cognitive-services/translator/).

</td></tr><tr><td id="d228568e296">

**Default provider for this language**

</td><td>

\(Optional\) Select this check box to set this translation provider as the default for this language in Localization Workspace.**Note:** The default provider in Localization Workspace is not related to the default translator in Dynamic Translation.

</td></tr></tbody>
</table>4.  Select **Submit**.


## What to do next

Edit an existing record as follows.

1.  With the localization\_admin role, select the record's Label in the **Translation Providers** list.![The list view of Localization Workspace's Translation Providers table, highlighting the value in the Label column for an example row.](../image/lw-configure-translation-provider2.png)
2.  The **Edit translation provider** window opens. Modify any values.
3.  Save the record by selecting **Update**.

**Note:** Updates to a translation provider are not applied to any translation requests currently in progress.

**Parent Topic:**[Configuring Localization Workspace](../concept/configuring-localization-workspace.md)

