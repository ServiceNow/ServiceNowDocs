---
title: General guidelines for Workflow Studio flows, subflows, and actions
description: Create, run, troubleshoot, and monitor your Workflow Studio components more effectively. Use these guidelines to optimize the performance of your Workflow Studio components.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 34
breadcrumb: [Flows, subflows, and actions reference, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# General guidelines for Workflow Studio flows, subflows, and actions

Create, run, troubleshoot, and monitor your Workflow Studio components more effectively. Use these guidelines to optimize the performance of your Workflow Studio components.

## Overview of Workflow Studio

Integrate workflow authoring, configuring, and monitoring into a single page experience. Consolidate playbooks, flows, actions, decision tables, and integrations into one design environment.

## Application development

When designing an action or a flow, use these general guidelines.

Use standard ServiceNow AI Platform application development capabilities to create, manage, protect, and deploy Workflow Studio content. Flow and action designers typically perform the following application development tasks:

-   Create a custom application to store flows and actions.
-   Set application permissions to share or restrict access to application data.
-   Grant application developers access to Workflow Studio.
-   Publish custom applications to the application repository to deploy flows and actions on other instances.

## Flows

Flows should be short, modular, reusable collections of work. If they take more than an hour to execute, they’re probably too long and can be more efficient.

Any general guidelines that apply to flows also apply to [subflows](design-considerations-consolidated.md#subflows-design-considerations).

-   **Prevent conflicting or duplicate business logic**

    Automations can be created with Flow Designer, business rules, workflows, and Integration Hub. Before you start using Workflow Studio , make sure you understand how existing ServiceNow AI Platform automations work. Deactivate automations before replacing them with Workflow Studio flows and actions. See the [Architecture Overview](../concept/flow-designer-arch-overview.md) to learn how Workflow Studio works within the ServiceNow AI Platform.

    Review [Flows](../concept/flows.md), [Sub-flows](../concept/subflows.md), and [Actions](../concept/actions.md) documentation, if necessary.

-   **Determine whether your flow needs a trigger or variable input**

    Flows always run when their trigger conditions are met, and triggers always provide the same data as input for flows. If you need variable input to initiate a flow instead, create a [subflow](design-considerations-consolidated.md#subflows-design-considerations).

-   **Reuse business logic**

    Create a set of reusable operations as a subflow that can then be used in multiple flows.

-   **Grant flow roles to access role-protected data and preserve user information**

    Flow roles help keep permissions for your flows simple. Use flow roles to preserve user information and grant access to data, instead of running a flow as the system user. Adding flow roles also gives access to additional data that a user-initiated flow does not usually have. The roles granted only apply to the flow. They do not apply to the user who initiated the flow.

-   **Use flow logic or a schedule-based trigger to control flow timing**

    Flow logic or schedule-based triggers help to optimize the performance of your flows. Do not use the gs.sleep\(\) method to wait within a flow. The gs.sleep\(\) method prevents the thread from performing other work. To run a flow at a specific time, use a schedule-based trigger. To pause a flow for a specific duration, use the [Wait for a duration](../concept/flow-logic-wait-for-a-duration.md) or [wait for condition](wait-for-condition-flow-designer.md) flow logic.

-   **Avoid dependencies**

    Parallel branches that depend on each other stall a flow when a branch has to wait for output from another branch. Instead of creating parallel branches within a flow, call a subflow and return the results to the main flow.

-   **Scope loop counters**

    Script loops don't have a maximum number of iterations, so loops execute infinitely when there is not a valid exit condition.

    To make sure that there is a valid exit condition, scope loop counters in inline scripts or in script steps within an action. Add `var` to `for (i=0; i< length; i++)` :`for (var i=0; i< length; i++)`

-   **Limit For Each and Do Until loops to 1000 iterations**

    Iterations with 1000 or more loops can lead to memory issues from having to store execution details and context records.

    -   Set max records on Look Up Records.
    -   Avoid changing property sn\_flow\_designer.max\_iterations, which defaults to 1000.
    -   For nested loops, each loop has its own maximum number of iterations.
    -   For large amounts of data processing, consider batching into smaller batches.
    -   For bulk imports, consider [concurrent imports](https://www.servicenow.com/docs/access?context=concurrent-imports&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).
-   **Use QuickAPI for faster executions \(business rule alternative\)**
    -   [QuickAPI](https://www.servicenow.com/docs/access?context=ScriptableFlowRunnerScopedAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US) executions are much faster, but there is less debugging capability.
    -   Foreground QuickAPI executions run in the user session as the user who called the flow.
    -   Background QuickAPI executions run in a background thread and are run in the ‘system’ user session.
-   **Use Do Until loops instead of calling flows from themselves**

    Direct recursion where a flow calls itself is not allowed and errors out. Indirect recursion where flow A calls flow B, which calls flow A is allowed up to three times. Instead of calling a flow recursively, use the Do Until flow logic to continue working on records until a certain condition is met.

-   **Execute flows in the background**

    Executing flows in the background allows UI threads to be released rather than pausing the user session until the flow execution completes. By default, flows run asynchronously in the background. Running flows in the background allows users to continue working in the UI while the flow runs.

-   **Avoid flow logic that waits after collecting a large output**

    Using a large payload immediately after it is retrieved can help prevent memory issues. Rather than store a large payload in memory, add actions to process the payload. The sooner you process a retrieved payload, the sooner the system can free up memory to process other actions.

-   **Minimize switching between environments**

    Constantly switching back and forth between instance and MID Server steps in a flow can lead to delays in processing. To minimize the risk of delays, limit switching between instance and MID to only one time.

-   **Include sys\_complex\_object records generated by the flow in update sets**

    Missing [complex data](../concept/complex-data.md) schemas can cause execution issues. Make sure you include sys\_complex\_object records generated by the flow in update sets. Rather than manually build update sets, consider transferring flows from one instance to another by using the application repository.

-   **Call flows from a script when you need a custom trigger**

    If none of the existing triggers meet your business needs, you can create a script to start a flow when its custom trigger conditions are met. Rather than creating a flow with an unneeded trigger, consider instead creating a subflow, which does not have a trigger. Use your script to provide the necessary subflow inputs only when your script conditions are met. Calling a subflow rather than a flow avoids the possibility of the flow trigger conditions being met and running the flow unexpectedly.

-   **Avoid deploying newer release flows to instances on older releases**

    Workflow Studio does not support deploying newer release flows to instances running on earlier releases.

    **Danger**

    The flow data model can change between releases, which can prevent newer flows from running or produce unexpected results when running on earlier release instances. Upgrade your instances to be on the same release versions before deploying them.

-   **Turn flow reporting off in production**

    Minimize the amount of memory required to run flows by disabling [Flow reporting](../task/enable-flow-reporting.md#). Flow reporting stores configuration and runtime information for the Execution Details page. These reports are good for troubleshooting, but requires a large amount of data to be retained both in memory and in the database. By default, flow reporting is disabled, and the system only generates execution details when you manually test a flow or action. Instead you can use log files, which are still available when reporting is turned off.

-   **Reduce the amount of memory consumed in flows with nested looping**

    When reporting is activated, set com.snc.process\_flow.reporting.iteration.lastn to a value of "1" to reduce the amounts of the amounts of memory that previous loop iterations consume. The more iterations you report on, the more memory is required.


## Subflows

General guidelines that apply to [flows](../concept/flows.md) also apply to subflows.

Reasons to use a subflow instead of a flow include the following:

-   **Reuse business logic**

    Create a set of reusable operations as a subflow that can then be used in multiple flows.

-   **Reuse business logic**

    Create a set of reusable operations as a subflow that can then be used in multiple flows.

-   **Configure different input values for each call**

    Configure a subflow's input values differently each time you call it. For example, design a subflow to accept different record types as an input run. Reuse this generic record subflow instead of writing a specific flow for each record type.

-   **Improve performance and readability of large flows**

    Use subflows when a flow exceeds 25 actions. 50 is the maximum number of actions specified by the sn\_flow\_designer.max\_actions system property, but limit a flow to 25 actions for the best performance.

-   **Pass inputs and outputs with subflows**

    Call subflows if you want to pass inputs and outputs. Use subflows if you want to specify the inputs available to a subflow when it starts, or if you want to specify the outputs available to the parent flow after a subflow ends.

-   **Trigger multiple flows on a single event vs using parallel subflows**
    -   Use parallel subflows if there are interrelated outputs or some action must be taken when all are available. If not, then it’s simpler to trigger multiple flows.
    -   To configure parallel subflows, launch each subflow without a wait and then use wait for condition to wait for each subflow to be terminal \(complete, error, canceled\)
-   **Use dynamic flows if you have multiple subflows with similar functionality**

    Dynamic flows let you compartmentalize your processes by applying a template to handle the inputs of multiple similar subflows. Compartmentalization lets you distinguish between subflows that perform similar functions, such as subflows for [IntegrationHub](https://www.servicenow.com/docs/access?context=integrationhub&version=australia&pubname=australia-integrate-applications&ft:locale=en-US) spokes.

-   **Avoid the 10-item limit in the error-handling-process**

    Rather than force your error-handling-process to fit within a 10-item limit, call subflows, which can contain many more items. You can also use the subflow outputs to trigger automation in other flows.

-   **Take corrective actions**

    Rather than recreate the same sequence of actions in multiple flows, create reusable subflows to correct errors to your record data. When a flow error leaves your record data in an undesired state, use subflows to correct these records. You can use the error handler to identify such record data as a subflow output.


## Triggers

Follow these general guidelines when creating record triggers.

-   **Determine whether your flow needs a trigger or variable input**

    Flows always run when their trigger conditions are met. Triggers always provide the same data as input for flows. If you need variable input to initiate a flow instead, create a [subflow](design-considerations-consolidated.md#subflows-design-considerations).

-   **Add conditions to specify what record values start your flow**

    Starting a flow only when needed consumes fewer system resources than starting a flow, pausing it, and waiting to resume the flow until a specific record condition applies. Instead of creating a flow that starts with a Wait for condition action, redesign the flow to include the wait condition as part of the record trigger.

-   **Create unique conditions for record triggers on the same table**

    To prevent flows from overwriting each other, create unique conditions for each flow running on the same table. If multiple flows on the same table the same filter, there is no way to know the order in which the flows run. Using conditions also helps to optimize flow performance by returning a more precise, smaller set of records.

-   **Ignore records added or updated by import and update sets**

    Record triggers ignore records added or updated by applying an update set or importing an XML file. These operations apply to the entire application or table rather than an individual record.

-   **Replace record triggers on Service Catalog tables with Service Catalog application triggers**

    Flow Designer no longer displays Service Catalog tables as options for record triggers. Instead, create flows that use the Service Catalog application trigger type.


## Wait conditions

Follow these general guidelines when creating flows that wait for a condition.

-   **Use record triggers instead of wait conditions to start flows**

    If you only want a flow to run when certain record conditions are met, create a flow with a record trigger instead of starting and pausing a flow. A waiting flow consumes more system resources than a flow trigger.

-   **Cancel flows whose resume conditions can never occur**

    Prevent your flows from waiting indefinitely by specifying flow stop conditions with [End Flow flow logic](../concept/flow-logic-end-action.md). To free up system resources, you can also cancel any flow whose resume conditions can never be met. For example, cancel flows waiting for incident record updates where the related incident is closed.

-   **Restrict wait conditions to fields present on the current table**

    The Wait For Condition action can only monitor changes to the fields of the table to which the record belongs. The action cannot detect changes to fields in related records or catalog variables. For example, if an action waits for changes to an Incident record, then it cannot detect changes to a related record such as a catalog item or change task record. Avoid building wait conditions that dot-walk to another record as these fields actually belong to the related record. Avoid building wait conditions that rely on catalog variables.


## Flows or subflows with stages

Follow these general guidelines when creating flows or subflows with stages.

-   **Avoid defining stages that depend on a For Each flow logic**

    Flow Designer prevents you from adding stages within a **For Each** block. You can only add stages before or after a **For Each** block.

-   **Avoid creating stages for the same records in different flows or subflows**

    A stage field always displays the stage information provided by the last flow or subflow to run on a table's record. If multiple flows or subflows run on the same records, then the stages defined in one flow or subflow can in theory overwrite the stages from another flow or subflow. To avoid multiple flows or subflows overwriting each other's stages, define unique trigger or start conditions for each flow or subflow.

-   **Avoid updating stage fields from outside a flow or subflow**

    If you manage stages with a flow or subflow, avoid directly updating record stage fields from outside the flow or subflow. Manually updating the value of a stage field may produce unexpected or undesired results.

-   **Ensure that each flow on a table has unique trigger conditions**

    Adding unique trigger conditions to each flow ensures the flows only run under those conditions and prevents the stages from one flow overwriting the stages of another flow. Specifying unique trigger conditions makes it easier to troubleshoot flows by limiting the number of flow executions that can produce record changes.

-   **Use error stages to communicate with the user**

    The flow error state does not affect flow execution. A flow continues running even if it reaches an error stage. Use a conditional flow logic block to set the error stage and communicate to the user that the state of the current stage is Error. For example, if an approval is not approved within the required limit, you may want to communicate an error to the user.

-   **Use the error stage to stop processing a flow**

    Use a conditional flow logic block to identify when a flow enters the error stage. Use the flow logic to stop processing the flow or take some kind of remediation action. For example, you may want to change the record state or assignment when a flow reaches an error state.


## Do the following in parallel flow logic

-   **Avoid creating data dependencies between paths**

    Since a flow can run paths in any order, avoid creating data dependencies between separate paths. For example, do not have one path that creates a record and another path that updates the same record. The update record path may run before the create record path.

-   **Do not share data between paths**

    Workflow Studio prevents you from dragging data pills between paths because the system cannot determine which path will finish first to supply the output value.


## Dynamic flows flow logic

-   **Use dynamic flows if you have multiple subflows with similar functionality**

    Dynamic flows let you compartmentalize your processes by applying a template to handle the inputs of multiple similar subflows. Compartmentalization lets you distinguish between subflows that perform similar functions, such as subflows for [IntegrationHub](https://www.servicenow.com/docs/access?context=integrationhub&version=australia&pubname=australia-integrate-applications&ft:locale=en-US) spokes.

-   **Ensure dynamically called subflow inputs match template flow inputs**

    The system throws an error and the main flow can't run properly when the inputs of a dynamic flow and flow template don't match.

-   **Use the correct context when getting flow outputs**

    A context record uniquely identifies the flow run. If you run a dynamic flow multiple times, there are multiple context records to choose from. When you use dynamic flow multiple times within a flow, make sure to pick the right context record from the right run each time you get flow outputs.


## Password2 data pills

Follow these general guidelines when designing flows containing Password \(2 Way Encrypted\) data.

-   **Assign values using existing Password \(2 Way Encrypted\) data pills.**

    You can only assign a value to a password2 variable by selecting an existing password2 data pill. Selecting values from other field types is not supported. Workflow Studio presents a warning message when invalid data pill types are selected.

    ![The warning message displayed when dragging a non-password2 data pill onto a password2 field.](../images/password2-field-warning.ong.png)

    **Note:** You cannot manually enter Password \(2 Way Encrypted\) values.

-   **Use Password \(2 Way Encrypted\) variables only for valid field types**

    Workflow Studio prevents selecting Password2 data pills as the value for invalid field types. The system presents a warning message when the field is an incompatible type.

    ![The warning shown when dragging a password2 field to a disallowed field.](../images/password2-field-warning2.png)

    Workflow Studio only allows Password2 data pills to be dragged into the following field types:

    -   Email body fields
    -   HTML fields
    -   Password 2 Fields
    -   PowerShell Input Variables
    -   REST fields
        -   Variables
        -   REST payload body
        -   Query parameters
        -   Headers
        -   REST multi-part form values
        -   Form URL-encoded values
    -   SOAP fields
        -   Headers
        -   Envelope
    **Note:** you cannot use Password \(2 Way Encrypted\) variables as conditions

    Flow Designer performs a validation check when a user saves, publishes, or tests actions and flows. This check shows that an alert for any data pills dropped in restricted field types and prevents the action or flow from executing. Update the action or flow to remove the invalid data pill and then retry the action.

-   **Set up encryption modules for decryption**

    Only users with a valid encryption module access can decrypt and view the contents of password2 variables. To specify the encryption algorithm and which roles can access encrypted data, see [Password2 encryption with KMF](https://www.servicenow.com/docs/access?context=password-2way-encrypted-fields&version=australia&pubname=australia-platform-security&ft:locale=en-US) .


## SLA Percentage Timer actions

Follow these general guidelines when creating flows that contain Service Level Agreement \(SLA\) Percentage Timer actions.

-   **Add SLA Percentage Timer actions only to flows with an SLA Task trigger**

    An SLA Percentage Timer action can only run when the flow starts from an SLA Task trigger. You cannot activate a subflow containing an SLA Percentage Timer action.

-   **Create conditional flow logic for expected Status values**

    Use the value of the **Status** field as a condition for flow logic. Build flow logic for expected **Status** values such as **Completed**, **Repair**, and **Skipped**. For example, add an **If** flow logic block to send a notification when the SLA Percentage Timer has a status of **Completed**.

-   **Assign each SLA Percentage Timer action a unique cumulative Wait for percentage value**

    Each SLA Percentage Timer action computes its own Scheduled End Date/Time using its Wait for percentage value. If you create multiple SLA Percentage Timer actions, give each action its own unique cumulative Wait for percentage value. For example, create three separate actions with different percentage complete values such as 25%, 50%, and 75% complete. Setting all three actions to the same percentage complete value such as 25% causes the timers to complete at the same time.

-   **Copy existing flows to make customizations**

    Reduce development time by copying the default SLA flows and customizing the copies with your own logic. Select a customized flow to run from the SLA definition. See [Create an SLA definition](https://www.servicenow.com/docs/access?context=t_CreateAnSLADefinition&version=australia&pubname=australia-it-service-management&ft:locale=en-US) .


## Dynamic inputs

-   **Consider dynamic inputs for third-party integrations**

    Dynamic inputs let you create flows that fetch data dynamically from external sources. In third-party integrations, dynamic inputs can provide data values that pertain to a particular endpoint. For more information on setting up third-party integrations with Workflow Studio, see [IntegrationHub](https://www.servicenow.com/docs/access?context=integrationhub&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

-   **Be aware of the time required to retrieve large amounts of data**

    By default, dynamic inputs have up to 300 seconds to gather data before they time out. If your data gathering action needs more time to gather data, set the **sn\_flow\_designer.sync\_action\_execution\_timeout\_in\_seconds** system property to a higher value. However, don't use long timeout values for interactive flows where an end user must enter or select a value.

-   **Be aware of scripting errors**

    Because all data gathering actions use a script step, potential errors could occur from scripting. When using scripts to output JSON variables for your dynamic inputs, you may encounter errors that prevent inputs from receiving the JSON values they need. When a dynamic input scripting error occurs, the following warning message may appear.

    ![Dynamic action error message](../images/warning-dynamic-action-error.png "Message displayed for scripting error")

-   **Limit dynamic inputs type inputs to 40 input values**

    A dynamic inputs type input can only render a certain number of inputs before the JSON object becomes to too big to store in memory. Limiting your dynamic inputs to 40 input values minimizes the chances that you will run out of memory and experience unexpected behaviors such as rendering errors or data truncation.

-   **Limit JSON output to 5000 array items for dynamic templates and dynamic choices**

    Dynamic choice and dynamic template inputs can only display up to 5000 array items. A dynamic choice can only display up to 5000 choice list options, and a dynamic template can only display up to 5000 field template values. If your data gathering action collects data for a dynamic template or a dynamic choice, restrict the maximum number of array items it returns to 5000. The 5000 array items limit prevents the instance from having performance issues when rendering the choices or field values.


## Dynamic outputs

-   **Use dynamic outputs for third-party integrations**

    Use dynamic outputs to introspect and fetch data from external systems during the flow design. For example, you can specify service endpoints or call actions that interact with specific endpoint APIs. For more information on setting up third-party integrations with Workflow Studio, see [IntegrationHub](https://www.servicenow.com/docs/access?context=integrationhub&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

-   **Note the time that is required to retrieve large amounts of data**

    By default, dynamic outputs have up to 300 seconds to gather data before the system stops them. If your data gathering action needs more time to gather data, set the **sn\_flow\_designer.sync\_action\_execution\_timeout\_in\_seconds** system property to a greater value. Avoid long timeout values for interactive flows where an end user is expecting to enter or select a value.

-   **Be aware of scripting errors**

    Because all data gathering actions use a script step, potential errors could occur from scripting. Review any scripts that are used to output JSON variables because script errors may prevent the outputs from receiving the JSON values that they need. When a dynamic output scripting error occurs, the following warning message may appear.

    ![Dynamic action error message](../images/warning-dynamic-action-error.png "Message that is displayed for scripting error")


## List.\[Table\] data

-   **Add a reference qualifier to filter list records**

    Filter the records that the list variable displays as valid options by adding a reference qualifier. The reference qualifier acts as a required list filter and causes the list variable to display only records that match the reference qualifier conditions. For example, to only displays active incident records add the reference qualifier condition **\[Active\]\[is\]\[true\]**.

-   **Avoid selecting default records for actions intended for ServiceNow Store**

    Avoid selecting default records for a list unless you know that all instances have access to the selected records. Spoke developers typically do not have access to the data of the customers who install their custom action. If you want to publish a custom action on the ServiceNow Store, you may need to provide default records as demo data.

-   **Use List variables in For Each flow logic**

    You can use a List variable to specify the records to process within For Each flow logic. The For Each flow logic ignores any non-record sys\_id present in the data. For example, if the List variable contains an email address, the flow logic ignores it.


## Approval rules

-   **Provide a default value**

    Create or select an approval rule as a default value.


## Transform functions

-   **Apply transform functions to valid types of data pills for the input**

    Be sure to check the type of data pill for the input before applying a transform function. Applying a transform function to an invalid data pill type results in the system skipping the transform. An error also occurs if transform functions produce results that the system cannot parse. For example, when transforming a string into a date, the system throws an error if the transform does not produce a valid date.

-   **Confirm applied transform functions for multiple inputs with the same data pill**

    A transform function creates a new value at runtime for a specific input, and does not change the original data pill. If you use the same data pill across multiple actions or steps, transform functions must therefore be applied to each individual input.

-   **View final transformed values in the flow execution details**

    Only the final transformed value, and not the value for each applied transform, appears in the [flow execution details](../concept/flow-execution-details.md).

-   **Test transform functions to verify they produce expected results**

    Make sure that your transform functions produce the expected runtime values for the data pills. For more information, see [Test a flow](../task/flow-test.md) and [Test an action](../task/test-action.md).


## Inline scripts

Follow these general guidelines to create reusable and maintainable inline scripts.

-   **Write inline script for small non-reusable logic**

    Use inline script format or modify the data for specific inputs and use cases. For reusable logic, create an action or subflow instead.

-   **Review available transform functions**

    Workflow Studio provides a list of standard transform functions for data conversions and formatting operations. Rather than write and maintain a custom script solution, select an existing transform function if one is available.

-   **Call script includes from inline script**

    Call a script include from your inline script to reduce the amount of code you write and also to maintain common code in a single location. Use the class constructor to call your script include. For more information about creating a script include, see [Script includes](https://www.servicenow.com/docs/access?context=c_ScriptIncludes&version=australia&pubname=australia-api-reference&ft:locale=en-US).

    ```
    var si = new MyScriptInclude();
    si.functionOne();
    ```

-   **Create custom actions or subflows for reusable code rather than inline script**

    Create custom actions or subflows for reusable or complex data logic such as changing the data type of source data. You may also want to provide custom actions or subflows for flow designers who are not comfortable with code.

-   **Avoid duplicating action and flow functionality**

    Avoid writing inline script that duplicates action and flow functionality. For example, rather than write inline script to perform record operations, use the create and update record baseline actions.

-   **Avoid data type changes**

    Avoid runtime errors by verifying that your inline script provides information in the same data type as the input or output expects.

-   **Create variables by declaring them with the var keyword**

    Use the `var` keyword to declare variables so that they remain within the proper JavaScript scope. When you create a variable by assigning it a value, JavaScript may attach it to the global object, which can result in variable values persisting outside of the local scope and causing errors.

-   **Process records outputs with For Each flow logic and the flow data object**

    Inline script can only access the **records** output of a Look Up Records action from For Each flow logic. Add a Look Up Records action to the flow to generate the records output. Add a For Each flow logic to the flow to process each record in the records output. Create an inline script reference to the For Each flow logic using the fd\_data and item objects. For example, this reference assumes that the For Each flow logic is the second item in your flow outline `fd_data._2__for_each.item`.

-   **Use type ahead suggestions to generate references to flow and action data.**

    Create references to flow and action data using the fd\_data object. The script editor displays type ahead suggestions for existing flow and action data when you type `fd_data`. Select a suggestion to build references to flow and action data.

    **Note:** Refer to record data in a For Each flow logic using the **item** object.

-   **Scope loop counters**

    Script loops don't have a maximum number of iterations, so loops execute infinitely when there is not a valid exit condition.

    To make sure that there is a valid exit condition, use scope loop counters in inline scripts or in script steps within an action. Add `var` to`for (i=0; i< length; i++)` and get `for (var i=0; i< length; i++)`


## Complex data

Follow these general guidelines to create reusable and maintainable data structures.

-   **Minimize the number of child levels in the hierarchy**

    The more child levels a data structure has, the more difficult it is to view and select a data variable from the hierarchy. While you can build data structures with any number of child levels, it becomes difficult to navigate and understand data structures with more than seven child levels. For the best user experience, avoid creating data structures that have so many child levels that you must scroll horizontally to see and populate them.

-   **Create a separate object for each type of record data**

    Most Workflow Studio data is record data whether it is from an instance or an external system. This design method ensures that you know what the object contains and where the data came from.

-   **Recreate record data structures**

    When building objects that receive or transmit record data, review the database dictionary entries for these records and create matching object data structures. For example, suppose that you want an object to contain data from Incident and Configuration Item tables. You might create a string element for the **Short description** field in the Incident table, and an array of strings element for the **Class** field in the Configuration Item table.

-   **Create objects to combine different types of records**

    If you need information from multiple types of records, create an object that contains all the information you need. You can then use the object to format or parse data in Workflow Studio.


## Scripting with complex data

Keep these general guidelines in mind when scripting with complex data.

-   **Use string inputs to convert complex data into a JSON string**

    When you map complex data to a string input, Workflow Studio automatically converts it into a JSON string. Instead of writing a script, you can add a string input to a REST step and map it to complex data from a prior action or step.

-   **Save your objects as templates**

    Save your objects as templates so you can reuse them in other actions, flows, and Script steps.

-   **Create script input variables to access prior data**

    Create a script input variable for any data you want to access from the action input or a prior step. Map the script input variable to the input or step data pill. For example, map the script input variable to a list of user records you looked up in a prior step.

-   **Create a script output variable to store complex data**

    Create a script output variable to store any complex data your script creates. The script output variables must match the values defined in the script. For example, create a contacts array of objects to store multiple contact objects. Save the contact object as a template so you can reuse it.

-   **Map the action output to the script output variable**

    When you want a custom action to output complex data, add an action output and map it to the data pill for your Script step output variable. For example, create a contacts array and load the contact object template you saved earlier. Map the action output to the contacts array produced by your Script step.


## Flow Designer and domain separation

Follow these general guidelines when using domain separation with Workflow Studio.

-   **Ensure that tenant flows, actions, and subflows are run properly for domains**

    Since tenants cannot override Workflow Studio content, a service provider \(SP\) administrator from the TOP domain must author and manage them to ensure they run properly for domains. While you can create domain-specific flows, users working from domains higher in the hierarchy may trigger multiple child domain flows. For example, a user working in the TOP domain can trigger flows in child domains such as ACME and INITECH.

    **Note:** Flow authors can see only Workflow Studio content available from their current domain and any parent domains in the hierarchy. Workflow Studio does not display content visible from Contains domains.

-   **Provide a unique name for each flow, action, and subflow**

    Since all domains share Workflow Studio content, have an SP administrator in the TOP domain uniquely name each flow, action, and subflow. This ensures that a flow intended for one domain does not duplicate the name of a flow in another domain. For example, add the domain to the flow name such as `Validate incidents - TOP`, `Validate incidents - ACME`, and `Validate incidents - INITECH`.

-   **Ensure that flows and actions only contain artifacts from current or parent domains**

    Workflow Studio prevents the activation of any flow containing artifacts unavailable to the current or parent domains. For example, if you create a domain-specific flow that belongs to the ACME domain, it cannot contain actions or subflows belonging to the sibling domain INITECH.

-   **Edit Workflow Studio content in the domain to which it belongs**

    Users in a parent domain can't see flows, actions, and subflows in a child domain. They must change to the domain to which they belong to edit them. For example, an administrator in the TOP domain can't see flows from the ACME domain. The administrator must switch to the ACME domain to see and edit them.


## Deployment

-   **Avoid deploying newer release flows to instances on older releases**

    Workflow Studio does not support deploying newer release flows to instances running on earlier releases.

    **Danger**

    The flow data model can change between releases, which can prevent newer flows from running or produce unexpected results when running on earlier release instances. Upgrade your instances to be on the same release versions before deploying them.


## Flow error handling

Follow these general guidelines to achieve the benefits offered by flow error handling.

-   **Avoid adding error handling items to the main section of the flow**

    A flow normally stops running when an action or subflow returns an error in the main section. A stopped flow cannot run any actions or subflows past the point where it returned an error. Adding error handling actions and subflows to the Error Handler section ensures they run them when there is an error.

-   **Capture Error Status information**

    The Error Status object contains information about the action that produced an error. You can use this information to identify the cause of the error as well as record data that may need correction.

-   **Suppress subflow error messages**

    You can enable the Error Handler for a subflow to prevent its errors from cascading to a parent flow. Leaving the subflow Error Handler section empty ensures that it always generates the **Completed \(error caught\)** state.

-   **Use subflows to avoid the 10-item limit**

    Rather than force your error-handling-process to fit within a 10-item limit, call subflows, which can contain many more items. You can also use the subflow outputs to trigger automation in other flows.

-   **Use subflows to take corrective actions**

    Rather than recreate the same sequence of actions in multiple flows, create reusable subflows to correct errors to your record data. When a flow error leaves your record data in an undesired state, use subflows to correct these records. You can use the error handler to identify such record data as a subflow output.


## Action error evaluation

Follow these general guidelines to achieve the benefits offered by action error evaluation.

-   **Allow only independent steps to continue running**

    Allow a step to continue running if it does not return data required by a later step. If a step provides data necessary for later steps, then you know that the later steps cannot run successfully.

-   **Avoid more than 10 error conditions**

    While there is no limit to the number of error conditions you can create, each error condition requires evaluation. The more error conditions your action has to evaluate, the potentially slower your action can run.

-   **Identify specific step failures**

    You can use the Step Status to identify when a specific step fails. Identifying a specific step can be useful when your action contains multiple instances of the same type of step. You may also want to identify a specific step so that a flow error handler can take appropriate corrective actions for the failure.

-   **Put specific error conditions before general error conditions**

    Error evaluation stops when the action finds a matching error condition. Putting general error conditions first may prevent the action from ever matching specific error conditions.

-   **Use descriptive error condition labels**

    Identify an error condition without having to edit it. By default, you can only see error conditions when you edit them.


## Flow Administrator

-   **Turn flow reporting off in production**

    Minimize the amount of memory required to run flows by disabling [Flow reporting](../task/enable-flow-reporting.md#). Flow reporting stores configuration and runtime information for the Execution Details page. These reports are good for troubleshooting, but requires a large amount of data to be retained both in memory and in the database. By default, flow reporting is disabled, and the system only generates execution details when you manually test a flow or action. Instead you can use log files, which are still available when reporting is turned off.

-   **Reduce the amount of memory consumed in flows with nested looping**

    When reporting is activated, set com.snc.process\_flow.reporting.iteration.lastn to a value of "1" to reduce the amounts of the amounts of memory that previous loop iterations consume. The more iterations you report on, the more memory is required.

-   **View final transformed values in the flow execution details**

    Only the final transformed value appears in the [flow execution details](../concept/flow-execution-details.md), and not the value for each applied transform.


## Flow Priority

Follow these design considerations when setting flow priority.

-   **Avoid setting all flows to run at high priority**

    Use a mix of priorities rather than set all flows to high priority. Worker threads use the relative priority between flows to select work. If all of your flows run at high priority, then there are no lower-priority flows to make wait.

-   **Avoid setting flow priority for flows that have to pause**

    Keep flows that have to pause at the default medium priority since a flow that pauses loses its priority value when it resumes running.

-   **Use high priority for business critical flows**

    Limit high-priority to flows that have high business value, run rarely, and have a short runtime. Avoid setting high-volume flows to high priority as doing so limits the number of worker threads available to run other flows. A long-running high priority flow can also reduce the worker threads available to run other flows.

-   **Use low priority for high-volume flows**

    Run high-volume flows at low priority so that other time-sensitive flows can run first. Low-priority flows shouldn't be time-sensitive.

-   **Use medium priority for time-sensitive flows**

    Use the default flow priority when a flow has some time urgency when compared to other flows.


**Parent Topic:**[Flows, subflows, and actions reference](flow-designer-reference.md)

**Related topics**  


[https://learning.servicenow.com/](https://learning.servicenow.com/)

