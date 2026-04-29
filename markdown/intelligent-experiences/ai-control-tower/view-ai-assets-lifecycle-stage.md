---
title: View AI assets by life-cycle stage
description: View AI assets based on the AI asset life-cycle stage that they are currently in. Use this information to determine which AI assets require your attention.
locale: en-US
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Use, AI Control Tower, Enable AI experiences]
---

# View AI assets by life-cycle stage

View AI assets based on the AI asset life-cycle stage that they are currently in. Use this information to determine which AI assets require your attention.

## Before you begin

Role required: sn\_ai\_governance.ai\_steward or sn\_ai\_asset\_mgmt.ai\_asset\_owner

## Procedure

1.  Navigate to **Workspaces** &gt; **AI Control Tower**.

2.  From the AI Control Tower, open the AI assets view.

3.  From the navigation menu of the AI assets view, locate the **Lifecycle** section.

    You can select **Cancel** to cancel AI asset.

4.  Depending on the life-cycle stage that you want to view AI assets for, select one of the following Lifecycle subsections:

    -   To view the list of AI assets that are currently in the New stage, select **New**.
    -   To view the list of AI assets that are currently in the assess stage, select **Assess**.
    -   To view the list of AI assets that are currently in the build and test stage, select **Build and test**.
    -   To view the list of AI assets that are currently in the deploy stage, select **Deploy**.
5.  Select an AI asset to launch the life-cycle review process or to view and modify additional details about the asset.

    -   To initiate the life-cycle review process for the asset, select **Start review** and then follow the proceeding steps in [Complete AI asset lifecycle](complete-ai-asset-lifecycle.md).
    -   To continue a life-cycle review that is already in progress, select the **Lifecycle** tab and then follow the proceeding steps in [Complete AI asset lifecycle](complete-ai-asset-lifecycle.md).
    -   To view or modify general details about the asset, select the **Details** tab and then navigate to **Details** &gt; **Details**.
    -   To view or modify the use and purpose of the asset, select the **Details** tab and then navigate to **Details** &gt; **Use &amp; purpose**.

        **Note:** This option is available only for AI systems.

    -   To view, modify, or add associations to other AI assets that are related to this asset, select the **Details** tab and then locate the **Related assets** section of the navigation menu. Select the subsection for the type of related AI asset that you want to view, modify, or add associations for.

        For example, if you want to view all datasets that can help train an AI model, select the **Training datasets** subsection.

        **Note:**

        If you want to associate the asset with additional related AI assets, select one of the following options from the Add from inventory drop-down menu:

        -   To associate the asset with a related AI asset that is already available in your asset inventory, select **Add from inventory**.
        -   To associate the asset with a related AI asset that is not already available in your asset inventory, select **Create**. This option is not available for related AI tools.
        You can then follow the proceeding steps in the corresponding AI asset creation topic:

        -   [Create AI system assets](create-ai-system-assets.md)
        -   [Create AI model assets](create-ai-model-assets.md)
        -   [Create prompt assets](create-prompt-assets.md)
        -   [Create dataset assets](create-dataset-assets.md)
    -   To view evaluation metrics for the asset, select the **KPIs &amp; metrics** tab.

        **Note:** This tab is available only for AI systems and AI models.

    -   To view, modify, or create value templates that are mapped to the asset, select the **Value template** tab.

        **Note:** This tab is available only for AI systems.

        For more information on value templates, see [Using value templates](../concept/using-value-templates.md).

    -   To view associated onboarding, change, and off-boarding requests for the asset, select the **Requests** tab.

        For more information on change and off-boarding requests, see [Creating requests for AI assets](../concept/creating-ai-asset-requests.md).

    -   To view the evaluations that are enabled for the asset, select the **Evaluation template** tab.

        **Note:** This tab is available only for AI systems.


