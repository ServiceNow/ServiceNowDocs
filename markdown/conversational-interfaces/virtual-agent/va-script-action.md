---
title: Script Action utility
description: Use the Script Action utility in a Virtual Agent topic to run a script.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Virtual Agent Designer utilities, Virtual Agent Designer interface reference, Virtual Agent reference, Virtual Agent, Conversational Interfaces]
---

# Script Action utility

Use the Script Action utility in a Virtual Agent topic to run a script.

## Script Action utility properties

<table id="table_nff_y1b_3db"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Node name

</td><td>

The name that identifies this Script Action node in the topic flow.

</td></tr><tr><td>

Action expression

</td><td>

The script that performs an action.

</td></tr><tr><td class="sub-head" colspan="2">

Advanced

</td></tr><tr><td class="sub-head" colspan="2">

Hide this node

</td></tr><tr><td>

Conditionally show this node if

</td><td>

No-code condition statement or low-code script that specifies a condition for presenting this node in the conversation. The condition must evaluate to true.

</td></tr></tbody>
</table>## Example Script Action utility

![Basic properties include the node name and the action expression that contains the script.](../images/ScriptActionExample.png "Script Action utility basic properties")

## Example script action

```
(function execute() {
    var list = [];
    if (vaInputs.case_number != "") {
        var gr = new GlideRecord("sn_customerservice_case");
        gr.addQuery("number", "CONTAINS", vaInputs.case_number);
        gr.addQuery("active", "true");
        gr.orderBy("number");
        gr.query();
        while (gr.hasNext()) {
            gr.next();
            list.push(gr.getUniqueValue().toString());
        }
    }
    vaVars.case_list = list;
})()

```

This example performs a search on the \[sn\_customerservice\_case\] table for a specific case number based on the input from another control called `case_number`. The script then places the results in an array and stores them in the `case_list` variable, which is accessible by other nodes in the same topic. Because `vaVars` only supports string, number, and Boolean values, the script uses `toString()` to store these values as strings. The code is contained in an `if` statement, so it only executes if the `case_number` variable has a value. This `if` statement prevents the code from running if the user has not entered a number.

For more information about writing scripts for Virtual Agent, see [Virtual Agent scripts](../concept/virtual-agent-scripts.md).

**Parent Topic:**[Virtual Agent Designer utilities](va-utilities.md)

