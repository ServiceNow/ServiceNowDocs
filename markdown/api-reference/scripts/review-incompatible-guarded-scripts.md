---
title: Review and update scripts incompatible with guarded script
description: Review scripts that are incompatible with guarded script and either rewrite them to use supported features or create an exemption for scripts that can't be rewritten.
locale: en-US
release: australia
product: Scripts
classification: scripts
topic_type: task
last_updated: "2024-12-19"
reading_time_minutes: 3
keywords: [Guarded Script DSL, script remediation, script includes, script exemptions, incompatible scripts]
breadcrumb: [Guarded script evaluator, Sandbox environment, Server-side scripting, Scripting, API implementation, API implementation and reference]
---

# Review and update scripts incompatible with guarded script

Review scripts that are incompatible with guarded script and either rewrite them to use supported features or create an exemption for scripts that can't be rewritten.

## Before you begin

Role required: admin

## About this task

Guarded script detects and records scripts that use unsupported JavaScript features in the Incompatible Guarded Scripts list when transactions calling those scripts are sent. For information about supported features, see [JavaScript features supported by guarded script](../concept/guarded-script.md#supported-features).

**Note:** When guarded script is in Phase 1: Detection, scripts sent from authenticated users are recorded in the Incompatible Guarded Scripts list only if they have incompatible syntax. Scripts with incompatible APIs aren't recorded until Phase 2: Syntax enforcement.

Analyze each incompatible script and determine the best remediation approach. Consider the following factors when analyzing scripts:

-   Complexity of the script logic
-   Frequency of script execution
-   Business criticality of the functionality
-   Feasibility of rewriting using supported guarded script features

Automatic exemptions are created for incompatible scripts sent by authenticated users and detected during Phase 1: Detection and Phase 2: Syntax enforcement. To further secure your instance, you can still review any scripts that have an automatic exemption, update them to be compatible with guarded script, and then remove the exemption. For more information, see [Guarded script enforcement](../concept/guarded-script.md#guarded-script-enforcement).

## Procedure

1.  Navigate to **All** &gt; **Guarded Script** &gt; **Incompatible Guarded Scripts**.

2.  For each script in the list, select a remediation approach.

    **Note:** Scripts with the same logic are normalized into a single row in the list.

<table id="choicetable_jkt_gpt_v3c"><thead><tr><th align="left" id="d191558e136">

Option

</th><th align="left" id="d191558e139">

Steps

</th></tr></thead><tbody><tr><td id="d191558e145">

**Move complex logic to a script include**

</td><td>

For scripts that contain complex logic and can be rewritten, move the logic to a script include. Script includes run outside of the sandbox so they can use all features supported by the JavaScript engine.1.  Remove complex logic from the script.
2.  Create a script include and add the removed code.
3.  On the Script Include form, select **Sandbox enabled**.
4.  Update the original script to call the new script include using a simple function call, such as `MyScriptInclude.function()`.
For more information about creating script includes, see [Script includes](../concept/c_ScriptIncludes.md#). You can test updated scripts by running them from the Scripts - Background module with **Execute in sandbox?** selected. For more information, see [Scripts - Background module](../concept/c_ScriptsBackground.md).

</td></tr><tr><td id="d191558e193">

**Create an exemption**

</td><td>

For scripts that can't be rewritten and are business-critical, create an exemption. Exempt scripts are routed to the script sandbox evaluator instead of the guarded script evaluator. For more information, see [Script sandbox evaluator](../concept/script-sandbox.md).**Warning:** Exemptions bypass the enhanced security provided by the guarded script evaluator and should be used sparingly.

1.  From the Incompatible Guarded Scripts list, select a script.
2.  Select **Add Exemption**.
You can deactivate or delete an exemption by opening an Incompatible Guarded Scripts record and navigating to the **Guarded Script Exemptions** related list.

**Note:** Exemptions aren't tracked in update sets. To move exemptions between instances, you must manually export and import them.

</td></tr></tbody>
</table>
When guarded script rejects a script, it logs an error with the following message: `KittyScript validation failed for <script name> with error: <error message> Source code: <script source>`. To identify these errors, navigate to **System Log** &gt; **Errors**. Use the script name and source in the error message to locate the corresponding entry in the Incompatible Guarded Scripts list and determine the appropriate remediation approach.

## Rewriting a script to use a script include

<table id="table_eg5_k2h_w3c"><thead><tr><th>

Before

</th><th>

After

</th></tr></thead><tbody><tr><td>

The Incompatible Guarded Scripts list includes the following script because it uses a variable and conditional logic:```javascript
var priority = current.priority;
if (priority == 1) {
    gs.beginningOfToday();
} else {
    gs.endOfLastWeek();
}
```

</td><td>

Move the complex logic from the original script to a script include:```javascript
var MyDateHelper = Class.create();
MyDateHelper.prototype = {
    initialize: function() {},
    getRelevantDate: function(priority) {
        if (priority == 1) {
            return gs.beginningOfToday();
        } else {
            return gs.endOfLastWeek();
        }
    },
    type: 'MyDateHelper'
};
```

Then, update the original script to use only a simple expression calling the script include so it's compatible with guarded script:

```javascript
new MyDateHelper().getRelevantDate(current.priority)
```

</td></tr></tbody>
</table>## What to do next

Monitor the Incompatible Guarded Scripts list regularly to identify any scripts that may need remediation. The list is updated when transactions calling those scripts are sent.

**Parent Topic:**[Guarded script evaluator](../concept/guarded-script.md)

