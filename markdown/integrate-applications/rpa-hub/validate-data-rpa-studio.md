---
title: Validate the data in RPA Desktop Design Studio
description: Validate your data by using the Validate Data option at a component level in RPA Desktop Design Studio.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Using automations, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Validate the data in RPA Desktop Design Studio

Validate your data by using the **Validate Data** option at a component level in RPA Desktop Design Studio.

## Before you begin

Configure a component. For more information, see [Use a component in RPA Desktop Design Studio](configure-components.md).

Role required: none

## About this task

You can ensure that the data coming from a Data Out port is not null by using the NotNullValidation validation type. You can also write custom validations by using a script.

## Procedure

1.  In the RPA Desktop Design Studio, on the Design surface, right-click either the Data In or Data Out port of a component and select **Validate Data**.

2.  In the VALIDATIONS dialog box, from the Validator list, select either of the following validation types:

<table id="table_hnm_vtk_4rb"><thead><tr><th>

Type

</th><th>

Description and action

</th></tr></thead><tbody><tr><td>

NotNullValidation

</td><td>

Checks if the given input is null. A custom message can be inputted for validation and error handling.

 1.  Click the plus icon \(![Plus icon.](../image/add-image-icon.png)\) to add a validation.
2.  In the text box next to **\[NOT NULL\]**, enter the custom error message as shown in the following example.

![Text box for entering the error message.](../image/not-null-validation-text-box.png "Text box for entering the error message")

3.  Click **OK**.


</td></tr><tr><td>

ScriptValidation

</td><td>

Enables you to choose from a list of programming languages and write a validation script to ensure the data that flows in or out of the Data port is validated against the mentioned conditions. Otherwise, it stops execution and throws an error.1.  Click the plus icon \(![Plus icon.](../image/add-image-icon.png)\) to add a validation.
2.  Click the script icon \(![script icon.](../image/script-validation-icon.png)\) to open the SCRIPT VALIDATION dialog box.
3.  From the following SCRIPT LANGUAGE list, select your preferred scripting language to write your custom validation:
    -   **VB.NET**
    -   **C\#**
    -   **Javascript**
4.  In the Script section, enter the code. For example, `Return Value > 300`.
5.  Click **OK**.
6.  In the text box next to **\[SCRIPT\]**, enter the custom error message as shown in the following example.

![Field for entering the error message.](../image/script-validation-textbox.png "Field for entering the error message")

7.  Click **OK**.


</td></tr></tbody>
</table>3.  To delete a validation rule, click the delete icon \(![Delete icon.](../image/remove-icon.png)\) and in the Confirmation dialog box, click **Yes**.


**Parent Topic:**[Using automations](../concept/rpa-studio-use.md)

