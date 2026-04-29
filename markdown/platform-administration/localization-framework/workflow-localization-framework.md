---
title: Workflows in the Localization Framework
description: Workflows in the Settings table define the process for a localization task, including steps for approval and methods for translating and publishing.
locale: en-US
release: australia
product: Localization Framework
classification: localization-framework
topic_type: reference
last_updated: "2026-03-20"
reading_time_minutes: 3
breadcrumb: [Explore Localization Framework, Localization Framework, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Workflows in the Localization Framework

Workflows in the Settings table define the process for a localization task, including steps for approval and methods for translating and publishing.

## Overview of workflows in the Settings table of Localization Framework

You can configure the path you want your localization task to follow, with available steps for approval, translation, and publishing. You can define these workflows for each language and artifact configured on your instance.

For more information about navigating to the configuration web form for these workflows, see [Configure the Localization Framework preferences](../task/define-translation-preferences.md).

<table id="table_mfm_th2_qnb"><thead><tr><th>

Workflows

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Translation → Publish

</td><td>

The localization task is translated manually or by using one of the translation modes. After translation, the content is published manually.Group needed: Assign the **Localization Fulfiller Group**.

</td></tr><tr><td>

Translation → Translation Approval → Auto Publish

</td><td>

The localization task is translated manually or by using one of the translation modes. After translation the task undergoes translation approval, then is auto-published.Groups needed: Assign the **Localization Fulfiller Group** and **Translation Approver Group**.

</td></tr><tr><td>

Auto Translation → Translation Approval → Auto Publish

</td><td>

The localization task undergoes auto-translation. After translation, the task undergoes translation approval, then is auto-published.Groups needed: Assign the **Localization Fulfiller Group**, **Auto Translation Mode**, and **Translation Approver Group**.

Select an [Auto Translation Mode](../concept/translation-modes.md).

</td></tr><tr><td>

Auto Translation → Publish

</td><td>

The localization task undergoes auto-translation and is published manually.Groups needed: Assign the **Localization Fulfiller Group** and **Auto Translation Mode**.

Select an [Auto Translation Mode](../concept/translation-modes.md).

</td></tr><tr><td>

Auto Translation → Auto Publish

</td><td>

The localization task undergoes auto-translation then is auto-published.Group needed: Assign the **Localization Fulfiller Group**.

Select an [Auto Translation Mode](../concept/translation-modes.md).

</td></tr><tr><td>

Business Approval → Translation → Publish

</td><td>

The localization task first requires business approval for localization. Next the content is translated manually or translated by using one of the translation modes. Finally the content is manually published.Groups needed: Assign the **Business Approver Group** and **Localization Fulfiller Group**.

</td></tr><tr><td>

Business Approval → Translation → Translation Approval → Auto Publish

</td><td>

The localization task first requires business approval for localization. Next the content is translated manually or by using one of the translation modes. After translation, the task undergoes translation approval then is auto-published.Groups needed: Assign the **Business Approver Group**,**Localization Fulfiller Group**, and **Translation Approver Group**.

</td></tr><tr><td>

Business Approval → Auto Translation → Translation Approval → Auto Publish

</td><td>

The localization task first requires business approval for localization. Next the content is auto-translated. After translation, the task undergoes translation approval then is auto-published.Groups needed: Assign the **Business Approver Group**,**Localization Fulfiller Group**, and **Translation Approver Group**.

Select an [Auto Translation Mode](../concept/translation-modes.md).

</td></tr><tr><td>

Business Approval → Auto Translation → Publish

</td><td>

The localization task first requires business approval for localization. Next the content is auto-translated but is manually published.Groups needed: Assign the **Business Approver Group** and **Localization Fulfiller Group**.

Select an [Auto Translation Mode](../concept/translation-modes.md).

</td></tr><tr><td>

Business Approval → Auto Translation → Auto Publish

</td><td>

The localization task first requires business approval for localization. The content is auto-translated then auto-published.Groups needed: Assign the **Business Approver Group** and **Localization Fulfiller Group**.

Select an [Auto Translation Mode](../concept/translation-modes.md).

</td></tr></tbody>
</table>**Parent Topic:**[Explore Localization Framework](../concept/exploring-localization-framework.md)

