---
title: Add output variables to scripted steps
description: Execute the following steps to add additional outputs in Run Server Side Script and Custom Scripted StepConfig test steps.Modify the test scripts of Run Server Side Script test step to create additional outputs of your choice.Copy the Custom Scripted StepConfig test step and customize the copied version by adding additional outputs.
locale: en-US
release: australia
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Step configurations, Administration, Automated Test Framework \(ATF\) reference, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Add output variables to scripted steps

Execute the following steps to add additional outputs in Run Server Side Script and Custom Scripted StepConfig test steps.

**Parent Topic:**[Step configurations](step-configurations-module.md)

## Adding outputs in Run Server Side Script test step

Modify the test scripts of Run Server Side Script test step to create additional outputs of your choice.

### Before you begin

Role required: admin or atf\_test\_admin

### Procedure

1.  Navigate to **All** &gt; **Automated Test Framework \(ATF\)** &gt; **Administration** &gt; **Step Configurations**.

2.  Search and select Run Server Side Script.

    The read-only Test Step Config form shows up.

    **Note:** Although the form is read-only, new output variables can be created.

3.  Scroll down to the Output Variables related list.

    The list of default output variables shows up.

4.  Click **New** to create a new output variable.

<table id="table_b5b_p14_dlb"><thead><tr><th>

Field

</th><th>

Input Value

</th></tr></thead><tbody><tr><td>

Type

</td><td>

Type of output variable

</td></tr><tr><td>

Application

</td><td>

Scope of the user

</td></tr><tr><td>

Label

</td><td>

User-facing name of the output variable

</td></tr><tr><td>

Column name

</td><td>

Variable name used in the script

</td></tr><tr><td>

Max length

</td><td>

Length of the data type.**Note:** This field doesn't show up for all data types.

</td></tr></tbody>
</table>    ![Gif showing creating new output variables](../image/run_server_side_script.gif)

    The new output variable gets added to the Output Variable related list.

5.  Navigate to **Automated Test Framework \(ATF\)** &gt; **Tests**.

6.  Select the test where you want to implement the new output variable.

7.  Click **Add Test Step**.

8.  Search and select Run Server Side Script test step.

9.  Follow the instructions to change outputs mentioned in the **Test script**.

    ```
    outputs.<column_name> = "<desired value>";
    ```

10. Click **Submit**.

    The newly created output variables are now ready to be used in any subsequent steps of the test.


## Adding outputs in Custom Scripted StepConfig test step

Copy the Custom Scripted StepConfig test step and customize the copied version by adding additional outputs.

### Before you begin

Role required: admin or atf\_test\_admin

### Procedure

1.  Navigate to **All** &gt; **Automated Test Framework \(ATF\)** &gt; **Administration** &gt; **Step Configurations**.

2.  Search and select Custom Scripted StepConfig.

    The read-only Test Step Config form shows up.

    **Note:** Since the form is read-only, you must copy the test step to customize it to add more output variables.

3.  Select **Copy** to have a copied version of the test step.

    **Note:** The copied version is no longer read-only.

4.  Add additional output variables in the copied version by implementing the following steps:

    1.  Select **New** under Output Variables related list.

    2.  Modify **Step execution script** to add more output variables.

    See [Adding outputs in Run Server Side Script test step](scripting_atf.md#) to add more output variables.

    **Note:** You can use these steps to customize the test step only in the copied version.

5.  Reuse the copied version of the test step in any test whenever required.

    ![Gif showing reusing of Custom Scripted StepConfig test step](../image/custom_scripted_test_config-p.gif)


