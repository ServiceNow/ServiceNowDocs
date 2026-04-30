---
title: Create a flow with Now Assist
description: Use generative AI to create a flow from text directions.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2024-10-17"
reading_time_minutes: 7
breadcrumb: [Create a flow in Workflow Studio, Building flows, Using Workflow Studio, Workflow Studio, Build workflows]
---

# Create a flow with Now Assist

Use generative AI to create a flow from text directions.

Create a flow with Now Assist 

## Before you begin

-   Roles required:
    -   admin, flow\_designer, or a delegated developer permission
    -   now.assist.creator
-   Turn on the flow generation skill. See [Turn on the flow generation skill](turn-on-the-flow-generation-skill.md).

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  From the Workflow Studio home page, select **New** &gt; **Flow**.

3.  Select the **Build with Now Assist** tab.

4.  Fill in the fields to build your flow.

<table id="table_v2j_snf_p1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Flow name

</td><td>

Name to uniquely identify your flow. The system converts the flow name into an internal name by replacing space characters with underscore characters.

</td></tr><tr><td>

Now Assist directions

</td><td>

Text used by Now Assist flow generation skill to create your flow. Describe the flow trigger and its data first. Then describe all the actions and flow logic in the order you want them in the flow. Include as much detail as possible for the best results.

</td></tr><tr><td>

Try an example

</td><td>

Series of text examples to insert into the Now Assist directions field. Select this option to insert example text in the directions field. Each example illustrates directions that will build a flow outline. Trying an example overwrites any directions text that you previously added. You can use the undo and redo options to revert to your previous directions.

</td></tr><tr><td>

Application

</td><td>

Application scope to create your flow in. Global is the default. The application scope determines what data your flow can access and what data it can share.**Important:** You can’t change the application scope of a flow after you’ve generated a preview for it.

</td></tr></tbody>
</table>    Follow these general guidelines when writing Now Assist directions.

    -   **Always describe the trigger first**

        Describe the flow trigger and its data conditions first. After the trigger, describe the actions and flow logic in the same order that you want them to be in the flow.

    -   **Avoid spelling errors**

        Avoid misspelling the names of actions, flow logic, or tables. Consider using hash tags to avoid making mistakes with table names.

    -   **Be precise and descriptive in your request**

        Make sure that your request is precise and descriptive. Describe the flow trigger, record data, actions, and flow logic in as much detail as you can.

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

<table id="table_ltx_mlf_b1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Protection

</td><td>

Selection to specify if the flow is read-only. You can only select a value when you create the flow in an application scope that you own.

</td></tr><tr><td>

Run as

</td><td>

Option to specify the user that runs the flow. You can select the system user or the user who initiates the session. Select the user who initiates the session option when updates should come from the user who triggered the flow. For example, use this option when you want the incident record comments to come from the user who started the flow. Settings for the Run as option in a flow don't apply to child subflows.

 **Note:** By default, flows run as the user who initiates the session.

 To create a flow that can run with a personal OAuth token, select the user who initiates the session option. If the user who is running the flow has a personal OAuth token, the flow runs with that token. For more information about creating a personal OAuth token, see [OAuth 2.0 credentials](https://www.servicenow.com/docs/access?context=oauth-2-credentials&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

 When flows run as the user who initiates the session, the system limits flow actions by user ACL restrictions. Ensure that security restrictions don't prevent users who trigger the flow from performing flow actions. Flows run by the initiating user also respect user-specific settings such as date/time formats.

 **Note:** Inbound email flows ignore this setting and always run as the user who initiates the session. To test access controls for an inbound email flow, impersonate a typical inbound email user and manually trigger the flow.

</td></tr><tr><td>

Run with roles

</td><td>

Roles that the flow runs with. This option is only available when **Run as** is set to **user who initiates the session**. You can add one or more roles that the flow can use to access data. These roles only apply to running the flow. For example, add the itil role to flows that need to access ITSM data.

</td></tr><tr><td>

Flow Priority Default

</td><td>

Priority level at which you want the system to run this flow by default. Options include:

-   Low
-   Medium \(Default\)
-   High
 To learn about flow priority levels, see [Flow priority](../concept/flow-priority.md).

</td></tr></tbody>
</table>5.  Select the **Try an example** option to insert a valid example of flow directions.

    Each time you select the option, the system inserts a different example of flow directions text. There are three example directions to choose from. Each example direction produces a different type of flow. Selecting Try an example overwrites any directions text that you previously added. You can use the undo and redo options to revert to your previous directions.

6.  Select **Build flow with Now Assist**.

    ![Example Build with Now Assist window with a flow named test flow and directions to build a flow that runs every day at midnight.](../images/example-build-flow-with-now-assist.png)

    Workflow Studio uses your text directions to build a flow outline. If successful, Workflow Studio displays a preview of the flow in the diagramming view. Beneath each node of the flow there is an annotation showing the text directions used to generate the item.

    ![Example flow preview in diagramming view. Each node shows an annotation of the text directions used.](../images/example-flow-preview-with-annotations.png)

7.  If the generated flow preview does not meet your needs, you can update the Now Assist directions, and select **Rebuild flow**.

    Each time you build or rebuild a flow, the operation counts as an assist tracked by your Now Assist subscription. To track your Now Assist usage, see [Monitoring Now Assist usage in Subscription Management](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

8.  If you want to stop creating a flow and return to the Workflow Studio homepage, you can select **Discard flow**.

    **Important:** Workflow Studio does not save flow previews. If you discard a flow, all information about it is lost.

9.  Select **Save and edit flow** to review the flow outline.

    **Note:** Opening a flow does not count as an assist.


## Result

Now Assist creates a flow outline with the name you provided. If the large language model couldn't find a matching action, flow logic, or subflow for your request, it may add one or more placeholder steps instead.

## Create a flow with a scheduled trigger

![Create flow screen with options to build a flow with Now Assist](../images/example-build-with-now-assist-with-preview.png)

You can use these prompt values to create a flow with a scheduled trigger.

-   **Flow name**

    Assign new problems for triage daily

-   **Now Assist directions**

    Create a flow that runs every day at midnight, and then find all the newly created problem records for the past day. Iterate over them. If they are not assigned, update it to assign the problem to level 1 triage group, move the state to "triaged," and then send a notification to the group.


## What to do next

-   Replace any placeholder steps with actual actions or subflows.
-   Configure the inputs of each action, flow logic, and subflow to use appropriate data.
-   Test the flow before activating it.

**Parent Topic:**[Create a flow in Workflow Studio](create-flow.md)

