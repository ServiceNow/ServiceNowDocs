---
title: Import primary model content to a secondary model
description: When content in your primary NLU model is updated, you can import the updates directly to secondary models.
locale: en-US
release: australia
product: NLU Service
classification: nlu-service
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Multilingual model management, Natural Language Understanding, Enable AI experiences]
---

# Import primary model content to a secondary model

When content in your primary NLU model is updated, you can import the updates directly to secondary models.

## Before you begin

-   Activate the Localization Framework \(com.glide.localization\_framework.installer\) plugin. See [Localization Framework](https://www.servicenow.com/docs/access?context=localization-framework-landing&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
-   For Virtual Agent or AI Search models, create or use an existing primary model that has at least one secondary model.
-   Role required: nlu\_admin or admin.

## About this task

You can import content from a primary model to a secondary model after the initial translation. If you modify the primary model, those changes can be imported to your secondary models without the need to translate the entire primary model once again.

You can import primary model content to only one secondary model at a time.

## Procedure

1.  Navigate to **All** &gt; **NLU Workbench** &gt; **Models**.

    The Virtual Agent tab opens by default. Select the appropriate tab for your model.

2.  Access a secondary model that has been translated under the primary model, and on **Build and train your model**, select **View phase**.

    By default you are taken to the **Intents** tab.

3.  Select the **Check primary model for new content** button.

    ![The button for Check primary model for new content, on the Build and train your model phase.](../images/import-primary-content01U.png)

    The banner Import and translate the content to keep this model updated appears at the top of the screen, along with a summary of the updates in the primary model. ![The banner for "Import and translate the content to keep this model updated" is highlighted.](../images/import-primary-content02U.png)

    **Note:** By default, newly imported intents are disabled in secondary models. Activate any imported intents manually.

4.  In the banner, select **Import**.

5.  In the **Import and translate new content from your primary model** window, choose a translation method and select **Import**.

    ![The window for "Import and translate new content from your primary model". Choose how to translate new content.](../images/import-primary-content03U.png)

    The new content begins translating. When finished, the translated content must be reviewed.


## What to do next

Make sure that each of your secondary models receive the new content from the primary model. Review all the new, translated content before publishing the secondary models.

