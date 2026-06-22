---
title: Reviewing scripts incompatible with guarded script
description: Guarded script records scripts that use unsupported JavaScript features in the Incompatible Guarded Scripts list when transactions calling those scripts are sent to the server.Review scripts that are incompatible with guarded script and either rewrite them to use supported features or create an exemption for scripts that can't be rewritten.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/scripts/incompatible-guarded-scripts.html
release: australia
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2026-06-11"
reading_time_minutes: 5
keywords: [Guarded Script DSL, incompatible scripts, script remediation, script exemptions, Guarded Script DSL, script remediation, script includes, script exemptions, incompatible scripts]
breadcrumb: [Guarded script evaluator, Sandbox environment, Server-side scripting, Scripting, API implementation, API implementation and reference]
---

# Reviewing scripts incompatible with guarded script

Guarded script records scripts that use unsupported JavaScript features in the Incompatible Guarded Scripts list when transactions calling those scripts are sent to the server.

**Note:** When guarded script is in Phase 1: Detection, scripts sent from authenticated users are recorded in the Incompatible Guarded Scripts list only if they have incompatible syntax. Scripts with incompatible APIs aren't recorded until Phase 2: Syntax enforcement. For information about JavaScript features and APIs supported by guarded script, see [JavaScript features supported by guarded script](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/scripts/guarded-script.md).

From the Incompatible Guarded Scripts list, you can analyze each incompatible script and determine whether to move complex logic to a script include or create an exemption. Consider the following factors when analyzing scripts:

-   Complexity of the script logic
-   Frequency of script execution
-   Business criticality of the functionality
-   Feasibility of rewriting using supported guarded script features

Automatic exemptions are created for incompatible scripts sent by authenticated users and detected during Phase 1: Detection and Phase 2: Syntax enforcement. To further secure your instance, you can still review any scripts that have automatic exemptions, update them to be compatible with guarded script, and then remove the exemptions. For more information about automatic exemptions, see [Guarded script enforcement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/scripts/guarded-script.md).

For more information about remediating incompatible scripts, see the [Server-Side Sandbox Runtime Replacement \[KB2944435\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2944435) article on the Now Support Knowledge Base.

**Parent Topic:**[Guarded script evaluator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/scripts/guarded-script.md)

## Update scripts incompatible with guarded script

Review scripts that are incompatible with guarded script and either rewrite them to use supported features or create an exemption for scripts that can't be rewritten.

### Before you begin

Role required: guarded\_script\_admin or admin

### Procedure

1.  Navigate to **All** &gt; **System Diagnostics** &gt; **Guarded Script** &gt; **Incompatible Guarded Scripts**.

    The list contains the following columns.

    |Column|Description|
    |------|-----------|
    |Is Authenticated|Whether the script was sent by an authenticated user or unauthenticated \(guest\) user.|
    |Occurrence count|The amount of times that the script has been encountered.|
    |Exemption|A reference to an exemption record if an exemption has been created for the script.|
    |Normalized script|The script source in normalized form. Scripts with the same logic and authentication type are normalized into a single record in the list. For example, scripts sent by guest users that contain `gs.daysAgoStart(7)` or `gs.daysAgoStart(30)` would be normalized into a single record in the list.|
    |Page Title|The endpoints of the transactions that sent the script. For transactions where a page title isn't applicable, the script name is used, such as with a scheduled job.|
    |Scope|The scopes in which the script ran.|
    |Stack trace|The JavaScript stack trace captured the first time that the script was recorded by guarded script.|

2.  For each script in the list, select a remediation approach.

    **Note:** In addition to recording incompatible scripts, guarded script logs errors for rejected scripts. To identify rejected scripts, navigate to **System Logs** &gt; **System Log** &gt; **Errors** with the following message: `KittyScript validation failed for <script name> with error: <error message> Source code: <script source>`. Use the script name and source code in the error message to locate the corresponding entry in the Incompatible Guarded Scripts list.

<table id="choicetable_jkt_gpt_v3c"><thead><tr><th align="left" id="d875227e368">

Option

</th><th align="left" id="d875227e371">

Steps

</th></tr></thead><tbody><tr><td id="d875227e377">

**Move complex logic to a script include**

</td><td>

For scripts that contain complex logic and can be rewritten, move the logic to a script include. Script includes run outside of the sandbox so they can use all features supported by the JavaScript engine.1.  Use the information from the list, such as the stack trace or a piece of the script, to search the instance and locate the script.
2.  Remove complex logic from the script.
3.  Create a script include that includes the removed code.
4.  On the Script Include form, select **Sandbox enabled**.
5.  Update the original script to call the new script include using a simple function call, such as `MyScriptInclude.function()`.
For more information about creating script includes, see [Script includes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/scripts/c_ScriptIncludes.md). You can test updated scripts by running them from the Scripts - Background module with **Execute in sandbox?** selected. For more information, see [Scripts - Background module](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/scripts/c_ScriptsBackground.md).

</td></tr><tr><td id="d875227e428">

**Create an exemption**

</td><td>

For scripts that can't be rewritten and are business-critical, create an exemption. Exempt scripts are routed to the script sandbox evaluator instead of the guarded script evaluator. For more information, see [Script sandbox evaluator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/scripts/script-sandbox.md).**Warning:** Exemptions bypass the enhanced security provided by the guarded script evaluator and should be used sparingly.

1.  From the Incompatible Guarded Scripts list, select a script.
2.  Select **Add Exemption**.
The exemption applies to every runtime variation of scripts that normalize to the same form with the same authentication type.

You can deactivate or delete an exemption by opening an Incompatible Guarded Scripts record and navigating to the **Guarded Script Exemptions** related list or by navigating to **All** &gt; **System Diagnostics** &gt; **Guarded Script** &gt; **Guarded Script Exemption**.

**Note:** Exemptions aren't tracked in update sets. To move exemptions between instances, you must manually export and import them.

</td></tr></tbody>
</table>
### Rewriting a script to use a script include

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
</table>### What to do next

Monitor the Incompatible Guarded Scripts list regularly to identify any scripts that may need remediation. The list is updated when transactions calling those scripts are sent.

