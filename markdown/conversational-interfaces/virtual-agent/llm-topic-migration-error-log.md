---
title: NLU to LLM migration log
description: The Topic Migration Execution Items \[topic\_migration\_execution\_item.list\] table includes data when migrating Natural Language Understanding \(NLU\) topics to large language model \(LLM\) topics such as the migration status, migration issues, and migrated or published topic information.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Migrating NLU/keyword Virtual Agent topics to LLM topics, Getting started with Virtual Agent Designer, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# NLU to LLM migration log

The Topic Migration Execution Items \[topic\_migration\_execution\_item.list\] table includes data when migrating Natural Language Understanding \(NLU\) topics to large language model \(LLM\) topics such as the migration status, migration issues, and migrated or published topic information.

You can access this topic migration data either by searching for `topic_migration_execution_item.list` in the Navigation pane or downloading the .CSV file version of the table. After you've migrated topics, the downloadable .CSV file is accessible through the **Review migration log** option in the topic migration workflow's Migrate topics step.

![Review migration log is an option available after topic migration is complete that appears in relation to the Migration progression status bar.](../images/llm-topic-migration-review-migration-log.png "Example of the Review migration log option")

The Topic Migration Execution Items \[topic\_migration\_execution\_item.list\] table defaults to include the following columns:

-   Description
-   Issues
-   LLM Topic
-   Migration Execution

    **Note:** The **Migration Execution** column includes the unique ID that is generated for each migration batch. For example, when 10 topics are migrated at the same time, the table contains 10 topic rows with each row containing the same migration execution value.

-   Migration status
-   NLU Topic
-   Status
-   Type

![Topic migration execution items log example with the following default columns: Description, Issues, LLM Topic, Migration Execution, Migration status, NLU Topic, Status, and Type.](../images/topic-migration-execution-item-log.png "Example of the Topic Migration Execution Items table data")

Generic issues may occur during the topic migration process. The following table includes specific, common issues that you may encounter in the Issues column and whether the issue blocks the topic from being published.

<table id="table_rwx_4sq_1bc"><thead><tr><th>

Issues column value

</th><th>

Types of issues

</th><th>

Can the topic be published?

</th></tr></thead><tbody><tr><td>

`Some topic properties couldn’t be generated. To publish, manually review and edit the following nodes: [list of node names]`

</td><td>

Node-level issues: These issues are validation error messages that can include missing fields such as name, description, and so on.

</td><td>

No.The issue must be corrected before the topic can be published.

</td></tr><tr><td>

`Some topic properties couldn’t be generated because the topic used a script. To publish, manually review and edit the following nodes: [list of node names]`

</td><td>

Script-level issues: These issues occur whenever an NLU input node has a script or data pill in the **Prompt** field.

</td><td>

Yes.Topics with this issue can be published because `Collect [Node Name]` populates in the **Detailed description** field, but the value of the **Detailed description** field value should be revised and improved.

</td></tr><tr><td>

`Some topic properties couldn't be generated. Edit them before publishing the topic.`

</td><td>

Topic-level issues: These issues are validation errors at the topic level such as a missing description, keywords, or any other required field.

</td><td>

No.The issue must be corrected before the topic can be published.

</td></tr><tr><td>

`The topic description couldn’t be generated. Edit the description field on the Publish page or from the topic properties page in Virtual Agent Designer before publishing.`

</td><td>

LLM-generated description issues: These issues occur whenever LLM is unable to generate a valid topic description.

</td><td>

Yes. Topics with this issue can be published because the `[Topic name]` populates the **Topic description** field, but the **Topic description** field value should be revised and improved.

</td></tr><tr><td>

`The topic description couldn’t be generated because the mapped intent wasn’t found. Edit the description field on the Publish page or from the topic properties page in Virtual Agent Designer before publishing.`

</td><td>

LLM-generated description issues related to NLU intent complications: These issues occur whenever an NLU model and intent is mapped to a topic but is missing from the sys\_nlu\_model or sys\_nlu\_intent table or if these values are incorrectly mapped to the topic.

</td><td>

Yes. Topics with this issue can be published because the `[Topic name]` populates the **Topic description** field, but the **Topic description** field value should be revised and improved.

</td></tr><tr><td>

`The topic description couldn’t be generated because both the intent and keywords are missing. Edit the description field on the Publish page or from the topic properties page in Virtual Agent Designer before publishing.`

</td><td>

LLM-generated description issues related to NLU intent complications: These issues occur whenever an NLU model's intent and keywords aren’t mapped to the topic.

</td><td>

Yes.Topics with this issue can be published because the `[Topic name]` populates the **Topic description** field, but the **Topic description** field value should be revised and improved.

</td></tr><tr><td>

`The migration tool couldn’t convert one or more dynamic topic block nodes from this topic. The topic blocks used inside the dynamic topic blocks must be manually migrated. The following nodes use these dynamic topic blocks: [list of node names]`

</td><td>

Dynamic topic block issues: These issues occur whenever there’s a node that has a dynamic topic block that wasn’t migrated.

</td><td>

Yes.Topics with this issue can be published because the topic block names use a script for dynamic topic blocks and continue to operate as expected, using the NLU topic block. If you encounter this issue, select these topic blocks for migration from the Select topics step and update the topic block names in the script.

</td></tr><tr><td>

`The migration tool couldn’t convert one or more switch topic scripts from this topic. The topics used inside the switch topic script need to be manually migrated. The following nodes use these switch topic scripts: [list of node names]`

</td><td>

Switch topic script issues: These issues occur whenever a node has a switch topic function that wasn’t migrated.

</td><td>

Yes.Topics with this issue can be published because the topic script continues to use the NLU topic until migration. If you encounter this issue, select these topics for migration from the Select topics step.

</td></tr><tr><td>

`This topic couldn't be migrated. Contact ServiceNow support for assistance.`

</td><td>

Process failure issues: These issues occur whenever there's an error during a particular migration process.

</td><td>

No. The issue must be corrected by a ServiceNow employee before the topic can be published.

</td></tr><tr><td>

`This topic couldn't be migrated because the transformation of NLU nodes to LLM nodes failed. Contact ServiceNow support for assistance.`

</td><td>

Process failure issues: These issues occur whenever there's an error during the transformation of NLU nodes to LLM nodes.

</td><td>

No.The issue must be corrected by a ServiceNow employee before the topic can be published.

</td></tr><tr><td>

`This topic couldn't be migrated because the publish payload failed to generate. Contact ServiceNow support for assistance.`

</td><td>

Process failure issues: These issues occur whenever there's an error during a particular migration process.

</td><td>

No.The issue must be corrected by a ServiceNow employee before the topic can be published.

</td></tr><tr><td>

`This topic can’t be published until a topic description is added.`

</td><td>

Process failure issues: These issues occur whenever there's an error during a particular migration process.

</td><td>

No. The issue must be corrected before the topic can be published. Edit the description field on the Publish step or from the topic properties page in an Virtual Agent Designer topic before publishing.

</td></tr></tbody>
</table>**Parent Topic:**[Migrating NLU/keyword Virtual Agent topics to LLM topics](../concept/llm-topic-migration.md)

