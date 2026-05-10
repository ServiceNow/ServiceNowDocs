---
title: Decision Tables
description: Use decision tables to decouple decision logic from your code by creating and maintaining decision rules.
locale: en-US
release: australia
product: Decision Tables
classification: decision-tables
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Builder library, Developing your application, Building applications]
---

# Decision Tables

Use decision tables to decouple decision logic from your code by creating and maintaining decision rules.

**Important:** Try creating decision tables in Workflow Studio instead. Workflow Studio integrates workflow authoring, configuring, and monitoring into a single page experience. For more information, see [Create decision tables in Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/create-decision-table-in-decision-designer.md).

Use decisions tables to help you reach outcomes that depend on multiple factors. In these tables, each factor is a decision input. For example, if you are trying to make a decision about car insurance coverage, your inputs might include the location where the insured person lives, the age and accident history of the insured person, the car make, the car model, and the car year. This logic can save time and present a more organized, readable format than using a script. Decision tables provide a single point where you can create, view, and modify decisions.

To interact with Decision Tables in script, use the [DecisionTableAPI - Scoped, Global](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/DecisionTableAPI.md).

## Components of a decision

-   **Decision Table \[sys\_decision\] records**

    Decision table records represent a single decision. In this record, you specify which table you want to use for your answers. This record also contains related lists where you can create your decision inputs and decisions.

-   **Decision inputs \[sys\_decision\_input\] records**

    Decision input records represent your inputs that are used to obtain answers in a decision. These inputs can include a variety of types, including strings, references, true/false inputs, and dates. Each decision input has a specified input type and can be assigned a default value.

-   **Decision \[sys\_decision\_question\] records**

    Each decision record represents a decision that is based on your inputs. Use the condition builder on the decision record form to create a condition that is based on the inputs for this decision. Then, you can select an answer record for this decision. The answer record can be any record from the table that you have defined in the Decision Table record. You can select the same answer record for more than one decision.

-   **Answer \[sys\_decision\_multi\_result\_element\] records**

    Answer records represent answers that are reached using different decision input values. Answers records can be records on any table, but you need to choose the table when creating your Decision Table record. You could, for example, use the sys\_choice table to use existing choice records. From the example about insurance coverage, you could create a table where each record contains details about the levels of insurance coverage.


-   **[Decision tables in the classic environment](decision-tables-classic-ui.md)**  
In the classic environment, you can develop a table to use for your decision answer records. You then associate an answer record to each decision on your decision table. This answer record is returned when the decision is reached based on your inputs.

**Parent Topic:**[Builder library](../../../build/custom-application/concept/builder-library-table.md)

