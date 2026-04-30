---
title: Workflows in the Localization Framework
description: Workflows define actions for completing a localization task. Each localization task undergoes the workflow configured for its target language to complete the task.
locale: en-US
release: yokohama
product: Localization Framework
classification: localization-framework
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Explore Localization Framework, Localization Framework, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Workflows in the Localization Framework

Workflows define actions for completing a localization task. Each localization task undergoes the workflow configured for its target language to complete the task.

<table id="table_mfm_th2_qnb"><thead><tr><th>

Workflows

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Translation → Publish

</td><td>

The localization task undergoes translation manually or by using one of the translation modes. After translation, the content gets published manually. **Note:** Ensure that you assign the **Localization Fulfiller Group** for the workflow to localize the content.

</td></tr><tr><td>

Translation → Translation Approval → Auto Publish

</td><td>

The localization task undergoes translation manually or by using one of the translation modes. After translation, the task undergoes translation approval and gets auto-published.**Note:** Ensure that you assign the **Localization Fulfiller Group** and **Translation Approver Group** for the workflow to localize the content.

</td></tr><tr><td>

Auto Translation → Translation Approval → Auto Publish

</td><td>

The localization task undergoes auto-translation. After translation, the task undergoes translation approval and gets auto-published.**Note:** Ensure that you assign the **Localization Fulfiller Group**, **Auto Translation Mode**, and **Translation Approver Group** for the workflow to localize the content.

</td></tr><tr><td>

Auto Translation → Publish

</td><td>

The localization task undergoes auto-translation and gets published manually.**Note:** Ensure that you assign the **Localization Fulfiller Group** and **Auto Translation Mode** for the workflow to localize the content.

</td></tr><tr><td>

Auto Translation → Auto Publish

</td><td>

The localization task undergoes auto-translation and gets auto-published.**Note:** Ensure that you assign the **Localization Fulfiller Group** and **Auto Translation Mode** for the workflow to localize the content.

</td></tr><tr><td>

Business Approval → Translation → Publish

</td><td>

The localization task needs business approval for localization. The content gets translated manually or translated by using one of the translation modes. The content gets manually published.**Note:** Ensure that you assign the **Business Approver Group** and **Localization Fulfiller Group** for the workflow to localize the content.

</td></tr><tr><td>

Business Approval → Translation → Translation Approval → Auto Publish

</td><td>

The localization task needs business approval for localization, and the content gets translated manually or by using one of the translation modes. After translation, the task undergoes translation approval and gets auto-published.**Note:** Ensure that you assign the **Business Approver Group**,**Localization Fulfiller Group**, and **Translation Approver Group** for the workflow to localize the content.

</td></tr><tr><td>

Business Approval → Auto Translation → Translation Approval → Auto Publish

</td><td>

The localization task needs business approval for localization, and the content gets auto-translated. After translation, the task undergoes translation approval and gets auto-published.**Note:** Ensure that you assign the **Business Approver Group**,**Localization Fulfiller Group**, **Auto Translation Mode**, and **Translation Approver Group** for the workflow to localize the content.

</td></tr><tr><td>

Business Approval → Auto Translation → Publish

</td><td>

The localization task needs business approval for localization. The content gets auto-translated but gets manually published.**Note:** Ensure that you assign the **Business Approver Group**,**Localization Fulfiller Group**, and **Auto Translation Mode** for the workflow to localize the content.

</td></tr><tr><td>

Business Approval → Auto Translation → Auto Publish

</td><td>

The localization task needs business approval for localization. The content gets auto-translated and auto-published.**Note:** Ensure that you assign the **Business Approver Group**, **Localization Fulfiller Group**, and **Auto Translation Mode** for the workflow to localize the content.

</td></tr></tbody>
</table>**Parent Topic:**[Explore Localization Framework](../concept/exploring-localization-framework.md)

