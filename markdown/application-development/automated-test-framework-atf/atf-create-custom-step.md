---
title: Create custom step configuration
description: Create a custom step configuration that can form the basis of new steps that run on the server.
locale: en-US
release: xanadu
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Creating custom test step configurations, Administering the Automated Test Framework, Test your apps with the ATF, Testing and debugging applications, Building applications]
---

# Create custom step configuration

Create a custom step configuration that can form the basis of new steps that run on the server.

## Before you begin

Role required: atf\_test\_admin

**Note:** Creating configurations are only supported in the server steps, the UI steps \(running in the browser\) are not supported. Also, only scripted steps are supported, custom Java-based steps are not supported.

## About this task

The Automated Test Framework includes specific types of steps such as Open Form, Set Value, Assert Value and so forth. With the **Step Configurations** module, you can create steps that perform actions you specify. You can only create configurations for steps that run on the Server. You cannot create configurations for steps that run on the browser.

## Procedure

1.  Navigate to **All** &gt; **Automated Test Framework** &gt; **Administration** &gt; **Step Configurations**.

2.  Click **New**.

    The system displays the **Test Step Config** form.

3.  In the **Name** field, enter a name for your step type.

4.  Leave **Active** checked.

5.  Leave **Step environment** set to **Server-Independent**.

    You can define only step configurations that run on the server and not step configurations that run in the browser.

6.  In the **Category** field, select the category to which you want to assign this step.

    Categories are used for filtering the step list in the Add Step dialog. For more information, see [Category field example](../reference/atf-step-config-xmpls.md#hbm_xwc_yw).

7.  In the **Batch Order Constraint** field, choose one of the following values.

    -   **None**: A step based on this configuration can appear at any point in a test.
    -   **Start Batch Execution**: If this test includes a batch with this step, this step must be the first in the batch.
    -   **Run in the middle of an execution**: If a test includes a batch with this step, this step must appear after the first and before the last step of the batch.
    -   **Stop Execution**: If a test includes a batch with this step, this step must be the last step in the batch.
8.  In the **Order** field, enter an integer specifying where steps with this configuration appear in the step list on the Add Test Step dialog.

    For more information, see the example using the **Order** field in [Order field example](../reference/atf-step-config-xmpls.md#iss_1jv_xw).

9.  In the **Template reminder** field, enter the instructions you want to appear when this step is included in a test as part of a template.

    For more information, see the [example of using the Template reminder field.](../reference/atf-step-config-xmpls.md#qzw_phv_xw)

10. In the **HTML description** field, enter the text you want to appear when the cursor highlights this step on the Create New Step dialog.

    For more information, see the example using the HTML description field in [.](../reference/atf-step-config-xmpls.md#qtf_33v_xw)

    **Note:** The next two steps involve writing scripts, which you should wait to complete until you have added input and output variables.

11. In the **Description generation script** field, add code to the provided template to generate the description assigned to a Test Step record when a step of this type is included in a test.

    For more information about writing this script, see [Step description generation script](../concept/atf-config-desc-script.md). To see an example of where the system displays this description, see [Description generation script example](../reference/atf-step-config-xmpls.md#b5m_zrx_yw).

12. In the **Step Execution Script** field, add code to the provided template to define the script that executes when a step of this type runs.

    The script template provides instructions and examples for working with step inputs, outputs, and step results. For more details on the step execution script, see [Step execution scripts](../concept/atf-config-script.md).

13. Click **Submit**.

    The system creates a new test step configuration and returns to the list of test configurations.

14. Add input variables to this step config.

    1.  Access the step config record.

    2.  Scroll to the Input Variables tab, then click **New**.

    3.  Fill in the required fields for the new variable.

    4.  Click **Submit**.

    5.  Repeat these steps until you have added all the input variables needed.

    6.  Control the order in which input variables appear on the New Step form by editing the values in the **Order** column for the Input Variables related list.

15. Add output variables to this step config.

    1.  Scroll to the Output Variables tab, then click **New**.

    2.  Fill in the required fields for the new variable.

    3.  Click **Submit**

    4.  Repeat these steps until you have added all the output variables needed.


**Parent Topic:**[Creating custom test step configurations](../concept/atf-custom-step-types.md)

**Related topics**  


[Step execution scripts](../concept/atf-config-script.md)

[Step configurations](../concept/step-configurations-module.md)

[Automated Test Framework Step Config record](../reference/atf-step-config-record.md)

[Add a predefined list of steps \(template\) to an automated test](atf-use-template.md)

