---
title: Customizing severity levels
description: Assign a severity level to each failure pattern that automated evaluations can detect, so your evaluation results reflect how your organization wants to weigh each type of failure.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/conversational-interfaces/now-assist-in-virtual-agent/customize-severity-levels.html
release: australia
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: concept
last_updated: "2026-10-05"
reading_time_minutes: 4
breadcrumb: [Testing assistant conversations, ServiceNow Otto for Virtual Agent, Conversational Interfaces]
---

# Customizing severity levels

Assign a severity level to each failure pattern that automated evaluations can detect, so your evaluation results reflect how your organization wants to weigh each type of failure.

## Available severity levels

Evaluation results in Assistant Designer classify failed scenarios into failure patterns. Each pattern carries a severity level so you can tell how much impact a failure has on the conversation. From the **Testing** tab, select **Customize severity levels** to open the **Severity levels** page.

\[Omitted image "cust-sev-levels-01.png"\] Alt text: Customize severity levels option on the Testing tab.

The following severity levels are available:

|Severity level|Definition|
|--------------|----------|
|Critical|Task did not complete, or completed with wrong or harmful data.|
|High|Didn't go well, but recoverable. Friction or incompleteness, no lasting harm.|
|Medium|Task still succeeded. This is a polish or quality issue only.|

## Default severity by failure pattern

Each failure pattern that an evaluation can detect has a default severity level, grouped by the evaluation metric it belongs to. You can change the default severity level for any failure pattern to match how your organization wants to weigh it.

A severity level that you set applies across your instance, not to a single evaluation. Every automated evaluation that runs after you save your changes uses the levels shown on the **Severity levels** page.

\[Omitted image "cust-sev-levels-02.png"\] Alt text: Severity levels page showing the default severity for each failure pattern, grouped by metric.

**Conversation success**

|Failure pattern|Description|Default severity|
|---------------|-----------|----------------|
|Access permission errors|The assistant incorrectly informs the user that they lack permission for the request.|Critical|
|Answered unanswerable query|The assistant provided a confident, specific answer to a query it should have flagged as unanswerable or lacking sufficient information.|Critical|
|Incomplete information|The assistant gave a correct but incomplete response, omitting key details or steps specified in the expected information.|Critical|
|Incomplete or incorrect input handling|The assistant failed to recognize valid user input, collect all required fields, or process the correct values before submission.|Critical|
|Incorrect response|The assistant provided information or instructions that were incorrect or contradicted the expected information.|Critical|
|Loop / stuck state|The assistant repeatedly asked for the same input or could not progress past a specific step, preventing task completion.|Critical|
|Other conversation success issues|Unsuccessful conversation that doesn't match the other issue categories.|Critical|
|Premature termination|The assistant ended the conversation without completing the requested task, such as submitting the request, providing the requested information, or performing the requested service action.|Critical|
|Technical or service failure|The assistant encountered a technical error, system error, or service unavailability that prevented any meaningful response or task progress.|Critical|
|Wrong action performed|The assistant performed a different action than expected, such as executing a service request instead of providing information or instructions, or performing the wrong service action.|Critical|

**Conversation fluency**

|Failure pattern|Description|Default severity|
|---------------|-----------|----------------|
|Ambiguous language|The assistant used vague or unclear language that could be misinterpreted.|Critical|
|Contradictory language|The assistant made statements that directly contradict each other within the same response or conflict with established facts from the conversation.|Critical|
|Grammar error|The assistant produced incorrect grammar such as subject-verb disagreement, wrong articles, incorrect prepositions, or inappropriate tense shifts.|High|
|Inappropriate closure|The assistant closed or attempted to close the conversation at a point that is premature, contradictory, or contextually inappropriate.|Critical|
|Internal detail exposure|The assistant exposed its system instructions, tool definitions, or internal reasoning that should not be visible to the user.|Critical|
|Off topic or incoherent response|The assistant introduced irrelevant content or deviated from the logical flow of the conversation thread.|Critical|
|Other fluency issue|Fluency issue that doesn't match the other issue categories.|Critical|
|Overly verbose|The assistant provided a response that is too lengthy or wordy relative to the simplicity of the request.|High|
|Poor formatting|The assistant used formatting unsuitable for the chat medium, such as excessive lists, broken markdown, or overwhelming picker options.|High|
|Response repetition|The assistant repeated words, phrases, or information without a clear conversational purpose.|High|
|Tone mismatch|The assistant was too formal, too casual, or too upbeat for the conversational context.|High|
|Truncated or incomplete response|The assistant provided a response that ended abruptly or was missing key linguistic components needed to convey a complete thought.|Critical|
|Unnatural or robotic phrasing|The assistant used phrasing that is stiff or awkward in a way a native speaker would not use.|High|

**Faithfulness**

|Failure pattern|Description|Default severity|
|---------------|-----------|----------------|
|Cross-document confusion|The assistant mixed up information from different reference documents, attributing details from one context to an unrelated topic.|Critical|
|Fabricated schema structure|The assistant asked for, presented, or processed parameters in a way that contradicts the defined parameter types, choices, or structure in the schema or API contract.|Critical|
|Fabricated skill capability|The assistant provided additional methods, capabilities, channels, catalog items, tools, or skills beyond those explicitly supported.|Critical|
|Failed to use available info|The assistant failed to use relevant information that's explicitly available in the reference documents, tool outputs, or conversation context. This includes omitting important information, incorrectly stating that information is unavailable, prematurely ending the conversation, or asking for information that's already available.|Critical|
|Hallucinated / fabricated information|The assistant presented facts, assumptions, conclusions, implications, or other information that is not supported by the reference documents, tool outputs, or conversation context.|Critical|
|Incorrect contact or reference detail|The assistant provided an incorrect phone number, email address, URL, name, or other specific reference detail that contradicts the source material.|Critical|
|Invented data after a failed lookup|The assistant invented specific data or results when a tool output returned an error, null, or empty response.|Critical|
|Other response faithfulness issue|Faithfulness issue that doesn't match the other issue categories.|Critical|
|Outdated information|The assistant presented information that has been superseded by more recent data available in the conversation history or tool outputs.|Critical|

