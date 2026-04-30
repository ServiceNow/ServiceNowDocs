---
title: LLM description and instruction guidelines for Virtual Agent topics
description: When you create large language model \(LLM\) topics, you provide instructions that determine the behavior of the LLM and a description that determines how the topic is discovered by the LLM.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [LLM topic discovery in Virtual Agent, Exploring Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# LLM description and instruction guidelines for Virtual Agent topics

When you create large language model \(LLM\) topics, you provide instructions that determine the behavior of the LLM and a description that determines how the topic is discovered by the LLM.

## Overview of LLM description and instruction guidelines

Topic authors can use plain text wording to tell the LLM how to discover an LLM topic, as well as tell the LLM how to respond. The Virtual Agent Designer interface provides text fields that let you provide both.

-   **Descriptions**

    Topics require a description when you create them. The description is used for topic discovery, so the more detailed and specific the topic description is, the more likely it will be to find a good match.

-   **Instructions**

    When you add LLM user input controls to your conversation flow, you can provide instructions to the LLM in the **Detail description** field, which tells the LLM how to respond. You can use this field to define tone, employ small talk, or provide a dynamic greeting. Your instructions can also function as entity detection.


## General guidelines

When constructing an LLM description or instruction, consider these basic guidelines.

-   Lead with action verbs. Use the imperative form or direct commands.
-   Users should avoid answering a question with a question.

    For example, if the LLM asks `What is your question?`, the user response `Who is on call today?` can confuse the LLM. Instead, the user should enter `Tell me who is on call today.`

-   Avoid references to third parties or pronouns. Removing the subject or any identifiers generally prevents the LLM from personifying or otherwise misidentifying the end user.
-   Your words instruct the logic that your bot will use. Detailed, chain-of-thought instructions work well for this.
-   Continually test and refine your instructions. Creating strong LLM instructions is an iterative process.

## Don't use NLU utterances as LLM descriptions

NLU utterances are more dependent on keywords and their phrasing, but LLM descriptions work very differently. The problem with NLU utterances in descriptions is that they don't provide instructions for the LLM. Google search descriptions won't work well with LLMs, either. When writing descriptions, you need to be specific about the purpose of the topic and the context of the task being performed in that topic. Keywords aren't necessarily helpful, but logic is.

For more information, see [General guidelines for writing instructions for generative AI large language models \(LLMs\)](https://www.servicenow.com/docs/access?context=capabilities-bundle-landingpage&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

## Example topic descriptions

The following examples describe weak and strong topic descriptions. Stronger topic descriptions result in more accurate topic discovery.

|Strength|Description|
|--------|-----------|
|Weak description|This topic is about a holiday calendar for employees in a company.|
|Strong description|This topic is about a holiday calendar for employees in a company. Users can ask for the holiday list or company holiday for a specific year, specific date, inquire about a specific holiday, or ask if they have a day off for a particular holiday. The topic also covers the availability of a holiday calendar and specific holidays like Freedom Day and wellbeing Day.|

|Strength|Description|
|--------|-----------|
|Weak description|This topic is related to the management and administration of Active Directory, a directory service provided by Microsoft.|
|Strong description|This topic is related to the management and administration of Active Directory, a directory service provided by Microsoft. It involves making changes to the Active Directory, such as creating, modifying, or deleting directories and processes. The topic also includes tasks performed by administrators, such as managing user accounts, groups, and permissions within the Active Directory environment.|

## Example input control instructions

The **Node name** field should be unique and explain the operation the user is trying to perform, so that the LLM can identify entities and slot-fill properly. For example, if there are two defined input nodes named `AD Operation Type` and `AD Operation`, there is a chance the LLM could identify the entity and map it to the wrong input node variable. Renaming the nodes to differentiate the two is best. For example, `AD Operation for Password Reset` and `AD Operation for Locked Credentials and Change Password` are stronger, more unique node names.

The **Detail description** field for the node should have clear instructions for the possible values that the LLM should extract from the user wherever it is applicable. For example, if the node will perform an Active Directory operation, then you should be specific about which operations are allowed in the **Additional instructions for LLM** area. Then the LLM will use the value mapping to identify the entity and fill the slots.

The following example describes weak and strong input node instructions. The better instructions result improved outcomes.

<table id="table_n21_pb1_lbc"><thead><tr><th>

Strength

</th><th>

Detail description

</th></tr></thead><tbody><tr><td>

Weak instruction

</td><td>

Collect AD Operation Type

</td></tr><tr><td>

Strong instruction

</td><td>

Collect AD Operation Type **Additional instructions for LLM**: For this input, these are mapped values, : \{"reset":\["reset","locked","unable to sign in","expiry", "expired", "expire"\],"change":\["change"\]\}. The key needs to be extracted if the user input contains the values associated with the keys.

</td></tr></tbody>
</table>![Text input node with the Detail description field filled in to include specific entity information.](../images/llm-input-node-detail-desc-example.png "Strong detail description example of LLM input node")

