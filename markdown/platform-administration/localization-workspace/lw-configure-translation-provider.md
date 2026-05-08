---
title: Configure a language provider
description: Set up language providers as part of configuring Localization Workspace. For each target language you can configure multiple providers with their pricing.
locale: en-US
release: australia
product: Localization Workspace
classification: localization-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Language setup in Localization Workspace, Configuring Localization Workspace, Localization Workspace, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure a language provider

Set up language providers as part of configuring Localization Workspace. For each target language you can configure multiple providers with their pricing.

## Before you begin

-   Install at least one target non-English [language](../../localization/concept/exploring-system-localization.md) on your instance.
-   Configure at least one [Translation Management System](../../localization-framework/concept/tms-configuration.md) \(TMS\) in Localization Framework, or one [machine translator configuration](../../dynamic-translation/concept/integration-with-other-translation-services.md) in Dynamic Translation. From version 2.0.2, you can access these tables in [Configuration Hub in Localization Workspace](../concept/lw-configuration-hub.md)
-   Role required: localization\_admin or admin.

## About this task

In Localization Workspace, a language provider is a record that combines:

-   a third-party service provider \(such as a TMS or machine translation API\)
-   a target language
-   a rate per unit \(the price your third-party service provider charges per word or character translated\)

The language provider record provides granular control over the execution of each task in your translation project, and supports the possibility of more than one service provider per target language.

This record also enables the calculation of the informational cost estimate.![The modal for Add new translation provider in Localization Workspace.](../image/lw-configure-translation-provider1.png)

**Note:** From version 3.0.0, a Guided Tour is available to assist localization admins with the setup of a language provider. Access the guided tour by selecting the Help Center icon ![](../../../common/image/Banner_HelpIcon.png)on the [Home](../concept/lw-status-synchronization.md) screen.

## Procedure

1.  Navigate to **All** &gt; **Localization Workspace** &gt; **Language setup** &gt; **Language Provider**.

2.  Select **New**.

3.  In the **Add a new language provider** window, enter the following information.

<table id="choicetable_az3_wjw_bfc"><thead><tr><th align="left" id="d243967e195">

Field

</th><th align="left" id="d243967e198">

Value

</th></tr></thead><tbody><tr><td id="d243967e204">

**Label**

</td><td>

Enter a descriptive name. This label is displayed in the **Language Providers** list.

</td></tr><tr><td id="d243967e216">

**Language**

</td><td>

Enter a language. You can search from among the languages you have configured on the instance.

</td></tr><tr><td id="d243967e225">

**Provider Type**

</td><td>

From the list, choose TMS \(Translation Management System\) or MT \(Machine Translation\). These provider types are available after you preconfigure them on your instance.

</td></tr><tr><td id="d243967e234">

**Rate**

</td><td>

Enter the base rate charged by your third-party service provider per word or character, without any volume discounts or overages. For more information see [Request translations in Localization Workspace: Estimate and Due Date](lw-estimate.md).You can choose a currency that is not in your user preferences. However, the informational cost estimate is displayed in the currency of the translation requester's user session.

This rate is used to calculate the informational cost estimate.

**Note:** When displayed on the Home page of Localization Workspace, the **Cost** uses a rate that is rounded up to the decimal place that is set in your **Display Value Currency** field. However, the calculation of the informational cost estimate for a translation request uses the actual rate that you have configured in Localization Workspace. The calculation does not use the currency's display value. For more information, see [Identify the FX Currency field and its display parameters](../../currency/task/fx-currency-display-parameters.md).

</td></tr><tr><td id="d243967e276">

**TMS \(or MT\) Configuration**

</td><td>

This field is dependent on your selection for **Provider Type**. Select from available providers that you have configured.For example, if you selected TMS as the Provider Type, and you have configured the XTM third-party provider, then **XTM** is available in the list.

</td></tr><tr><td id="d243967e293">

**Unit**

</td><td>

The Unit count multiplied by the Rate equals the informational cost estimate. Choose from **Word** or **Character**, according to the billing policy of your third-party service provider.The term Character in Localization Workspace corresponds to Unicode code point, which is the unit commonly used by machine translation service providers.

Check your service provider's documentation to confirm the unit used for pricing. For details about the pricing of Google Cloud Translator Service, see [https://cloud.google.com/translate/pricing](https://cloud.google.com/translate/pricing). For details about Microsoft Azure Translator, see [https://azure.microsoft.com/en-us/pricing/details/cognitive-services/translator/](https://azure.microsoft.com/en-us/pricing/details/cognitive-services/translator/).

</td></tr><tr><td id="d243967e331">

**Default provider for this language**

</td><td>

\(Optional\) Select this check box to set this provider as the default for this language in Localization Workspace.**Note:** The default provider in Localization Workspace is not related to the default translator in Dynamic Translation.

</td></tr></tbody>
</table>4.  Select **Add**.


## What to do next

With the localization\_admin role, edit an existing record as follows.

1.  Navigate to **All** &gt; **Localization Workspace** &gt; **Language setup** &gt; **Language Provider** tab.
2.  Select the record's Label in the **Language Providers** list.![The list view of Localization Workspace's Language Providers table, highlighting the value in the Label column for an example row.](../image/lw-configure-translation-provider2.png)
3.  The **Edit language provider** window opens. Modify any values.
4.  Save the record by selecting **Update**.

To delete a provider, select the check box next to its label, then select the **Delete** button.

**Note:** Updates to a provider are not applied to any translation requests currently in progress.

After you have configured individual language providers, you can optionally define Language Groups. Your users save time when creating translation requests by selecting a group rather than adding each language individually. For more information see [Configure language groups](lw-configure-language-groups.md).

**Parent Topic:**[Language setup in Localization Workspace](../concept/lw-language-setup.md)

