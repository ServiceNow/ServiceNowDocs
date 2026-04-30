---
title: UI scripts
description: UI scripts provide a way to package client-side JavaScript into a reusable form, similar to how script includes store server-side JavaScript. Administrators can create UI scripts and run them from client scripts and other client-side script objects and from HTML code.You can create a UI script and designate it as global, which makes the script available on any form in the system. You cannot create a global UI script in a scoped application.Create a UI script to define reusable client-side JavaScript code.Follow these guidelines when running UI scripts.
locale: en-US
release: yokohama
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Client-side scripting, Scripting, API implementation, API implementation and reference]
---

# UI scripts

UI scripts provide a way to package client-side JavaScript into a reusable form, similar to how script includes store server-side JavaScript. Administrators can create UI scripts and run them from client scripts and other client-side script objects and from HTML code.

UI scripts are not supported for mobile.

**Parent Topic:**[Client-side scripting](client-side-scripting-overview.md)

## Global UI scripts

You can create a UI script and designate it as global, which makes the script available on any form in the system. You cannot create a global UI script in a scoped application.

You can mark a UI script as Global to make it available on any form in the system. For example, you can create a UI script that has a function helloWorld\(\), and has the **Global** field checked:

```
function helloWorld() {
  alert('Hi');
}
```

After you create this global UI script, you can call the helloWorld\(\) function from any client script or UI policy you write.

## Create a UI script

Create a UI script to define reusable client-side JavaScript code.

### Procedure

1.  To create UI scripts, navigate to **System UI** &gt; **UI Scripts** and create or edit a record \(see table for field descriptions\).

<table id="table_zsc_z4z_sr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Script Name

</td><td>

Name of the UI script. Ensure the name is unique on your system.

</td></tr><tr><td>

API Name

</td><td>

The API name of the UI script, including the scope and script name \(for example, x\_custom\_app.HelloWorld\).

</td></tr><tr><td>

Application

</td><td>

Application that contains the UI script.

</td></tr><tr><td>

Active

</td><td>

Indicator of whether the UI script is active. Only active UI scripts can run.

</td></tr><tr><td>

Global

</td><td>

Indicator of whether the script loads on every page in the system.

 **Note:** Use caution when creating global UI scripts because they can impact performance. You cannot create a global UI script in a scoped application.

</td></tr><tr><td>

Description

</td><td>

Summary of the purpose of the script.

</td></tr><tr><td>

Script

</td><td>

Client-side script to run when called from other scripts.

</td></tr></tbody>
</table>
## Run UI scripts

Follow these guidelines when running UI scripts.

### Run a UI script from a form

To run a UI script on a form, [Create a formatter and add it to a form](https://www.servicenow.com/docs/access?context=t_CreateAFormatter&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US). In the associated [UI macro](../../server-scripting/concept/c_UIMacros.md#), include a `g:requires` tag and specify the **name=** parameter as the name of the UI script followed by the .jsdbx extension. Add the formatter on the form view.

This code ensures that the definitions and results of the UI script are immediately available in the browser.

```
<?xml version="1.0" encoding="utf-8" ?>  
<j:jelly trim="false" xmlns:j="jelly:core" xmlns:g="glide" xmlns:j2="null" xmlns:g2="null">  
    <g2:evaluate var="jvar_stamp">  
        var now_GR = new GlideRecord('sys_ui_script');  
        gr.orderByDesc('sys_updated_on');  
        gr.query();  
        gr.next();  
        gr.getValue('sys_updated_on');  
    </g2:evaluate>  
    <g:requires name="<UI SCRIPT NAME>.jsdbx" params="cache=$[jvar_stamp]" />  
</j:jelly>
```

### Call a UI script in HTML

To run a UI script from HTML code, use the `<script>` tag and specify the `src=` argument as the API name of the UI script followed by the .jsdbx extension. For example, include the UI script named CoolClock with this code:

```
<script language="javascript" src="CoolClock.jsdbx" />
```

### Call a UI script from client-side code

Access UI scripts from within client-side code using the g\_ui\_scripts global object. For more information, see [GlideUIScripts - Client](../../../app-store/dev_portal/API_reference/GlideUIScripts/concept/GUIScriptsAPI.md#).

**Note:** This class does not support UI scripts with the **Global** field set to true.

