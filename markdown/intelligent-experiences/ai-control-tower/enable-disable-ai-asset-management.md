---
title: Enable or disable the management of an AI asset
description: Enable or disable the management of an AI asset by designating it as either managed or unmanaged.
locale: en-US
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use, AI Control Tower, Enable AI experiences]
---

# Enable or disable the management of an AI asset

Enable or disable the management of an AI asset by designating it as either managed or unmanaged.

## Before you begin

Role required: sn\_ai\_governance.ai\_steward

## About this task

If you designate an AI asset as managed, you can perform all life-cycle management and request creation processes on that asset. In addition, you can determine the risk classification, value, quality, and safety of the asset. If you designate an AI asset as unmanaged, you cannot perform any processes on it. By using these designations, you can streamline the asset management process and reduce operational risks. For more information on managed and unmanaged AI assets, see [Assets list managed and unmanaged assets](../concept/assets-list-managing-and-unmanaging-assets.md).

**Note:** By default, all AI assets that you create through the AI Control Tower application are automatically designated as managed.

## Procedure

1.  Navigate to **Workspaces** &gt; **AI Control Tower**.

2.  From the AI Control Tower, open the AI assets view.

3.  Depending on whether you want to enable or disable the management of an AI asset, proceed with one of the following options:

    -   If you want to enable the management of an AI asset, use the following steps:

        1.  From the navigation menu of the AI assets view, locate the **AI asset inventory - Unmanaged** section.
        2.  Select the subsection for the type of AI asset that you want to enable the management of.

            For example, if you want to enable the management of an AI system, select the **AI systems** subsection.

        3.  From the list of available AI assets, select the check box for the asset that you want to enable the management of.

            **Note:** If you want to enable the management of multiple assets, select the check box for each asset.

        4.  Select **Move to Managed**.
        5.  In the dialog box, select **Move to Managed**.
        The asset is designated as managed and automatically moves to the corresponding **AI asset inventory - Managed** subsection. The life-cycle review process, risk classification, value template calculations, and evaluations for the asset automatically initiate.

    -   If you want to disable the management of an AI asset, use the following steps:

        1.  From the navigation menu of the AI assets view, locate the **AI asset inventory - Managed** section.
        2.  Select the subsection for the type of AI asset that you want to disable the management of.

            For example, if you want to disable the management of an AI model, select the **AI models** subsection.

        3.  From the list of available AI assets, select the check box for the asset that you want to disable the management of.

            **Note:** If you want to disable the management of multiple assets, select the check box for each asset.

        4.  Select **Unmanage**.
        5.  In the dialog box, select **Unmanage**.
        The asset is designated as unmanaged and automatically moves to the corresponding **AI asset inventory - Unmanaged** subsection. The life-cycle review process, risk classification, value template calculations, and evaluations for the asset are automatically canceled.


