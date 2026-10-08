---
title: Data sets for conversation evaluations
description: Test data sets supply the scenarios and expected results that conversation evaluations run on to measure how your assistant performs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/virtual-agent/data-sets-con-eval-ad.html
release: brazil
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2026-10-05"
reading_time_minutes: 19
breadcrumb: [Testing assistant conversations, Test and improve, Build conversations, Virtual Agent, Conversational Interfaces]
---

# Data sets for conversation evaluations

Test data sets supply the scenarios and expected results that conversation evaluations run on to measure how your assistant performs.

## Components of a test data set

A test data set has two parts that work together:

-   A test scenario, which defines what to evaluate the assistant on. It is made up of four fields: initial\_query, scenario\_context, run\_as\_user, and end\_goal.
-   Ground truth \(GT\), which defines the expected output for each test scenario. It captures what a successful response looks like, such as the correct information returned, the right action completed, or the expected asset selected. The evaluation compares the assistant's behavior against the ground truth to produce scores for the conversation success and skill selection accuracy metrics.

The test scenario sets up the test, and the ground truth specifies what good looks like. Building both carefully gives you a reliable, repeatable way to measure how well an assistant performs.

To build your data set from a template, download the sample test set, `template_conv_eval_dataset.xlsx`. When you select a table for an automated evaluation, open the **What evaluation inputs do I need to provide?** help and select **download an Excel file**. The template defines each field and shows the formatting that the evaluation expects. For more information, see [Set up an automated evaluation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/create-auto-evaluation-ad.md).

**Note:** A general guideline is to use a minimum of 500 test scenarios.

Each row in a test data set represents one simulated test scenario for an AI assistant. Together, the rows represent the range of situations that you expect the assistant to handle, from simple lookups to multi-step requests. A row contains the following fields:

-   **initial\_query**

    **Required**: Yes

    **What it does**

    The opening message auto-generated chat sends to start the conversation. This is the first thing the bot sees, so it must reflect how a real user would naturally phrase their request or question. A well-crafted initial query sets up the entire conversation and directly influences whether the bot engages the right skill or flow.

    **Guidance**

    -   Write queries in natural language.
    -   Vary the phrasing across test cases to cover how different users might say the same thing.
    For example:

    ```
    Can I see open incidents assigned to Howard Johnson?
    ```

-   **run\_as\_user**

    **Required**: Yes

    Specifies which user the assistant converses with during the simulation. When set, the conversation runs as that user, so the assistant responds under that user's permissions, roles, and access control lists \(ACLs\). This is useful for checking how the assistant behaves for users with different access levels, because the same query can return different results or actions depending on who is asking.

    **Note:** If you leave this field empty, the conversation falls back to the user who triggered the evaluation, or in some cases to a system default account such as an admin or guest account. Because that fallback account may not have access to the records or knowledge base articles referenced in your scenario, an empty run\_as\_user can cause the assistant to return incomplete or incorrect results that look like assistant failures, but are actually caused by missing access. To get reliable results, set run\_as\_user to an account with the same access as the person your scenario represents.

-   **scenario\_context**

    **Required**: Optional, but include it to help prevent the auto-generated chat from making random selections.

    **What it does**

    Natural language instructions that tell auto-generated chat how to behave throughout the conversation. This can be a single sentence or a detailed set of rules covering how to handle every turn in the dialogue. When omitted, the auto-generated chat behaves as a neutral, cooperative user. It might then make random selections or accept the fallback ticket generation.

    **Guidance**

    -   For Agent and Topic skills, include context about the user's situation so auto-generated chat can provide relevant follow-up inputs. For example, their department, location, or type of request.
    -   This field can be used to test edge cases: what happens if the user provides wrong information, changes their mind.
    -   Start with an intent statement that begins with "The user needs help with". Add the persona and state, such as the user's role, environment, and what the user already has. Add the slot and value pairs that the user provides when or if prompted for more information.
    -   Add an **Important Rules** block \(highly recommended\), with guidance that keeps the simulated user from inventing details such as table names, IDs, or ticket numbers, and that specifies when to end the conversation.

        **Note:** Always include an Important Rules block in the scenario\_context that tells the simulated user not to agree to creating an incident, catalog request, or other ticket if the assistant offers to do so as a fallback. The simulation's default persona is cooperative, so without this rule it can accept ticket-creation offers whenever the assistant can't answer, which can flood your instance with unwanted records.

    For example:

    ```
    The user needs help with finding open incidents assigned to a specific person.
    The user is an IT support agent reviewing a colleague's workload and wants to see the open incidents currently assigned to that person.
    If prompted, the user provides the following details:
    - Assigned to: Howard Johnson
    - Incident state: Open
    Important Rule: If the bot requests that the user create an IT incident or Universal Request because of insufficient information or resources, the user must not proceed. Instead, the user should instruct the bot to cancel the request and take no further action.
    
    ```

    **Template examples by skill**

    **QnA example**

    |Type|Template|Expected behavior|
    |----|--------|-----------------|
    |One turn QnA|The user is seeking information related to their initial query. After receiving the answer, the user thanks the bot and indicates that no further assistance is needed. If the bot offers a ticket, transfer, escalation, or any other follow-up action, the user declines the offer and states that no further assistance is needed.|The auto-generated chat receives the response and declines incident/ticket generation requests.|
    |Multi-turn QnA|The user asks the initial question. After the bot responds, the user asks &lt;follow-up question&gt;. After the bot responds, the user asks &lt;additional question&gt;. After receiving the final answer, the user thanks the bot and indicates that no further assistance is needed. If the bot offers a ticket, transfer, escalation, or any other follow-up action, the user declines the offer and states that no further assistance is needed.|After the initial response, the auto-generated chat asks 2 follow-up questions.|

    **Agent example**

    **Note:** This section can't be generalized for all agents because it depends on the agent's workflow

    For example, consider the following sample workflow for an agent that generates change plans:

    -   The user wants to generate change plans.
    -   The agent evaluates whether the request contains sufficient information.
    -   If sufficient information is available: The agent generates the change plan and asks the user for approval before updating the records.
    -   If sufficient information is not available: The agent asks whether the user would like to proceed using industry general guidelines to fill in the missing details.
    -   If the user agrees, the agent generates the change plan based on those general guidelines and then asks for approval before updating the records.
    The sequence of clarification questions, approvals, and follow-up actions is specific to the agent's workflow and business logic.

    For this agent, you can create the following scenario:

<table id="table_sc_agent_ad"><thead><tr><th>

Type

</th><th>

Template / Example

</th><th>

Expected behavior

</th></tr></thead><tbody><tr><td>

Agent

</td><td>

The user is seeking help to generate change plans for CHG0000. When asked, the user approves the generated change plans. If the bot asks whether the user wants to proceed based on general guidelines, the user replies, 'Yes'.

 Important Rule: If the bot requests that the user create an IT Incident or raise a request &lt;update this part if fallback option has a specific name&gt; because of insufficient information or resources, the user must not proceed. Instead, the user should instruct the bot to cancel the request and take no further action.

</td><td>

The auto-generated chat receives the response and approves the output

</td></tr></tbody>
</table>    **Topic examples**

<table id="table_sc_topic_ad"><thead><tr><th>

Type

</th><th>

Template

</th><th>

Expected behavior

</th></tr></thead><tbody><tr><td>

Topic

</td><td>

The user needs help with &lt;topic action such as booking a meeting room&gt;. When first prompted, the user provides the following details:

 &lt;Itemized specific information is asked by topic such as:&gt;

 - date and time: July 29 at 10:00 AM

 - Host: Abel Tuter

 - Building: A

 Important Rule: If the bot requests that the user create an IT Incident or raise a request &lt;update this part if fallback option has a specific name&gt; because of insufficient information or resources, the user must not proceed. Instead, the user should instruct the bot to cancel the request and take no further action.

</td><td>

The auto-generated chat provides the values when asked.

</td></tr></tbody>
</table>-   **end\_goal**

    **Required**: Optional

    **What it does**

    The terminal condition, the point at which the conversation should be considered complete. Auto-generated chat uses this to determine when to stop, so it does not keep the conversation going unnecessarily. Without an end goal, auto-generated chat relies on natural conversation signals to determine when to stop.

    **Guidance**

    -   For QnA skills, the end goal is typically that the bot has answered the question.
    -   For Agent skills, define the specific outcome that marks success. For example, a ticket has been created and the user has received a confirmation number.
    -   For Topic skills, describe the final state of the guided flow. For example, the user has ordered the food.
    **Template examples by skill**

    |Type|Template|Expected behavior|
    |----|--------|-----------------|
    |Single turn QnA|The conversation ends after the bot's first response, regardless of whether it is a standard response, a fallback response, or any other response type.|The auto-generated chat ends the conversation after the first response.|
    |Multi turn QnA|The conversation ends when the user indicates that no further assistance is needed and the bot acknowledges this.|Auto-generated chat ends the conversation when a condition specified in the scenario context is met. For example, the user thanks the bot and indicates that no further assistance is needed after all steps are completed.|
    |Specific agent|The conversation ends when the bot provides change plans and receives approval from the user.| |
    |Topic|The conversation ends when the user books the meeting room.| |

-   **ground\_truth**

    **Required**: Yes

    **What it does**

    The expected bot output or action used to determine success or failure. What the bot actually said or did is compared against the ground truth and a pass/fail verdict is produced.

    **Guidance**

    -   Focus on intent and outcome rather than exact phrasing, unless exact phrasing is the point of the test.
    -   For Agent skills, the ground truth can describe an action rather than specific bot text. For example, "A Priority 2 incident is created".
    -   Include the key information that must be present. Avoid adding additional details where there is no contribution.
    **Template examples by skill**

<table id="table_gt_ex_ad"><thead><tr><th>

Type

</th><th>

Template

</th><th>

Note

</th></tr></thead><tbody><tr><td>

Single turn QnA

</td><td>

The bot is considered successful if it provides this response: &lt;the simplest form of correct response, only key information to answer the query&gt;

</td><td>

Including unnecessary details makes the ground truth \(GT\) overly strict, causing the judge to penalize responses that omit those details.

</td></tr><tr><td>

Multi turn QnA

</td><td>

The conversation ends when the user indicates that no further assistance is needed and the bot acknowledges this.

</td><td>

Auto-generated chat ends the conversation when a condition specified in the scenario context is met. For example, the user thanks the bot after all steps are completed.

</td></tr><tr><td>

Specific agent

</td><td>

The conversation ends when the bot provides change plans and receives approval from the user.

</td><td>

 

</td></tr><tr><td>

Topic

</td><td>

The bot is considered successful if it correctly collects all required user inputs and successfully addresses or submits &lt;topic for example, the meeting room booking request&gt;. The conversation doesn't have to include all the following details. Ignore the details or values that don't appear in the conversation history. But any details that appear must match these values and processed as follows.

 Request Details and their expected values:

 &lt;Itemized specific information is asked by topic such as:&gt;

 - date and time: July 29 at 10:00 AM

 - Host: Abel Tuter

 - Building: A

</td><td>

 

</td></tr></tbody>
</table>
**Quick reference**

Use this table as a checklist when building each test case in your dataset.

|Field|Required|Key question to answer|
|-----|--------|----------------------|
|initial\_query|Yes|How would a real user phrase this request?|
|scenario\_context|Optional|What situation should auto-generated chat simulate?|
|end\_goal|Optional|What condition would complete \(end\) this conversation?|
|ground\_truth|Yes|What should the bot say or do to pass this test?|

## Load the evaluation data set to your instance

You load your evaluation data set into two related tables: a ground truth table that holds each ideal-behavior record, and an input scenarios table that holds each test scenario and references its matching ground truth. Create both tables first, and then load the data in two phases so that every reference resolves to a real **sys\_id**.

**Note:** The tables can be in any scope, as long as other apps have read access to them.

1.  Create the ground truth table.
    1.  Navigate to **System Definition** &gt; **Tables**.
    2.  Select **New**.
    3.  Enter a **Name** for the table. For example, &lt;your\_GT\_table&gt;.
    4.  Save the table.
    5.  From the **Columns** tab, select **New**.
    6.  Select the following for the new record:
        -   **Type**: JSON
        -   **Column label**: ground\_truth
        -   **Max length**: 2,147,483,647
2.  Create the input scenarios table.
    1.  Create a second table.
    2.  Enter a **Name** for the table. For example, &lt;your\_input\_scenario\_table&gt;.
    3.  Save the table.
    4.  From the **Columns** tab, add the following columns. For each column, select **New** and enter the following values.

        |Type|Column label|Other fields|
        |----|------------|------------|
        |String|initial\_query|**Max length**: 800|
        |String|scenario\_context|**Max length**: 4000|
        |String|end\_goal|**Max length**: 800|
        |Reference|ground\_truth|References the ground truth table from Step 1|
        |Reference|run\_as\_user|References the User \(`sys_user`\) table|

3.  Create the import set.
    1.  Navigate to **System Import Sets** &gt; **Load Data**.
    2.  For the **Import set table** option, select **Create table**.
    3.  Enter a **Label**. For example, &lt;your\_Eval Dataset Import&gt;.
    4.  Select **Source of the import** as **File**.
    5.  Choose your file containing the ground truth data set.
    6.  Select **Sheet number** as **1**.
    7.  Select **Header row** as **1**.
    8.  Select **Submit**.
4.  Create a transform map for the ground truth table.

    **Note:** Start with the ground truth table first.

    1.  Navigate to **System Import Sets** &gt; **Create Transform Map**.
    2.  Enter a **Name** for the transform map. For example, &lt;your\_gt\_transform\_map&gt;.
    3.  For **Source table**, select the import set table that you created in Step 3.
    4.  Select the ground truth table you created in Step 1 as the **Target table**.
    5.  For the **Order** field, choose a lower value from the default value given. For example, the default is 100, and you can change it to 99.
    6.  Save the table.
    7.  After saving, from the Related Links section, select **Auto Map Matching Fields**.
    8.  The **Field Maps** tab is updated with the mapping. Confirm that the source field maps correctly to the target field. For example, `u_ground_truth` maps to `ground_truth`.
    9.  Select the record created under **Source field**. For example, `u_ground_truth`.
    10. Select the **Coalesce** check box, so that each unique value creates one record, and a rerun updates the existing record instead of duplicating it.
    11. Select **Update**.
5.  Create a transform map for the input scenarios table.
    1.  Navigate to **System Import Sets** &gt; **Create Transform Map**.
    2.  Enter a **Name** for the transform map. For example, &lt;your\_input\_scenario\_transform\_map&gt;.
    3.  For **Source table**, select the import set table that you created in Step 3.
    4.  Select the input scenario table you created in Step 2 as the **Target table**.
    5.  For the **Order** field, choose a value higher than the one you set in Step 4. For example, 100.
    6.  After saving, from the Related Links section, select **Auto Map Matching Fields**.
    7.  The **Field Maps** tab is updated with the mapping. Confirm that the source field maps correctly to the target field. For example, `u_ground_truth` maps to `ground_truth`.
    8.  Select `ground_truth` to modify the mapping.
    9.  In the Field Map page, perform the following:
        1.  Select the **Use source script** check box.
        2.  Replace the **Source script** field with the following.

            **Note:** You must replace the **new GlideRecord** value with your correct table name.

            ```
            answer = (function transformEntry(source) { 
                var gtValue = source.u_ground_truth.toString(); 
                var gr = new GlideRecord('sn_skill_builder_demo_assistant_eval_ground_truth'); 
                gr.addQuery('ground_truth', gtValue); 
                gr.query(); 
                if (gr.next()) { 
                    return gr.getUniqueValue(); 
                } 
                ignore = true; // skip rows with no matching ground truth, rather than inserting a blank 
                return ''; 
            })(source);
            ```

        3.  Select **Update** to return to the transform map page.
    10. Select `run_as_user` to modify the mapping.
    11. In the Field Map page, perform the following:
        1.  Select the **Use source script** check box.
        2.  Replace the **Source script** field with the following.

            **Note:** If you have a non-standard user table, replace the **sys\_user** table name with your user table.

            ```
            answer = (function transformEntry(source) { 
                var userName = source.u_run_as_user.toString().trim(); 
                if (!userName) { 
                    return ''; // run_as_user is optional, leave blank when not provided 
                } 
                var gr = new GlideRecord('sys_user'); 
                gr.addQuery('user_name', userName); // switch to 'name' or 'email' to match your CSV 
                gr.query(); 
                if (gr.next()) { 
                    return gr.getUniqueValue(); 
                } 
                ignore = true; // skip rows whose user cannot be matched 
                return ''; 
            })(source); 
            ```

        3.  Select **Update** to return to the transform map page.
    12. In the Transform Map page, select **Update**.
6.  Run the transform maps.
    1.  Navigate to **System Import Sets** &gt; **Run Transform**.
    2.  From the **Import set** list, select your import set from Step 3.
    3.  Under **Selected maps**, add both transform maps that you created: the ground truth map and the input scenarios map.
    4.  Select **Transform**.
7.  Verify the result.

    Open your input scenario table and confirm the following:

    -   The rows are populated with all fields intact.
    -   The ground\_truth reference points to your ground truth table.

Script for ground truth mapping:

**Note:** Use **ground\_truth** if the table is created in global scope and **u\_ground\_truth** if the table is created in scoped app.

```
(function getValue(inputs) { // Example var artifactDatasetGr = new GlideRecord(inputs.getValue("artifact_dataset_table")); artifactDatasetGr.get(inputs.getValue('artifact_dataset')); var gt = artifactDatasetGr.ground_truth.getRefRecord(); return gt.getValue('ground_truth') || ""; })(inputs);
```

\(same for both fields, replace highlighted part with the correct column name, \)

## Data set creation guide

Guidelines for creating aia\_artifact\_dataset records.

Each record drives one auto-generated chat simulation. The auto-generated chat uses the record to impersonate a user and have a conversation with the bot. The result is then compared against the ground truth to determine if the bot succeeded.

Every record must have five columns that are internally consistent:

|Column|Required?|Purpose|
|------|---------|-------|
|**run\_as\_user**|Yes|The ServiceNow user identity that auto-generated chat impersonates. This affects what data the bot retrieves and what actions the user can perform.|
|**initial\_query**|Yes|The opening message the auto-generated chat sends to start the conversation.|
|**scenario\_context**|Optional|Instructions for how the auto-generated chat should behave throughout the conversation. Can be as simple as one sentence or as detailed as a full set of rules that covers all inputs.|
|**end\_goal**|Optional|The terminal condition, when the conversation should be considered complete.|
|**ground\_truth**|Yes|The expected bot output or action used to determine success or failure.|

**Column guidelines**

**run\_as\_user**

Pick a user whose account matches the scenario's data requirements. Use a specific named user when the scenario involves personal records like incidents. The bot looks up data tied to that exact user.

|Column|Bad|Good|
|------|---|----|
|run\_as\_user|Tom John -&gt; for 'List all my open incidents.'|Fred Luddy -&gt; for 'List all my open incidents.'|
|Why|Tom John doesn’t have incidents in the instance. The bot returns nothing, making the test invalid.|Fred Luddy has incidents in the instance. The bot returns real data.|

**initial\_query**

The exact first message auto-generated chat sends. Write it as a natural user would type it.

-   Keep intent clear and unambiguous.
-   Match the query type to the conversation category \(QnA, agentic, small talk, catalog\).

|Column|Bad|Good|
|------|---|----|
|initial\_query|email spam help|What should I do if I receive spam emails from unknown sources?|
|Why|Too vague. The auto-generated chat and the bot may not determine what the user wants.|Natural phrasing with clear intent. The auto-generated chat can simulate this reliably.|

**scenario\_context**

Tells the auto-generated chat exactly how to behave. The level of detail required varies by conversation type. Both versions are acceptable:

-   A one or two sentence description of the user's intent. This is generally good for Q&amp;A type of questions. This version works with topic/catalog type as well, but the auto-generated chat can come up with random or invalid selection inputs.
-   Provide all the required input values the auto-generated chat should give when prompted.

Optionally include an **Important Rules** block to restrict the auto-generated chat's behavior. For example, helping prevent it from taking unintended actions during the conversation, such as not proceeding with ticket generation.

|Column|Acceptable\*|Good|
|------|------------|----|
|scenario\_context|User wants to book a meeting room.|User wants to book a meeting room. The user provides these details when prompted: Location: Pleasanton / Date: Tomorrow 10AM / Host: Abel Tuter / Building: A. If pre-filled differently, update Building to D.|
|Why|\*The auto-generated chat can invent inputs and make random selections, some of these inputs might be invalid.|All inputs are explicit. The auto-generated chat knows exactly what to provide at every step.|

**end\_goal**

A single, observable statement of when the conversation is complete. The auto-generated chat uses this as a clue to decide when to end the conversation.

-   QnA: ends when the bot delivers the correct answer.
-   Agentic or catalog: ends when the request is successfully submitted with correct inputs.

|Column|Bad|Good|
|------|---|----|
|end\_goal|The conversation ends when the user is satisfied.|The conversation ends when the bot provides advice for handling spam emails.|
|Why|Provide the expected outcome from bot, not the user.|Specific and observable. The auto-generated chat can end the conversation when the condition is met.|

**ground\_truth**

The reference output used to score the bot. Must be self-contained.

-   QnA: include the full expected answer text.
-   Topics or Catalog: list all required fields and their final expected values. Or keep it simple, for example, the bot is successful if it submits the XX request.
-   Agent: state that the bot succeeds. For example, the bot is successful if it lists the incidents or a specific list.
-   Never reference specific knowledge base article names or IDs, as they can't be looked up.

|Column|Bad|Good|
|------|---|----|
|ground\_truth|Bot is successful if it answers correctly.|Bot is successful if it says: Don't reply to spam emails; never follow unsubscribe links, but simply delete them.|
|Why|This introduces subjectivity and may lead to incorrect judgments.|Self-contained and specific. The bot's response can be directly compared against this text.|

**Example - QnA**

|Column|Value|
|------|-----|
|**run\_as\_user**|System administrator|
|**initial\_query**|What should I do if I receive spam emails from unknown sources?|
|**scenario\_context**|User wants to know how to handle spam from unknown senders.|
|**end\_goal**|The conversation ends when the bot provides advice for handling spam emails.|
|**ground\_truth**|Bot is successful if it says: Don't reply or follow unsubscribe links. Simply delete the emails.|

**Example - Agent**

|Column|Value|
|------|-----|
|**run\_as\_user**|Fred Luddy|
|**initial\_query**|Can you check the status of my incident INC0000020?|
|**scenario\_context**|User wants status of INC0000020, a replacement iPhone request.|
|**end\_goal**|The conversation ends when the user receives a status update for INC0000020.|
|**ground\_truth**|Bot is successful if it retrieves INC0000020 with: ticket number, description, status, assigned person, last updated time, and recent comments.|

## Sample data set

To build your data set from a template, download the sample test set, `template_conv_eval_dataset.xlsx`. When you select a table for an automated evaluation, open the **What evaluation inputs do I need to provide?** help and select **download an Excel file**. The template defines each field and shows the formatting that the evaluation expects. For more information, see [Set up an automated evaluation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/create-auto-evaluation-ad.md).

**Parent Topic:**[Testing assistant conversations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/evaluations-ad.md)

**Related topics**  


[Set up an automated evaluation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/create-auto-evaluation-ad.md)

