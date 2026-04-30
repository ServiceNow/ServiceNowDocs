---
title: Migrating NLU/keyword Virtual Agent topics to LLM topics
description: The topic migration workflow enables you to migrate your existing Natural Language Understanding \(NLU\)/keyword topics into new large language model \(LLM\) topics.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Getting started with Virtual Agent Designer, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Migrating NLU/keyword Virtual Agent topics to LLM topics

The topic migration workflow enables you to migrate your existing Natural Language Understanding \(NLU\)/keyword topics into new large language model \(LLM\) topics.

**Note:** An updated Assistant Designer Asset library user interface is available when you install Now Assist in Virtual Agent and turn on the Now Assist Topics skill. This content assumes that you have activated this skill and can see the list view. If this skill is not activated, you see the legacy UI and topics page. For more information, see [Virtual Agent Designer legacy topics page](../reference/vad-prev-topics-page.md).

Now Assist capabilities bring generative AI to Virtual Agent using LLM topics. With topic migration, there’s no need to manually recreate all your NLU and keyword topics to be LLM topics. You can select the topics that you want to migrate into LLM topics from your existing NLU and keyword topics. Migrating NLU and keyword topics doesn’t change the original NLU or keyword topics. A copy of the existing topic is created during topic migration, but the new topic's **Model Type** field is set to LLM and includes LLM-compatible nodes and descriptions.

All types of topics can be migrated from the NLU/Keyword model type to the LLM model type during topic migration, including the following asset types:

-   Topic
-   Topic block
-   Setup topic
-   Small talk
-   Custom input control
-   Custom response control

If no migration issues occur, the preceding asset types can all optionally be published except the topic block. Although dynamic topic blocks can be optionally published, the topic block type is automatically published after it's been migrated.

## Roles and accessibility

Users with the virtual\_agent\_admin role or sn\_vad\_genai.topic\_migration\_admin role can work with topic migration. Topic migration is accessible through Assistant Designer in the **Migrate Topics to LLM** option.

![Migrate Topics to LLM is an option in the Virtual Agent Designer header.](../images/llm-topic-migration-vad.png "Migrate Topics to LLM option in Virtual Agent Designer") ![Migrate Topics to LLM is an option in theAssistant Designer Asset library Resources sidebar.](../images/llm-topic-migration-vad-2.png "Migrate Topics to LLM option in Virtual Agent Designer")

## System properties

Use the system property **sn\_vad\_genai.utterances.count.for.topic.description** to set the maximum number of NLU utterances that can be given to the LLM to generate the topic description for an NLU topic migrated to an LLM topic.

## Topic descriptions

When migrating NLU topics to LLM topics, you can choose whether you want to have generative AI create your LLM topic descriptions. When on the Settings step of the topic migration workflow, you can choose to **Keep current topic descriptions?**. The **Keep current topic descriptions?** option is off by default. When this setting is off, generative AI pulls either NLU intent utterances or keywords from topics to create LLM topic descriptions during the migration process. If the topic is associated with an intent, a maximum of 10 utterances are pulled into the LLM topic's **Detail description** field under an `Additional instructions` value. When this setting is on, generative AI doesn’t create LLM topic descriptions and your existing NLU and keyword topic descriptions migrate into your new LLM topics. Migrating existing topic descriptions can result in issues if the existing topic doesn’t have a description.

The **Detail description** field is required for LLM topics but not for NLU/keyword topics. If a new LLM topic is migrated over with an empty description, you must add a description prior to that topic being published. Regardless of how topic descriptions migrate, you can edit topic descriptions during the Review descriptions step of the topic migration workflow. You can also test your topic descriptions against the original NLU topic's utterances, if applicable, to improve relevance and topic description strength.

**Note:** NLU utterances themselves are not effective if you use them as topic descriptions for LLM topics. Avoid using NLU utterances for LLM topic descriptions. LLM topic descriptions require more specific detailed information.

For more information on editing topic descriptions, see [Migrate NLU topics to LLM topics](../task/migrate-nlu-llm.md). For examples of strong topic descriptions, see [LLM description and instruction guidelines for Virtual Agent topics](va-llm-instruction-guidelines.md).

## Node descriptions

Although NLU topics' node names migrate exactly as-is during migration, the node descriptions can vary. NLU input nodes use the **Prompt** field. LLM input nodes use the **Detail description** field. During topic migration, the value in the **Prompt** field migrates into the **Detail description** field's value. How the value migrates can vary depending on if that value included text-only, scripts, or data pills. Refer to the following table to view how the values migrate differently and compare examples.

<table id="table_d4r_lhr_y1c"><thead><tr><th>

NLU Prompt field value

</th><th>

LLM Detail description field value

</th></tr></thead><tbody><tr><td>

Contains text

</td><td>

Migrates text as-is.For example, if the NLU **Prompt** field's value is `Enter the incident number`, then the LLM **Detail description** field's value is also `Enter the incident number`.

</td></tr><tr><td>

Contains script or data pill

</td><td>

Migrates using the following template: `Collect + Node name`.For example, if you have an NLU node named `Get incident number` and the **Prompt** field's value contains a script or data pill, then the migrated LLM node's **Detail description** field's value is `Collect Get incident number`.

</td></tr></tbody>
</table>If the topics that you plan to migrate include scripts or data pills in their existing **Prompt** field, review and update the LLM **Detail description** field after migration for each affected topic. A warning message of `Add relevant detail description` appears for LLM topics on the Virtual Agent Designer canvas for each node that migrated with the template of `Collect + Node name`. Updating the description to something more accurate and descriptive improves your users' experience of interacting with the Virtual Agent. For an example of a strong node description, see [LLM description and instruction guidelines for Virtual Agent topics](va-llm-instruction-guidelines.md).

The following entities can be migrated from NLU nodes to LLM nodes:

-   simple
-   mapped
-   pattern
-   system-derived

If an NLU node is mapped to an entity, those utterances' entities are added to the LLM node's **Detail description** field under an `Additional instructions:` make-shift header value. The `Additional instructions:` content differs slightly depending on the type of entity that is migrated. The layout of the **Detail description** field value resembles something like the following:

-   `[Prior NLU Prompt field value]` if the value was text-only and not a script or data pill.
-   `[Additional instructions: For this input, the data should be extracted from the user input if it has a value from this list of words: [simple entity word list].`

![Prompt field values migrate to the Detail description field values along with NLU entities.](../images/nlu-llm-node-prompt-detail-desc-example-2.png "Example of an NLU node with associated entities migrating to an LLM node")

If you had vocabulary sources established in your NLU topic's text nodes, the list and table vocabulary sources migrate into LLM nodes. Text nodes with list vocabulary sources are migrated into static choice nodes. The vocab source selections appear in the LLM static choice node's **Detail description** field under an `Additional instructions:` make-shift header value. Text nodes with table vocabulary sources are migrated into dynamic choice nodes. The vocabulary source's table is migrated into the LLM dynamic choice node's **Table** field. The vocabulary source selections are migrated into a script and appear in the LLM dynamic choice node's **Detail description** field under an `Additional instructions:` make-shift header value.

## Migration issues

You can access migration issue data either by searching for `topic_migration_execution_item.list` in the Navigation pane or downloading the .CSV file version of the table. After you've migrated topics, the downloadable .CSV file is accessible through the **Review migration log** option in the topic migration's Migrate topics step. For more information about migration issues, see [NLU to LLM migration log](../reference/llm-topic-migration-error-log.md).

-   **[Migrate NLU topics to LLM topics](../task/migrate-nlu-llm.md)**  
Migrate one or more of your existing Natural Language Understanding \(NLU\) or keyword topics into new large language model \(LLM\) topics while maintaining your original NLU/keyword topics. After migration is complete, choose whether to publish your new LLM topics.
-   **[NLU to LLM migration log](../reference/llm-topic-migration-error-log.md)**  
The Topic Migration Execution Items \[topic\_migration\_execution\_item.list\] table includes data when migrating Natural Language Understanding \(NLU\) topics to large language model \(LLM\) topics such as the migration status, migration issues, and migrated or published topic information.

**Parent Topic:**[Getting started with Virtual Agent Designer](../reference/conversation-designer-virtual-agent.md)

