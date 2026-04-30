---
title: Scripting alert, info, and error messages
description: You can send messages to customers as alerts, informational messages, or error messages.
locale: en-US
release: yokohama
product: Scripts
classification: scripts
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Scripting, Building pro-code applications, Developing your application, Building applications]
---

# Scripting alert, info, and error messages

You can send messages to customers as alerts, informational messages, or error messages.

<table id="table_i1c_k2m_jp"><thead><tr><th>

Script

</th><th>

Result

</th></tr></thead><tbody><tr><td>

`current.field_name.setError("Hello World");`

</td><td>

Adds `Hello World` below the specified field in a red error message.

</td></tr><tr><td>

`gs.addInfoMessage("Hello World");`

</td><td>

Adds `Hello World` at the top of the browser window in a blue info message.

</td></tr><tr><td>

`gs.addErrorMessage("Hello World");`

</td><td>

Adds `Hello World` at the top of the browser window in a red error message.

</td></tr><tr><td>

`gs.print("Hello World");`

</td><td>

Writes `Hello World` to the text log on the file system but not to the sys\_log table in the database.

</td></tr><tr><td>

`gs.log("Hello World");`

</td><td>

Writes `Hello World` to the database and the log file.**Note:** gs.log can adversely affect performance if used too frequently.

</td></tr></tbody>
</table><table id="table_wbp_cfm_jp"><thead><tr><th>

Script

</th><th>

Result

</th></tr></thead><tbody><tr><td>

`alert("Hello World");`

</td><td>

Displays a window with `Hello World` and an **OK** button.**Note:** Rather than use JavaScript alert\(\), for a cleaner look, you can display an error on the form itself with thee showFieldMsg\(\) and hideFieldMsg\(\) methods. For more information, see [Display field messages](https://www.servicenow.com/docs/access?context=useful-client-side-scripts&version=yokohama&pubname=yokohama-api-reference&section=r_DisplayFieldMessages&ft:locale=en-US).

</td></tr><tr><td>

`confirm("Hello World");`

</td><td>

Displays a window with `Hello World?` and **OK** and **Cancel** buttons.

</td></tr><tr><td>

`g_form.showFieldMsg("field_name", "Hello World", "error");`

</td><td>

Adds `Hello World` below the specified field in a red error message.

</td></tr><tr><td>

`g_form.hideFieldMsg("field_name");`

</td><td>

Hides the most recent message for the specified field.

</td></tr></tbody>
</table>**Important:** The methods in this table are only for use in client scripts.

It is also possible to add other custom messages to your forms if necessary using client scripting.

The text size of info and error messages at the top of the screen is customizable. Two properties control this. If you configured your forms, you may need to add these properties.

**Note:** The client script alert option is not available for use with Automated Test Framework \(ATF\).

|Property|Description|
|--------|-----------|
|`css.outputmsg.info.text.font-size`|Sets the size for info messages. Default is 11pt.|
|`css.outputmsg.error.text.font-size`|Sets the size for error messages. Default is 11pt.|

**Parent Topic:**[Scripting](../../topic/c_Script.md)

