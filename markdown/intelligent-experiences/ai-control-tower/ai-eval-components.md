---
title: Components installed with the Evaluation dashboard
description: Several types of components are part of the Evaluation tab, including scheduled jobs, tables, system properties, and flows.
locale: en-US
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Evaluation dashboard reference, Reference, AI Control Tower, Enable AI experiences]
---

# Components installed with the Evaluation dashboard

Several types of components are part of the Evaluation tab, including scheduled jobs, tables, system properties, and flows.

## Scheduled jobs installed

<table id="table_bps_dyg_ngc"><thead><tr><th>

Scheduled job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

CE Populate Value Aggregates Chats – Daily

</td><td>

This scheduled script runs daily and randomly selects 1000 conversations from yesterday's conversations. After that, for each conversation, this job extracts the chat duration and classifies them as small, medium, or large. It also classifies the chats in which a Knowledge article or catalog item was invoked. For the evaluated chat, it also classifies the conversations based on the chat performance and populates that data into the Evaluation Value Aggregates table.

</td></tr><tr><td>

Evaluation Value Calcuation - Runs Only once after install

</td><td>

Deletes all the records on the Evaluation Value Aggregates tables, runs the calculations again and stores the aggregated value in the Evaluation Value Aggregates table. The data is from the first evaluation date.

</td></tr></tbody>
</table>## Tables installed

<table id="table_xmn_qj4_hgc"><thead><tr><th>

Label

</th><th>

Name

</th></tr></thead><tbody><tr><td>

Evaluation

</td><td>

\[sn\_na\_conv\_eval\_evaluation\]

</td></tr><tr><td>

Evaluation configurations

</td><td>

\[sn\_na\_conv\_eval\_evaluation\_configurations\]

</td></tr><tr><td>

Evaluation Metrics

</td><td>

\[sn\_na\_conv\_eval\_evaluation\_metrics\]

</td></tr><tr><td>

Evaluation Set

</td><td>

\[sn\_na\_conv\_eval\_evaluation\_set\]

</td></tr><tr><td>

Evaluation Value Aggregates

</td><td>

\[sn\_na\_conv\_eval\_evaluation\_value\_aggregates\]

</td></tr></tbody>
</table>## Remote tables installed

<table id="table_ctm_hpp_hgc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Conversation Evaluator Value Calculations

 \[sn\_na\_conv\_eval\_st\_value\_calcs\]

</td><td>

For the given query, the definition for this remote table calculates the time savings and efficiency percentage for small, medium, and large chats. Also, it returns the time savings and efficiency when a Knowledge article or catalog item was invoked.

</td></tr><tr><td>

Conversation weekly calculations\[sn\_na\_conv\_eval\_weekly\_cals\]

</td><td>

For the given query, the definition for this remote table calculates the time savings and efficiency percentage for small, medium, and large chats for different weeks of the selected date range. Also, it returns the time savings and efficiency when aKnowledge article or catalog item was invoked for all the different weeks of the selected date range.

</td></tr></tbody>
</table>## System properties installed

<table id="table_nby_14p_hgc"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_na\_conv\_eval.errorBandMinRecords

</td><td>

Minimum number of records required to calculate the error band for upper and lower deviation. By default, the value is 30.

</td></tr><tr><td>

sn\_na\_conv\_eval.evalWeights

</td><td>

Contains weights to each evaluation metric for chat evaluation. This property is used to compute total or composite scores for evaluation records.

</td></tr><tr><td>

sn\_na\_conv\_eval.maxEvaluateCount

</td><td>

Maximum number of records to evaluate in a day. By default, the value is 200.

</td></tr><tr><td>

sn\_na\_conv\_eval.total\_sampled\_conv\_count

</td><td>

Edit this property to control the total number of conversations that can be sampled for value calculations. By default, the value is 1000.

</td></tr><tr><td>

sn\_na\_conv\_eval.value\_chat\_classifier

</td><td>

Edit this property to change the definition of small, medium, and large conversations. By default, the value it stores is 4, 10.

 Here, 4 and 10 signify the total number of inbound messages. Fewer than or equal to 4 inbound messages in the sys\_cs\_message table for a conversation means that it’s a small conversation. More than 4 inbound messages and fewer than or equal to 10 inbound messages means that it’s a medium conversation, and more than 10 inbound messages means that it’s a large conversation.

</td></tr><tr><td>

sn\_na\_conv\_eval.ce\_value\_calculation\_weights

</td><td>

Value calculation weight values for each type of evaluated chat.

</td></tr><tr><td>

sn\_na\_conv\_eval.eval\_value\_rerun\_status

</td><td>

Reruns the value calculations once after the installation. This property will check the status of the Conversation Evaluator Value Rerun status. If it has run, then the script will change the value of this system property to false.

</td></tr></tbody>
</table>## Business rules installed

|Name|When|Insert|Update|Filter Conditions|
|----|----|------|------|-----------------|
|Add info message for Evaluation set|after|TRUE|TRUE|stateCHANGESTOIn Progress^evaluation\_type=conversation^EQ|
|Scale Up labeling metric|before|TRUE|TRUE|metric\_type=Labeling^metric\_nameINhelpfulness\_chat\_eval,intent\_recognition\_chat\_eval,slot\_filling\_chat\_eval,forgetfulness\_chat\_eval,hallucination\_chat\_eval,redundancy\_chat\_eval,deadlock\_chat\_eval,coherence\_chat\_eval^raw\_scoreVALCHANGES^EQ|
|updateLabelingScoresOnEvaluation|after|TRUE|TRUE|metric\_type=Labeling^raw\_scoreVALCHANGES^metric\_nameINhelpfulness\_chat\_eval,intent\_recognition\_chat\_eval,slot\_filling\_chat\_eval,forgetfulness\_chat\_eval,hallucination\_chat\_eval,redundancy\_chat\_eval,deadlock\_chat\_eval,coherence\_chat\_eval^EQ|
|Update deviation scores|before|TRUE|TRUE|metric\_type=LLM Generated^scoreVALCHANGES^EQ|
|getAutoEvalCompositeScore|after|FALSE|TRUE|stateCHANGESTOComplete^total\_scoreISEMPTY^EQ|

## Flows installed

<table id="table_bcl_3sx_hgc"><thead><tr><th>

Flow

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Execute Evaluation

</td><td>

Performs evaluations when conversations are completed.

 By default, the Execute Evaluation flow is deactivated. You can use the nightly scheduled job Execute Evaluations to evaluate the chats. If you want to evaluate the chats on chat completion, activate the Execute Evaluation flow.

</td></tr><tr><td>

Execute Batch Evaluation

</td><td>

Performs batch evaluations, evaluating up to 100 completed virtual agent conversations. Flow is triggered when the Evaluation set is created or updated and the Evaluation Type is Conversation.

</td></tr></tbody>
</table>## Flow actions installed

<table id="table_q3c_tsx_hgc"><thead><tr><th>

Flow action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Randomize conversations

</td><td>

Performs randomization of conversations and returns 100 conversations randomly from a given query.

</td></tr><tr><td>

invokeApiDefinition

</td><td>

Invokes OneExtend Capability in the large language model \(LLM\).

</td></tr><tr><td>

Chat Classifier Eval

</td><td>

Gives the title, category, and whether the evaluation should be executed.

</td></tr><tr><td>

buildTranscript

</td><td>

Builds the transcript from a conversation.

</td></tr><tr><td>

evalExecuteCondition

</td><td>

Checks if the transcript is good enough to be evaluated.

</td></tr></tbody>
</table>## Script includes installed

<table id="table_atn_2tx_hgc"><thead><tr><th>

Script includes

</th><th>

Description

</th></tr></thead><tbody><tr><td>

evalExecuteCondition

</td><td>

Use this script include to update the evaluation condition.

</td></tr><tr><td>

evalUtils

</td><td>

Primary Utility function for the Evaluator.

</td></tr></tbody>
</table>**Related topics**  


[Remote tables](https://www.servicenow.com/docs/access?context=remote-tables&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)

