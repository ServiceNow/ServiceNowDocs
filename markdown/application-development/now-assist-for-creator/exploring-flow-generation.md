---
title: Exploring flow generation
description: Create multiple step flows and subflows with generative AI. Generate appropriate data pill values for supported flow triggers and action inputs.
locale: en-US
release: australia
product: Now Assist for Creator
classification: now-assist-for-creator
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 12
breadcrumb: [Flow generation, Use generative AI, Now Assist for Creator, Vibe coding and AI app development on the ServiceNow AI Platform, Building applications]
---

# Exploring flow generation

Create multiple step flows and subflows with generative AI. Generate appropriate data pill values for supported flow triggers and action inputs.

Create a flow with Now Assist 

## Activation

The skill Flow generation is installed with the Now Assist for Creator \(sn\_now\_creator\) application. You can install this application from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Benefits

Enable flow generation to gain these benefits.

-   Build a multi-step flow or subflow from a flow description in Workflow Studio. Supported triggers and actions are configured with appropriate data pill values.
-   See the text directions used to generate each item in your flow.
-   Use standard flow design patterns.

## Supported LLMs

You can use Now LLM Service, Now LLM Long Term Stable models \(LTS\), Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all Now Assist skills and AI agents. Use the Configuration Controls in [AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/ai-model-providers.md) to define which options are available, then set the skill-level preferences in the [Now Assist Admin console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/manage-large-language-models.md). For more information, see [Large language models on the ServiceNow AI Platform®](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-large-language-model-now-llm/exploring-large-language-models.md).

## Supported user interfaces

Access flow generation skills from the Workflow Studio user interface.

![Dialog window with options to build a flow with Now Assist](../images/example-input-build-with-now-assist.png "Flow generation from the Workflow Studio user interface")

## Supported trigger types

Flow generation supports a limited number of trigger types. You can use text directions to specify these trigger types.

-   Scheduled triggers
-   Record triggers
    -   Created
    -   Created or Updated
    -   Updated
-   Service Level Agreements triggers
-   Inbound email triggers
-   Service Catalog triggers

## Annotations display directions used

Beginning with the Xanadu Patch 1 release, the flow generation skill displays flow annotations below each item added to the flow. The flow annotations contain the text directions that the flow generation skill used to generate the item. You can use these flow annotations to build better text directions and also receive feedback about how your directions map to specific actions, flow logic, and subflows.

![Example flow preview in diagramming view. Each node shows an annotation of the text directions used.](../images/example-flow-preview-with-annotations.png "Flow preview with flow annotations")

This example illustrates how the flow generation skill mapped specific text directions to flow items.

|Directions|Flow item generated|
|----------|-------------------|
|`runs every day at midnight`|Daily trigger|
|`find all the newly created problem records for the past day`|Look Up Records action|
|`iterate over them`|For Each flow logic|
|`If they are not assigned`|If flow logic|
|`update it to assign the problem to level 1 triage group`|Update Record action|
|`move the state to "triaged,"`|Update Record action|
|`send a notification to the group`|Send Notification action|

## Data pill configuration for supported items

Beginning with the Xanadu Patch 3 release, the flow generation skill generates appropriate data pill values for supported triggers, actions, and flow logic. The flow generation skill updates the flow preview with data pill values as it generates them. While generating a flow preview, the system displays a check mark icon next to each item that contains generated data pill values. You can see the data pill values generated between the name of the flow component and the flow annotations containing your original text directions. The flow preview displays an animated working icon next to items that are waiting for data pill values to be generated. While the flow preview is generating data pill values, the system displays an option to stop generating the flow preview. If you stop generating the flow preview, you must either manually save and edit the flow, or edit your directions to generate another flow preview.

![Flow preview populating the data pill values of each node.](../images/example-filling-out-flow-properties.jpg "Flow preview with data pill configuration")

-   **1. Completed icon**

    The system displays a green check mark icon on the cards of flow components for which it has generated data pill values. These status icons are only visible while the system is generating the flow preview.

-   **2. Generated data pill values**

    The system displays a preview of data pill values in between the flow component name and the text directions used to generate the flow component. The system displays a preview of long data pill values. You can select a flow component to see the full data pill configuration in the properties pane.

-   **3. Working icon**

    The system displays an animated working icon on the current card for which it is generating data pill values. The system displays a static working icon for the flow components that have not yet generated any data pill values. These status icons are only visible while the system is generating the flow preview.

-   **4. Stop generating button**

    The system displays the Stop generating button while it is generating data pill values. You can stop flow generation to either manually save and edit the flow or to update the Now Assist directions used to generate your flow preview.


## Descriptions of flow data

![Flow preview of components showing the title Look Up Problem Records and the also the data pills used in the query filter.](../images/example-flow-generation-natural-language-titles.png)

See a natural language description of the data each component of a flow uses. Understand what data flow triggers, actions, and flow logic blocks use without having to open their configuration details. Where possible, the title of the flow component displays information about the table where data comes from. Otherwise, the flow component displays the data pills it has been configured to use.

## Hash tag support for table name references

Beginning with the Xanadu Patch 3 release, you can refer to a specific table in your Now Assist directions by typing a hash tag character and then typing either the table label or table name. As you type, autocomplete displays tables that match your entry. Add hash tag references to your directions when you want to ensure that flow generation selects the correct table for triggers or record-based actions. Hash tag references are particularly useful to help the LLM distinguish between tables that have similar or even identical labels such as the User \[imp\_user\] and User \[sys\_user\] tables.

![Autocomplete table name suggestions for the Strategic hash tag](../images/example-hash-tags-autocomplete.jpg "Hash tag autocomplete")

![Now Assist directions containing a hash tag link to the Strategic Priority table.](../images/example-hash-tags-autocomplete-02.jpg "Now Assist directions with a hash tag table reference")

-   **1. Hash tag text**

    The system recognizes hash tags as a reference to a table label or table name. You can type either a table label such as Strategic Priority or a table name such as sn\_gf\_strategy.

-   **2. Autocomplete table name suggestions**

    The system displays table name suggestions that match your hash tag text. You can select an autocomplete suggestion to use data from that specific table in your Now Assist directions.

-   **3. Hash tag link to table**

    The system displays underlined link text to the table you selected.


## Retrieval Augmented Generation \(RAG\) support

Flow generation uses Retrieval Augmented Generation \(RAG\) to include the names of common and recently published actions and subflows available on your instance. Workflow Studio updates the list of common and recently published actions and subflows every hour to make them available to flow generation. You can list published actions and subflows by name in your flow generation directions.

## Example prompts

Here are some examples that you can use to create flows and subflows.

-   **Example flow prompt 1: scheduled trigger**

    You can use this prompt to create a flow with a scheduled trigger.

    `Create a flow that runs every day at midnight, and then find all the newly created problem records for the past day. Iterate over them. If they are not assigned, update it to assign the problem to level 1 triage group, move the state to "triaged," and then send a notification to the group.`

-   **Example flow prompt 2: Service Level Agreement \(SLA\) Task trigger**

    You can use this prompt to create a flow with a Service Level Agreement \(SLA\) Task trigger.

    `Create a flow with SLA trigger. Wait for 50% of the SLA, then send a notification. Next, wait for 75% of the SLA then send another notification. After 100% of the SLA is complete, do an if statement to determine if the SLA is breached or was completed.`

-   **Example flow prompt 3: Record trigger**

    You can use this prompt to create a flow with a record trigger.

    `Whenever a change request is created or updated where model is unauthorized demo, do the following in parallel. First, Apply change approval policy. If approvals are approved or skipped, update change request record as approved. If not, updated change request record as rejected. Evaluate the model once again. If rejected, send email. Second, Wait until active is false, disregard change request approvals and evaluate the change model.`

-   **Example subflow prompt 4: Record input**

    You can use this prompt to create a subflow with a record input.

    `Create a subflow that logs the name of the problem input, and then check if the last updated by person is the same as the assigned to. Output the result from the subflow output.`

-   **Example subflow prompt 5: Approval input**

    You can use this prompt to create a subflow for an approval.

    `Create a subflow to create a flow launcher job using the given job config sys id and workload generator parameters. If the job sys id is not empty, assign it as the job exec id subflow output. Subsequently, start the flow launcher for the created job sysid and assign subflow outputs.`

-   **Example subflow prompt 6: Catalog tasks**

    You can use this prompt to create a subflow that creates catalog tasks.

    `Create a subflow that for every user with an assigned laptop it sends an email stating that their operating system has to be updated immediately and sends an SMS with the instructions to do it.`


These examples illustrate using hash tags to refer to specific tables.

-   **Example flow 7: Strategic Priority \[sn\_gf\_strategy\] and Goal \[sn\_gf\_goal\]**

    `Upon creation of a new #Strategic Priority, if the type is key initiative, and the start date is before the end date, check if there is any #Goal under the strategic priority record. If no goal exists, send the owner an email.`

-   **Example 8: Transfer Order \[alm\_transfer\_order\]**

    `Once a #Transfer Order is updated to the stage shipment preparation, check that there is a value in the to stockroom field. If it is not empty, create a new transfer order line and link it to the triggering transfer order record.`

-   **Example 9: Assessment Metric type \[asmt\_metric\_type\]**

    `Everyday at 7pm, check if there are new #Assessment Metrics Type records that are live feed. For each of them, if the pagination setting is category, then add the assessor role to the assessment manager user.`

-   **Example 10: Test Suite \[sys\_atf\_test\_suite\] and Test \[sys\_atf\_test\]**

    `When a new #Test Suite record is created or updated, check if there are any child #Test records within it. If there are none, then set the Active field to false.`


## Placeholder steps

Flow generation inserts a placeholder step when it can’t match part of your request to an available action or subflow. Placeholder steps don't perform any operations. They’re empty steps that only display an annotation. Flow authors can use the placeholder text to select an appropriate replacement action or subflow.

**Important:** You can't activate a flow that contains placeholder steps. You must either delete or replace each placeholder step with an action or subflow.

## General guidelines

Follow these general guidelines when writing Now Assist directions.

-   **Always describe the trigger first**

    Describe the flow trigger and its data conditions first. After the trigger, describe the actions and flow logic in the same order that you want them to be in the flow.

-   **Avoid spelling errors**

    Avoid misspelling the names of actions, flow logic, or tables. Consider using hash tags to avoid making mistakes with table names.

-   **Be precise and descriptive in your request**

    Make sure that your request is precise and descriptive. Describe the flow trigger, record data, actions, and flow logic in as much detail as you can. If you attach an image, make sure to attach a clear, high quality image of the process.

-   **Be succinct and direct in your request**

    Start by specifying whether you want to generate a flow or a subflow. For example, use the phrase, "`Create a flow that`" to generate a flow. Describe each step the flow in order.

-   **Refer to actions, flow logic, and tables by name**

    Use action, flow logic, and table names as part of your directions. The closer your directions are to the actual names, the easier it is for the LLM to recognize them. For example, use the text `for each` or `do the following in parallel` to refer to those specific flow logic options. For table names, consider using hash tags.

-   **Review the generated flow outline and input values**

    Review each action, flow logic, and subflow in the generated flow outline. Review the generated inputs values to confirm that they contain relevant data references.

-   **Use hash tags to refer to data in a specific table**

    Use a hash tag to select a specific table name. Hash tags are particularly useful to distinguish between tables that have identical or similar display names such as the User \[sys\_user\] and User \[imp\_user\] tables.

-   **Use numbers to distinguish the branches of do the following in parallel flow logic**

    Add a number to each parallel branch. For example, the directions, "`When a P1 incident is created, do the following in parallel: 1. Log its short description and 2. Look up the user assigned to it and send an email`," makes it clear that there are two branches.

-   **Use quotation marks to set exact values**

    Enclose exact data values in quotations marks to help the LLM distinguish between operation names and data values. For example, the directions, "`Log the value, 'incident reopened'`" make it clear that the text "incident reopened" is a data value.


## AI limitations

This application uses artificial intelligence \(AI\) and machine learning, which are rapidly evolving fields of study that generate predictions based on patterns in data. As a result, this application may not always produce accurate, complete, or appropriate information. Furthermore, there is no guarantee that this application has been fully trained or tested for your use case. To mitigate these issues, it is your responsibility to test and evaluate your use of this application for accuracy, harm, and appropriateness for your use case, employ human oversight of output, and refrain from relying solely on AI-generated outputs for decision-making purposes. This is especially important if you choose to deploy this application in areas with consequential impacts such as healthcare, finance, legal, employment, security, or infrastructure. You agree to abide by [ServiceNow’s AI Acceptable Use Policy](https://www.servicenow.com/ai-acceptable-use-policy.html), which may be updated by ServiceNow.

**Parent Topic:**[Flow generation](../reference/flow-generation-landing.md)

