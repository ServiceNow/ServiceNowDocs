---
title: Topic Block utility
description: Use a Topic Block in a Virtual Agent conversation to perform a specific function or subflow that runs certain steps in a calling topic.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2024-11-05"
reading_time_minutes: 4
keywords: [Virtual Agent, topic block, utility]
breadcrumb: [Virtual Agent Designer utilities, Virtual Agent Designer interface reference, Virtual Agent reference, Virtual Agent, Conversational Interfaces]
---

# Topic Block utility

Use a Topic Block in a Virtual Agent conversation to perform a specific function or subflow that runs certain steps in a calling topic.

## Topic Block utility properties

For more information, see [Add a reusable topic block to a calling topic or topic block](../task/add-topic-blocks-to-topic.md).

<table id="table_nff_y1b_3db"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Use dynamic Topic Block

</td><td>

Set this toggle to activate dynamic Topic Block options.

</td></tr><tr><td>

Topic block

</td><td>

A list of published topic blocks. Select a topic block to add to the calling topic.With **Use dynamic Topic Block** active, use the condition builder to input a condition or script instead.

</td></tr><tr><td>

Node name

</td><td>

Name of the topic block node. The name is automatically assigned based on the topic block that you select. For example, if you choose the Acme Contextual Search topic block, the **Name** is Acme Contextual Search.With **Use dynamic Topic Block** active, input a name of your choice.

</td></tr><tr><td>

Input mapping

</td><td>

The variables to be used as input to the selected topic block. For example, the following image has example variables:

 ![In this example, input mapping variables include catalog item ID, execute contextual search, confirm catalog item, and show end state card.](../images/map-tb-input-values.png)

 The contents of this area change according to the topic block you selected. Options may include string input, referenced records, scripts, and so forth.

 With **Use dynamic Topic Block** active, you add all input mappings manually instead by selecting the Manage inputs to define icon ![Manage inputs to define icon.](../images/manage-inputs-outputs.png). Inputs are handled similarly to the Input Parameters dialog box in the Start segment of a [reusable topic block](../task/create-topic-blocks.md).

</td></tr><tr><td>

Output mapping

</td><td>

The variables to be output by the selected topic block. For example, the following image has example variables that are enabled:

 ![In this example, output mapping variables include record ID, record table, and user option variables.](../images/map-output-vars-tb.png)

 The contents of this area change according to the topic block you selected.

 With **Use dynamic Topic Block** active, you add all input mappings manually instead by selecting the Manage outputs to define icon ![Manage outputs to define icon.](../images/manage-inputs-outputs.png). Inputs are handled similarly to the Input Parameters dialog box in the Start segment of a reusable topic block.

</td></tr><tr><td class="sub-head" colspan="2">

Advanced

</td></tr><tr><td class="sub-head" colspan="2">

Hide this node

</td></tr><tr><td>

Conditionally use this node if

</td><td>

A no-code condition statement or low-code script that specifies a condition for presenting this node in the conversation. The condition must evaluate to true.

</td></tr></tbody>
</table>## Example Topic Block utilities

![Topic Block utility properties include the reference to an available topic block, input mapping variables to the topic block, and the output variables that the topic block will pass.](../images/topic-block-initial-props.png)![Topic Block utility properties with the Use dynamic Topic Block toggle switch turned on.](../images/topic-block-dynamic.png)

## Using dynamic Topic Blocks

Toggling the dynamic setting on the Topic Block enables you to programmatically choose which topic block or blocks to invoke, based on any number of conditions. You can pass in a dynamic set of inputs without an explicit, one-to-one match for a Topic Block definition.

For example, assume you have two Topic Blocks. One sets your password by taking your username and returning a success or fail message. The other resets your password, but requires that you send two-factor authentication \(2FA\) token with the request before returning a success or fail message and a temporary password.

You can create two separate Topic Block invocations to handle the password-reset procedure, or you can create one Topic Block with the dynamic setting active and defined as follows:

-   Add a script that checks if the reset type is `includesTwoFactor = true`. If the statement evaluates to `true`, then you return `TwoFactorReset`, otherwise you return `NormalPasswordReset`.
-   Define two input mappings: `password` and `twoFactorToken`, both set equal to an object passed in which contains their values.
-   Define two output mappings: `successful` and `tempPass`, the latter of which is only set if it exists in the return value for the Topic Block.
-   Define two output nodes to output success or failure, and an output to confirm to you whether the `tempPass` value is true.

## Example dynamic Topic Block expression

```
(function execute() {
    /* Return the name of the topic block to run. For example:
        switch (vaVars.car_make) {
            case 'Ford':
                return 'Ford troubleshooting';
            case 'Toyota':
                return 'Toyota troubleshooting';
            default:
                return 'General car troubleshooting';
        }
    */
})()
```

The script in the dynamic Topic Block expression returns a value based on your input. In this example, if you input `Ford` or `Toyota`, the Virtual Agent will call for the appropriate troubleshooting topic. If you input any other value, the Virtual Agent returns a general troubleshooting topic instead.

**Parent Topic:**[Virtual Agent Designer utilities](va-utilities.md)

