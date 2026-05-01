---
title: General guidelines for writing instructions for generative AI large language models \(LLMs\)
description: When using Now Assist products and skills, you may have the option to give specific instructions or other guidance to the LLM. Writing generative AI instructions is different from conducting a keyword search. Use the following general guidelines when crafting your instructions.
locale: en-US
release: zurich
product: ServiceNow Large Language Model \(Now LLM\)
classification: servicenow-large-language-model-now-llm
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 8
keywords: [LLM, Large language model, writing, guidelines, instructions, Now Assist, GenAI, Generative AI]
breadcrumb: [Large language models on the ServiceNow AI Platform, Enable AI experiences]
---

# General guidelines for writing instructions for generative AI large language models \(LLMs\)

When using Now Assist products and skills, you may have the option to give specific instructions or other guidance to the LLM. Writing generative AI instructions is different from conducting a keyword search. Use the following general guidelines when crafting your instructions.

Writing instructions for generative AI is very different from using search keywords. Keywords are the words that you might expect to appear in your results. For example, if you search for "gray bobtail cats," then you can reasonably expect your search results to return with topics or media that is about gray cats, bobtail cats, or even just cats in general. But with generative AI, you are asking the LLM to perform a task for you. The phrase "gray bobtail cats" does not include a verb to tell the LLM what to do. What about these gray cats? Should it locate all there is to know about them? Should it find gray bobtail cats to adopt? Should it create a picture of a gray bobtail cat? Should it be a realistic picture, or more of a line drawing? Generative AI needs more than just keywords.

## General LLM instructions

Use instructions or questions to tell the LLM what you want. They can include four parts:

-   **Goal**

    What kind of result do you want from the LLM?

    Example: `I want a list of 3-5 bullet points to prepare me...`

-   **Context**

    Why do you need it, and who is involved?

    Example: `...for an upcoming meeting with [client], focusing on their current state and what they're looking to achieve with their "Phase 3+" brand campaign.`

-   **Expectations**

    How should the LLM best fulfill your request?

    Example: `Please use simple language so I can get up to speed quickly.`

-   **Source**

    What information or other resources would you like the LLM to use?

    Example: `Focus on email and Teams chats with [people] since June.`


![Instructions for the LLM that includes a goal, some context, your expectations, and sources to be used.](../images/general-na-prompt-instructions.png "Sample LLM instructions")

Continually test and refine your instructions. Creating good LLM instructions is an iterative process, and as the LLM model learns, you may want to modify your instructions over time.

## Stating your goal

When constructing an LLM description or instruction, consider these basic guidelines.

-   Lead with action verbs. Use the imperative form or direct commands.
-   Be direct and use simple sentences rather than complex ones.
-   Be specific.
-   Don't use jargon or slang terms.
-   Avoid references to third parties or pronouns. Removing the subject or any identifiers generally prevents the LLM from personifying or otherwise misidentifying the end user.
-   Your words instruct the logic that generative AI will use. Detailed, chain-of-thought instructions work well for this.

Instructions should also be tailored to the type of task. The following table describes the different kinds of tasks and the sort of instructions you might write for each circumstance.

|Task type|Description|Example instruction|
|---------|-----------|-------------------|
|Simple search|Simple search for an answer.|When is the next company holiday?|
|Answer|Gather information from multiple sources and provide a summarized answer.|What were the major customer support issues in the past 30 days?|
|Chat|A back-and-forth conversation in which the LLM is getting additional information from the requester.|I have a new phone and now I can’t access Okta.|
|Create|Create a new ServiceNow component.|Write a new KB on common reasons for slow query execution and how to fix it, based on problems created in the last 12 months.|
|Workflow|Leverage existing workflows and create conversations from them.|Reset my Okta password.|

![Different kinds of LLM task instructions can be provided to the LLM, which then displays results to the requester. The types of instruction include answers, workflows, search, chat, and create.](../images/types-llm-task-instructions.png "LLM instruction workflow")

## Providing context in your instructions

Providing context to the LLM may feel like you are stating the obvious. For example, you may need to explain why your user would want to perform the task, or explain more about what the task is about. If you're using language that could have alternative meanings, you may want to define your terms. For example, if your instructions are about Microsoft Teams, you may need to say something like, "Teams refers to Microsoft Teams, an application that employees in a company can use to communicate with one another individually or in groups."

When providing context, think about the target audience for the task. This will help you to write better instructions. Mentioning whom the task is for also helps the LLM carry out the task.

Types of users to consider:

-   **Admins**

    Admins configure skills in the Now Assist Admin console. They work with platform owners and product owners for tasks and requirements. Subject-matter experts check the accuracy of generative AI results. Governance boards or committees may oversee final sign-off on the skill.

-   **Builders**

    Builders create assets such as applications and workflows. Their skill level may vary from no-code, low-code, mid-skill, or high-skill. They mostly interact with each other and admins.

-   **Agents**

    Agents provide technical assistance, customer support, or other problem-solving help for users of a product, service, or organization. Agents work with their peers and support many kinds of requesters.

-   **Requesters**

    Requesters may include your organization's employees, partners, or customers. Requesters encounter generative AI mostly in a self-service context. Generative AI provides the opportunity to requesters to solve the problem themselves before they resort to asking an agent for help.


In addition, you may need to "instruct" the LLM how to arrive at the kind of answer you want. Detailed chain-of-thought instructions are more likely to produce the results you're looking for. If you make assumptions in your instructions, your results may vary wildly.

<table id="table_kjx_zkq_mbc"><thead><tr><th>

Standard instructions

</th><th>

Chain-of-thought instructions

</th></tr></thead><tbody><tr><td>

Q: Start with 5 tennis balls. Buy 2 more cans of tennis balls. Each can has 3 tennis balls. How many tennis balls are there now?

 A: The answer is 11.

 Q: The cafeteria had 23 apples. If the cafeteria used 20 to make lunch and bought 6 more, how many apples does the cafeteria have?

</td><td>

Q: Start with 5 tennis balls. Buy 2 more cans of tennis balls. Each can has 3 tennis balls. How many tennis balls are there now?

 A: There are 5 balls. 2 cans of 3 tennis balls each is 6 tennis balls. 5+6=11. The answer is 11.

 Q: The cafeteria had 23 apples. If the cafeteria used 20 to make lunch and bought 6 more, how many apples does the cafeteria have?

</td></tr><tr class="sub-head"><td>

LLM results \(incorrect!\)

</td><td>

LLM results \(correct!\)

</td></tr><tr><td>

A: The answer is 27.

</td><td>

A: The cafeteria had 23 apples originally. They used 20 to make lunch. So they had 23-20=3. They bought 6 more apples, so they have 3+6=9. The answer is 9.

</td></tr></tbody>
</table>## Expectations

You can specify how you want your results to sound and look. For example, you can tell the LLM what kind of tone you want it to use.

<table><thead><tr><th>

Instruction

</th><th>

LLM result

</th><th>

Evaluation of result

</th></tr></thead><tbody><tr><td>

Greet the user with a casual, laid-back tone.

</td><td>

Hey there! \(: Welcome to May 22, 2024, a Wednesday. Chill and have a great day!

</td><td>

Too casual!

</td></tr><tr><td>

Greet the user with a professional, business-like tone.

</td><td>

Good day, welcome to our business. How may I assist you today?

</td><td>

A little too formal.

</td></tr><tr><td>

Greet the user with a professional, but friendly tone.

</td><td>

Hello there! I'm glad to assist you today, May 22, 2024. How can I help you?

</td><td>

Great, but I don't want the date.

</td></tr><tr><td>

Greet the user with a professional, but friendly tone. Do not include the date.

</td><td>

Hello! I'm here to help. How can I assist you today?

</td><td>

Perfect.

</td></tr><tr><td>

Instruction

</td><td>

LLM result

</td><td>

Evaluation of result

</td></tr></tbody>
</table>In some Now Assist applications, you may have the option to specify formatting. In those cases, you can tell the LLM to provide answers in a bulleted list, for example. Bulleted lists are often easier to read.

![In the Now Assist Admin console, some skills allow you to specify formatting. The chat summarization skill has an option to render results in a bulleted list.](../images/enable-bulleted-list-chat-summarization.png "Enabling bulleted list results in the chat summarization skill")

## Source

You can suggest a variety of sources that the LLM should use to find answers, including Microsoft Teams conversations, Microsoft SharePoint Online sites, incidents and cases, and internal knowledge articles. In order for an agent or skill to access all of these sources, an admin must configure access on the instance.

For developers, the sources that a skill or AI agent can access may vary depending on the desired outcome. For example, the incident summarization skill uses the Incident table as its source. AI agents use different tools and knowledge sources, customized for the task they perform.

For more information about configuring sources for skill or AI agent use, see the following topic areas:

-   [AI Search](https://www.servicenow.com/docs/access?context=overview-ais&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)
-   [Now Assist in AI Search](https://www.servicenow.com/docs/access?context=now-assist-ais&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)
-   [External Content Connectors](https://www.servicenow.com/docs/access?context=ext-cont-connectors-landing-page&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)
-   [Overview tab in Now Assist Admin](configuring-now-assist.md)
-   [Now Assist AI agents](../../now-assist-ai-agents/reference/na-ai-agents.md)

## Additional guidelines for Now Assist skills and tools

|Skill|Reference|
|-----|---------|
|App generation|[General guidelines for using Now Assist for app generation in ServiceNow Studio](https://www.servicenow.com/docs/access?context=sns-app-gen-guidelines&version=zurich&pubname=zurich-application-development&ft:locale=en-US)|
|Analytics generation|[Guidelines and example questions](https://www.servicenow.com/docs/access?context=example-questions-generating-dv&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)|
|Catalog item generation|[Suggestions to describe catalog items](https://www.servicenow.com/docs/access?context=how-to-describe-catalog-item&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)|
|Code generation|[General guidelines for code generation](https://www.servicenow.com/docs/access?context=general-guidelines-code-generation&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)|
|Flow generation|[Exploring flow generation](https://www.servicenow.com/docs/access?context=exploring-flow-generation&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)|
|LLM topic skill for Virtual Agent||
|Now Assist Skill Kit|[General guidelines for Now Assist Skill Kit](../../now-assist-skill-kit/reference/na-skill-kit-guidelines.md)|
|RPA bot generation|[General guidelines for RPA bot generation](https://www.servicenow.com/docs/access?context=rpa-bot-generation&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)|
|Test generation|[Design considerations for prompting](https://www.servicenow.com/docs/access?context=tg-prompt-design-considerations&version=zurich&pubname=zurich-application-development&ft:locale=en-US)|
|UI generation|[General guidelines UI generation](https://www.servicenow.com/docs/access?context=general-guidelines-ui-generation&version=zurich&pubname=zurich-application-development&ft:locale=en-US)|

**Parent Topic:**[Large language models on the ServiceNow AI Platform](../../general/concept/exploring-large-language-models.md)

