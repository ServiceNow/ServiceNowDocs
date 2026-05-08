---
title: Migrate NLU topics to LLM topics
description: Migrate one or more of your existing Natural Language Understanding \(NLU\) or keyword topics into new large language model \(LLM\) topics while maintaining your original NLU/keyword topics. After migration is complete, choose whether to publish your new LLM topics.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Migrating NLU/keyword Virtual Agent topics to LLM topics, Getting started with Virtual Agent Designer, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Migrate NLU topics to LLM topics

Migrate one or more of your existing Natural Language Understanding \(NLU\) or keyword topics into new large language model \(LLM\) topics while maintaining your original NLU/keyword topics. After migration is complete, choose whether to publish your new LLM topics.

## Before you begin

Role required: virtual\_agent\_admin or sn\_vad\_genai.topic\_migration\_admin

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**.

2.  Select **Migrate Topics to LLM**.

    ![Migrate Topics to LLM is an option in the Assistant Designer Asset library side panel.](../images/llm-topic-migration-vad.png)

    **Note:** An updated Assistant Designer Asset library user interface is available when you install Now Assist in Virtual Agent and turn on the Now Assist Topics skill. This content assumes that you have activated this skill and can see the list view. If this skill is not activated, you see the legacy UI and topics page. For more information, see [Virtual Agent Designer legacy topics page](../reference/vad-prev-topics-page.md).

    The Topic Migration workflow opens in a new browser tab.

3.  Review and determine which NLU and keyword topics you want to migrate into LLM topics on the Select topics step.

    ![Select topics step of the topic migration workflow enables you to select topics that you want to migrate from NLU and keyword topics to become new LLM topics.](../images/llm-topic-migration-select-topics.png "Select topics step")

    **Tip:** Select the link in the Name column to review the topic in the Virtual Agent Designer canvas in a new browser tab. Migrate fewer than 50 topics at one time to give yourself enough time to review the topics.

4.  Select which NLU and keyword topics you want to migrate, and then select **Next** on the Select topics step.

    **Important:** If you leave the topic migration workflow, you’re unable to return to where you left off and you must restart the process.

5.  Review the affected topic blocks, Virtual Agent notifications, and Proactive Triggers, and then select **Next** on the Review connections step.

    On the Topic blocks tab, only topic blocks and topic blocks connected with the selected topics are displayed in this list. Dynamic topic blocks must be manually selected for migration. You can select the link in the Topic Block column to view the topic block in the Virtual Agent Assistant Designer canvas in a new browser tab. Although dynamic topic blocks can be optionally published, topic blocks are automatically published after migration. The Virtual Agent Notifications and Proactive Triggers tabs only appear if the topics you've selected for migration have notifications or Proactive Triggers associated with the original NLU topic. You can select the link in the Topic Name column on their respective tabs to view the NLU topic in the Virtual Agent Designer canvas in a new browser tab. The LLM-compatible Virtual Agent notifications and Proactive Triggers are created and connected to the new LLM topics only after those topics are published through the last Publish step in the topic migration workflow.

    **Note:** The Proactive Triggers tab is only applicable if you've installed the Proactive Triggers \[sn\_pt\] app version 3.0.1 or later and have turned on this feature. If you'd prefer to manually migrate your actions for Virtual Agent notifications and Proactive Triggers rather than them automatically migrating after the Publish step, set the **com.glide.cs.notification.create\_llm\_actions\_after\_topic\_migration** and **com.glide.cs.proactive\_trigger.create\_llm\_actions\_after\_topic\_migration** system properties to `false` in **All** &gt; **System Properties** &gt; **All Properties**.

    ![Review topic blocks or notifications to see where they are used prior to continuing on in the topic migration workflow.](../images/llm-topic-migration-review-topic-blocks.png "Example of the Review connections step with the Topic blocks and Notifications tabs")

    **Note:** If no topic blocks, notifications, or Proactive Triggers were selected or connected to the selected topics, their respective tabs don’t appear.

6.  Choose which settings to apply to all topics migrating to LLM, and then select **Next** on the Settings step.

<table id="table_lrd_nww_1bc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Select assistant\(s\) for migrated topics

</td><td>

Migrated LLM topics are associated with these assistants. Associating topics to an assistant makes those topics discoverable with that assistant. For topic discovery results, associate LLM topics with an assistant.When you select an assistant, you can view whether that assistant is a primary or secondary assistant. When testing a primary assistant, topics from secondary assistants are included in topic discovery. When testing a secondary assistant, topics from primary assistants aren't included in topic discovery.

</td></tr><tr><td>

Choose how migrated topics are named

</td><td>

Newly migrated topics include the value entered in the **Add to internal topic name** field as either a prefix or suffix \(default\). This option only affects the migrated topics' **Internal name** value and not the topics' **Display name** value. The original NLU topic name is used as the **Display name** to customers interacting with LLM topics in Virtual Agent.

</td></tr><tr><td>

Keep current topic descriptions?

</td><td>

Current topic descriptions are used as the LLM topic descriptions rather than using generative AI to create topic descriptions for migrated LLM topics. This field is turned off by default. If this field is turned on, and there was no topic description in the original NLU topic, a topic description must be manually added to the new LLM topic before publication.

</td></tr></tbody>
</table>    ![Settings includes three main fields that you need to review including the Select assistants for migrated topics, Choose how migrated topics are named, and Keep current topic descriptions fields.](../images/llm-topic-migration-settings.png "Settings step")

7.  Review the topics for migration on the Migrate topics step, and then select **Next** to begin migration.

    **Note:** Leave the browser window open until the migration process is complete.

    ![When migrating topics is in progress, the screen dynamically updates with which topics are Not Started, In progress, Complete, or Failing migration.](../images/llm-topic-migration-migrate-topics-process-bar.png "Example of an in-progress topic migration")

    ![When topic migration is complete, the Download migration log option appears and you can select this option to view additional data on the success or failure of your topic migration.](../images/llm-topic-migration-migration-complete.png "Example of a completed topic migration")

    The migration complete progression bar appears and displays a dynamic percentage of completeness. During migration, the Migration status column updates dynamically with the values changing from `Not started` to either `Failed` or `Complete`. After migration is complete, any topic blocks selected, or those associated with the selected topics, are automatically published. You can choose to select **Download migration log** or **Next**. Selecting **Download migration log** downloads a .CSV file of the Topic Migration Execution Items \[topic\_migration\_execution\_item.list\] table data. For more information on this table data, see [NLU to LLM migration log](../reference/llm-topic-migration-error-log.md). Selecting **Next** continues the workflow to the Review descriptions step.

8.  Continue to the Review descriptions step by selecting **Next**.

    The new LLM topics that you've migrated appear, along with their migrated topic descriptions, and any available NLU utterances that were associated with the migrated topics' original NLU topics.

9.  Choose one of the following scenarios.

    **Note:** The display name, not the internal name, of the new LLM topics appears. The display name of the new LLM topics matches the existing NLU topic's display name. If you select the LLM topic link, you are redirected to that topic in Virtual Agent Designer through a new browser tab or window. For additional information about strong LLM topic descriptions, see [LLM description and instruction guidelines for Virtual Agent topics](../concept/va-llm-instruction-guidelines.md).

<table id="choicetable_vjq_sfm_wbc"><thead><tr><th align="left" id="d125850e504">

Option

</th><th align="left" id="d125850e507">

Description

</th></tr></thead><tbody><tr><td id="d125850e513">

**Edit topic description**

</td><td>

1.  Review the topic description of the new LLM topic.

All topic descriptions, either migrated from the existing NLU topic description or created by generative AI, are available for review. Topics that are missing topic descriptions must be updated before publishing.

2.  Edit the topic description, as needed.
3.  Select **Save description**.
4.  Repeat this process until all topic descriptions are reviewed and edited.


</td></tr><tr><td id="d125850e545">

**Edit topic description and test utterances**

</td><td>

This scenario is only applicable if there were NLU utterances connected to the original NLU topics.

 1.  Review the topic description of the new LLM topic.

All topic descriptions, either migrated from the existing NLU topic description or created by generative AI, are available for review. Topics that are missing topic descriptions must be updated before publishing.

2.  Edit the topic description, as needed.
3.  Select **Save and test with utterances**.

The original NLU topic's utterances are compared against the new LLM topic description. An overall percentage of matches appears along with an individual result by each utterance. These statuses are either `Matching` or `No match`. Use these statuses to adjust your topic description so that you more closely match your prior NLU utterances and retest. The LLM topic description doesn't have to use the exact NLU utterance wording for a match to occur. The context of the NLU utterance is referenced to determine the matching status.

4.  Repeat this process until all topic descriptions are reviewed and edited.


</td></tr></tbody>
</table>    ![No NLU utterances to test and only the edit description feature.](../images/llm-topic-migration-review-desc-no-utterance.png "Example of reviewing a topic description without NLU utterances")

    ![NLU utterances that match and do not match.](../images/llm-topic-migration-review-desc-utterances.png "Example of reviewing a topic description with NLU utterances")

10. Continue to the Publish step by selecting **Next**.

11. Select each LLM Topic check box that you want to publish, and then select **Publish topics**.

    ![The Publish topics option becomes available after you select LLM topics for publication.](../images/llm-topic-migration-publish-topics.png)

    **Tip:** If you select the LLM topic link, you’re redirected to that topic in Virtual Agent through a new browser tab or window. Any edits that you make in Virtual Agent Designer are reflected in the topic migration's Publish step. You must publish LLM topics through this step for any connected notifications or Proactive Triggers to work.

    You receive a `Selected topics were successfully published` output message. The topics that you migrated, but didn't select to publish, continue to appear on this step until you navigate away from the topic migration workflow.

12. Exit the topic migration workflow by selecting **Close**.

    You’re redirected to the Virtual Agent Designer Topics step.


## What to do next

After you navigate away from the topic migration workflow, the topics that you migrated, but didn’t publish, can be managed and published from the Virtual Agent Designer canvas. If you choose to migrate other topics in the future, the topic migration workflow restarts from the beginning.

**Parent Topic:**[Migrating NLU/keyword Virtual Agent topics to LLM topics](../concept/llm-topic-migration.md)

