---
title: Create the More Information workflow in the Asset Refresh topic
description: In our example, we must provide the workflow for the "more information" Decision branch. If the user wants to learn more before upgrading, we can point them to a specific KB article explaining how your organization's policy works.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
keywords: [More Information, Asset Refresh, topic, workflow, KB, AI Search]
breadcrumb: [Example Asset Refresh Virtual Agent conversation with notifications, Virtual Agent chat widget interface for NLU, Explore, Virtual Agent, Conversational Interfaces]
---

# Create the More Information workflow in the Asset Refresh topic

In our example, we must provide the workflow for the "more information" Decision branch. If the user wants to learn more before upgrading, we can point them to a specific KB article explaining how your organization's policy works.

## Before you begin

-   [Create the Asset Refresh topic in Virtual Agent Designer](create-example-conv-asset-refresh.md)
-   [Create the Open Incident workflow in the Asset Refresh topic](create-example-asset-refresh-flow2.md)

Role required: virtual\_agent\_admin or admin

## Procedure

1.  Open the Asset Refresh topic in Virtual Agent Designer.

2.  Return to the **info** decision branch after the Continue or Defer static choice node where you first prompted the user to continue or get more information.

    1.  From the Components area, drag a Topic Block utility node onto the canvas.

    2.  In the properties palette, select **AI Search** for the Topic block.

    3.  Under Input mapping, specify the search term.

        For example, enter `hardware upgrade policy`.

        ![Enter the search string in the Search Term field.](../images/crawl-ex-run-ai-search-string.png)

3.  Show the results of the search to the user.

    1.  From the Components area, drag a Card bot response node onto the canvas.

    2.  In the properties palette, specify the following information:

        -   A unique name, such as `Upgrade KB Articles`.
        -   Card type: **Record**
        -   Populate this card by referencing: **Table**
        -   Table name: **Knowledge Article \[sn\_km\_mr\_st\_kb\_knowledge\]**
        -   In the Condition builder, restrict the results to specific internal KB numbers that describe the policy, such as **Number is KB000000456**.

            ![In the condition builder, specify a specific KB article or a range of articles. For example, Number is KB000000456.](../images/crawl-ex-poss-ai-search-results.png)

        -   In the **fields** area, select **Content** for a single KB article, or **Short description** if multiple records are returned.
4.  Once the user has read the KB article, give them the option to continue with the upgrade.

    1.  From the Components area, drag a Static choice input node onto the canvas.

    2.  In the properties palette, enter the following information:

        -   A unique name, such as `Upgrade Next Steps`.
        -   A text prompt, such as `Would you like to upgrade now?`
        -   In the Choices area, provide a text prompt for each choice and a value for that choice, so you can refer to it later on.

            For example, your choices might be `Yes, upgrade now` and `No, maybe later`. The values should make sense as variable names. For example, `yes` and `no`.

        ![Static choice properties for "Upgrade Next Steps" node. It includes a user prompt and two choices: Yes, upgrade now or No, maybe later.](../images/crawl-ex-upgrade-now-later.png)

5.  Add a Decision utility to handle the user's choice.

    1.  From the Components area, drag a Decision utility onto the canvas.

    2.  Select the plus icon to add a second branch.

    3.  Name each branch to correspond with the static choice node decisions \(yes and no\).

    4.  For each branch, select it and then use the Branch Condition area to indicate which option the branch will follow.

        ![Use the condition builder to specify the Upgrade Next Steps choice node and the corresponding user choice that this branch will follow, such as "Yes, upgrade now."](../images/crawl-ex-condition-upgrade-now.png)

    5.  Drag the `no` flow's arrow to the End node to complete this part of the workflow.

    6.  Drag the `yes` flow's arrow to the Asset Lookup node to bring the user to the upgrade workflow.

6.  Select **Save**.


## Result

Your topic is ready to test. Test the topic, making sure you go through each possible workflow in the conversation and make any needed adjustments.

For more information about testing topics, see [Testing NLU/Keyword topics](../reference/va-designer-testing.md). If you're using NLU discovery, [add utterances](modify-nlu-utterances-va-topic.md) to the intent and [train and test your NLU model.](train-test-publish-nlu-model-vad.md)

When you're finished, [publish the topic](publish-virtual-agent-topic.md).

## What to do next

[Create the notification for the Asset Refresh topic](create-example-asset-refresh-notification.md)

**Related topics**  


[Improving the user experience with AI Search](../concept/va-ai-search.md)

