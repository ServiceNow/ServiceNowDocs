---
title: Create a subflow with Now Assist
description: Use generative AI to create a subflow from text directions and images.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Building subflows, Use, Workflow Studio, Build workflows]
---

# Create a subflow with Now Assist

Use generative AI to create a subflow from text directionsand images.

## Before you begin

-   Roles required:
    -   admin, flow\_designer, or a delegated developer permission
    -   now.assist.creator
-   Turn on the flow generation skill. See [Turn on the flow generation skill](turn-on-the-flow-generation-skill.md).
-   Turn on the flow generation with images skill. See [Turn on the flow generation with images skill](turn-on-the-flow-generation-with-images-skill.md).

## About this task

Generate subflows by using text prompts and image. Describe the subflow in details, attach an image that illustrates the process clearly, and generate the subflow with Now Assist. You can use only text prompts, only image, or both to generate the subflow. Review the and flow and if required, make necessary updates to the prompts and regenerate the subflow preview.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  From the Workflow Studio home page, select **New** &gt; **Subflow**.

3.  Select the **Build with Now Assist** tab and fill in the fields.

<table id="table_cnv_ps3_w2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Subflow name

</td><td>

Name to uniquely identify your subflow.

</td></tr><tr><td>

Application

</td><td>

Application scope to create your subflow in. Global is the default. The application scope determines what data your flow can access and what data it can share.**Important:** You can’t change the application scope of a flow after you’ve generated a preview for it.

</td></tr><tr><td>

Now Assist directions

</td><td>

Text and image used by Now Assist to create your subflow. You can use only text, only image, or image and text both to create the subflow. For example, if you attach an image of a flow chart, you can add additional information about the flow as text directions.Describe all the actions and flow logic in the order you want them in the subflow. Include as much detail as possible for the best results.

</td></tr><tr><td>

Try and example

</td><td>

Series of text examples to insert into the Now Assist directions field. Select this option to insert example text in the directions field. Each example illustrates directions that will build a subflow outline. Trying an example overwrites any directions text that you previously added. You can use the undo and redo options to revert to your previous directions.

</td></tr></tbody>
</table>    For general guidelines about writing Now Assist directions, see [Create a flow with Now Assist](create-flow-now-assist.md).

4.  Select **Show additional properties** and fill in the fields.

<table id="table_ctd_dgj_w2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Description

</td><td>

Description of the subflow.

</td></tr><tr><td>

Accessible from

</td><td>

Accessible from all application scoped or only within the specified application scope.

</td></tr><tr><td>

Category

</td><td>

Defined category within the application scope for a subflow. You can create a custom category to organize your subflows.

</td></tr><tr><td>

Protection

</td><td>

Select whether the subflow is read-only. You can only select a value when you create the subflow in an application scope you own. The default value is None.

</td></tr><tr><td>

Subflow annotation

</td><td>

Help text that appears under the subflow title in Workflow Studio to help flow authors understand what the subflow does when used in a flow.

</td></tr><tr><td>

Run as

</td><td>

Option to specify the user that runs the flow. You can select the system user or the user who initiates the session. Select the user who initiates the session option when updates should come from the user who triggered the flow. For example, use this option when you want the incident record comments to come from the user who started the flow. Settings for the Run as option in a flow don't apply to child subflows. Running as the initiating user also ensures the actions taken during flow execution are limited by the user's ACL restrictions. Flows run by the initiating user will also respect user-specific settings like date/time format.**Note:** When choosing the option to run as the user who initiates the session, ensure that your security restrictions do not prevent your users from making any changes the flow executes.

</td></tr><tr><td>

Run with roles

</td><td>

Roles that the flow runs with. This option is only available when **Run as** is set to **user who initiates the session**.

</td></tr><tr><td>

Flow priority default

</td><td>

Priority level at which you want the system to run this subflow by default. Options include:

-   Low
-   Medium \(Default\)
-   High
 To learn about flow priority levels, see [Flow priority](../concept/flow-priority.md).

</td></tr></tbody>
</table>5.  Select **Generate subflow preview**.

    Workflow Studio uses your text and image inputs to build a subflow outline. If successful, Workflow Studio displays a preview of the subflow in the diagramming view. Beneath each node of the subflow, there is an annotation showing the text directions used to generate the item.

    Review the generated subflow preview to make sure that the subflow meets your requirements. Hover over **Inputs and Outputs** to see a list of the inputs and outputs that the subflow will generate.

6.  If the generated subflow preview does not meet your needs, you can update the Now Assist directions, and select **Regenerate preview**.

    Each time you generate or regenerate a subflow, the operation counts as an assist tracked by your Now Assist subscription. To track your Now Assist usage, see [Monitoring Now Assist usage in Subscription Management](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

7.  If you want to stop generating the subflow and return to the Workflow Studio homepage, you can select **Discard subflow**.

    **Important:** Workflow Studio does not save subflow previews. If you discard a subflow, all information about it is lost.

8.  Select **Save and edit subflow** to review the subflow outline.


## Result

Now Assist creates a subflow outline with the name you provided. If the large language model couldn't find a matching action, flow logic, or subflow for your request, it may add one or more placeholder steps instead.

**Parent Topic:**[Building subflows](../concept/subflows.md)

