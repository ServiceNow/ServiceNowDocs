---
title: UI macros
description: UI macros are discrete scripted components administrators can add to the user interface.UI macros can be used to build solutions that can’t be built using the available catalog variable types.Administrators can call UI macros from certain record types associated with the user interface.Each UI macro record consists of a name and an XML document written in Jelly code.This section describes how to create a custom approval UI macro.
locale: en-US
release: yokohama
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Creating custom UI Pages and UI macros, Scripting, API implementation, API implementation and reference]
---

# UI macros

UI macros are discrete scripted components administrators can add to the user interface.

UI macros are typically controls that provide inputs or information not provided by existing field types. By default, the system provides UI macros for a variety of user interface elements such as:

-   All formatters
-   The Service Catalog cart
-   The action icons next to fields
-   The action icons on forms and lists
-   The widgets of a content management system
-   The Orchestration activity designer

Administrators can create their own UI macros to provide custom controls or interfaces. Creating UI macros requires knowledge of [Jelly script](http://commons.apache.org/proper/commons-jelly/). Review the existing UI macros for examples and suggested approaches. Those who want to build custom interfaces with JavaScript technologies should consider Service Portal as an alternative.

**Note:** To view available UI macros, navigate to **All** &gt; **System UI** &gt; **UI Macros**.

**Parent Topic:**[Creating custom UI Pages and UI macros](../../general-scripting/concept/create-custom-ui-pages.md)

## UI macro basics

UI macros can be used to build solutions that can’t be built using the available catalog variable types.

### Accessible UI macros

Several UI macros are available in the UI macros \[ui\_macros\] table. These UI macros have names starting with `ui_` and emulate the behavior of a subset of standard form field types for use in UI pages. For example, the ui\_date\_time UI macro can act like a glide\_date\_time field in a UI page, providing a type-able input field with a date/time selector.

A UI macro can be included in a UI page with the &lt;g:&gt; Jelly tag. The following example includes the ui\_date\_time UI Macro, providing two optional attributes to the UI Macro:

```
<g:ui_date_time name="due_date" value="2023-11-24 08:30:00" onchange="checkDateValue()" />
```

The attribute values in the &lt;g:&gt; Jelly tag are provided to the UI macro as jvar-prefixed variables. The UI macro can use the jvar-prefixed variables in its XML.

|Attributes|jvar-prefixed variables|
|----------|-----------------------|
|name|jvar\_name|
|value|jvar\_value|
|onchange|jvar\_onchange|

**Note:** These UI macros aren’t intended to support all features of their corresponding form field type. In many cases, the macros are only intended for specific ServiceNow application use cases.

The `ui_`-prefixed UI macros include descriptions specifying supported attributes that can \(or must\) be provided in the UI page's &lt;g:&gt; Jelly tag. To view available UI macros, navigate to **All** &gt; **System UI** &gt; **UI macros**.

/

### Custom UI macros

The ui\_example UI macro uses three jvar-prefixed variables: jvar\_name, jvar\_test\_attribute and jvar\_laptop\_type. These variables can be provided to the UI macro as name, test\_attribute and laptop\_type attributes in a &lt;g:&gt; Jelly tag in a UI page.

-   **Creating the ui\_example UI macro**

    Navigate to **All** &gt; **System UI** &gt; **UI Macros** and select **New**.

    Name the macro `ui_example` and add the following script to the **XML** field:

    ```
    <?xml version="1.0" encoding="utf-8" ?>
    <j:jelly trim="true" xmlns:j="jelly:core" xmlns:g="glide">
        <div>name jvar: ${jvar_name}</div>
        <div>test_attribute jvar: ${jvar_test_attribute}</div>
        <div>laptop_type jvar: ${jvar_laptop_type}</div>
    </j:jelly>
    ```

-   **Using the macro in a UI page**

    Navigate to **All** &gt; **System UI** &gt; **UI Pages** and select **New**. You will be asked to select an administrator role.

    Name the UI page and add the following script to the **HTML** field:

    ```
    <?xml version="1.0" encoding="utf-8" ?>
    <j:jelly trim="false" xmlns:j="jelly:core" xmlns:g="glide" xmlns:j2="null" xmlns:g2="null">
        <div style="text-decoration:underline">Template include one:</div>
        <g:ui_example name="Fred Luddy" test_attribute="I am an attribute" laptop_type="ThinkPad" />
        <hr/>
        <div style="text-decoration:underline">Template include two:</div>
        <g:ui_example name="Pat Casey" test_attribute="I am a different attribute" laptop_type="Macbook Pro" />
    </j:jelly>
    ```

-   **Checking output**

    In the UI page, you can click **Try It** to view the results.


**Note:** If you create a macro and it doesn’t display as expected in the UI page, clearing the cache might help. To clear the cache of your instance, in your browser, enter `<server_url>/cache.do`.

**Related topics**  


[UI pages](../reference/r_UIPages.md#)

[Jelly tags](../../general-scripting/reference/r_JellyTags.md)

[&lt;g:ui\_form/&gt;](../../general-scripting/concept/c_ExtensionsToJellySyntax.md#)

[&lt;g:ui\_input\_field /&gt;](../../general-scripting/concept/c_ExtensionsToJellySyntax.md#)

[&lt;g:ui\_checkbox/&gt;](../../general-scripting/concept/c_ExtensionsToJellySyntax.md#)

## Calling UI macros

Administrators can call UI macros from certain record types associated with the user interface.

<table id="table_j2v_pzq_rv"><thead><tr><th>

Record type

</th><th>

Example

</th></tr></thead><tbody><tr><td>

Dictionary attribute

</td><td>

Display an icon for a reference field:

 ```
ref_contributions=ui_macro_name
```

</td></tr><tr><td>

UI page

</td><td>

Display something on a UI page:

 ```
<g:macro_invoke macro="ui_macro_name" />
```

</td></tr><tr><td>

UI macro

</td><td>

Call a UI macro from another UI macro:

 ```
<?xml version= "1.0" encoding="utf-8"&nbsp;?>
<j:jelly trim= "false" xmlns:j="jelly:core" xmlns:g="glide" xmlns:j2="null" xmlns:g2="null">
  <g:ui_macro_name />
  <g:ui_macro_name_2 />
</j:jelly>
```

</td></tr></tbody>
</table>## UI macro form

Each UI macro record consists of a name and an XML document written in Jelly code.

|Field|Description|
|-----|-----------|
|Name|A unique and descriptive name for this macro.|
|Active|Select the check box to render the element as defined. Clear the check box to disable the element without deleting the code. For example, the **email\_reply** macro is inactive by default.|
|Description|Describe the purpose of the macro and parameters passed to it.|
|XML|Jelly script that defines the macro.|

## Custom approval UI macro

This section describes how to create a custom approval UI macro.

**Warning:** The customization described here was developed for use in specific instances, and is not supported by Now Support. This method is provided as-is and should be tested thoroughly before implementation. Post all questions and comments regarding this customization to our community [forum](http://community.service-now.com/).

**Script Name**: Custom Approval UI Macro

**Type**: UI Macro

**Description**: Here is an option to get more detail out of the My Approvals view of an Execution Plan. This can be done by creating a new UI macro. Navigate to **System UI** and click **UI Macros**. First, you will need to rename the existing `approval_summarizer_sc_task` to something like `approval_summarizer_sc_task_old` and deactivate it. Then you will need to create a new one using the same name \(`approval_summarizer_sc_task`\). The name should basically tell you what the macro does and what it applies to. In this case, we're replacing an existing one so we decided to re-use the existing name.

![](../../useful-scripts/image/ApprovalMacros.png "Approval macros")

Then you should copy the xml script at the bottom of this article into the xml code window in the new UI macro. This is great way to give some detail to an approver when you are doing line item approvals via approval tasks within the Service Catalog Execution Plans.

### The old way

This is the view you see in My Approvals when using an approval task via the old method.

![](../../useful-scripts/image/MyApprovalsOld.png "My Approvals (old way)")

Notice there is not much detail telling the approver what they are actually approving. You can see the short description of the task but not much around what the item is.

### The new way

This is the view you will see if you use the xml script below in place of the OOB \(out-of-box\) UI macro.

![](../../useful-scripts/image/MyApprovals.png "My Approvals")

Using this method you can see details much like the request approval. You have a link into the item ordered, a short description \(which contains the ability to expand the variables from the item\), price, quantity and the total price. This helps the approver in that it shows more detail. They can now see what they are actually approving.

Script:

```
<?xml version="1.0" encoding="utf-8" ?>
    <j:jelly trim="true" xmlns:j="jelly:core" xmlns:g="glide" xmlns:j2="null" xmlns:g2="null">
    <tr>
        <td class="label_left" width="100%">
            <label style="margin-left: 10px">
                ${gs.getMessage('Summary of Item being approved')}:
                <input style="visibility: hidden" NAME="make_spacing_ok"></input>
            </label>
        </td>
    </tr>
    <g:evaluate var="jvar_ni" expression="
        var sc_task = ${ref}.sysapproval;
        var sc_req_labels = new GlideRecord('sc_req_item');
        sc_req_labels.initialize();
        var sc_req_item = new GlideRecord('sc_req_item');
        sc_req_item.addQuery('request_item', sc_task.request_item.sys_id);
        sc_req_item.query();
    " />
    <tr>
        <td width="100%">
            <table width="100%">
                <tr>
                    <td class="label_left" width="150px">
                        <label style="margin-left: 10px">
                            ${sc_task.request_item.request.opened_by.sys_meta.label}:
                        </label>
                    </td>
                    <td>
                        ${sc_task.request_item.request.opened_by.getDisplayValue()}
                    </td>
                </tr>
                <tr> 
                    <td class="label_left" width="150px">
                        <label style="margin-left: 10px">
                            ${sc_task.request_item.request.requested_for.sys_meta.label}:
                        </label>
                    </td>
                    <td>
                        ${sc_task.request_item.request.requested_for.getDisplayValue()}
                    </td>
                </tr>
                <tr>
                    <td class="label_left" width="150px">
                        <label style="margin-left: 10px">${gs.getMessage('Total')}:</label>
                    </td>
                    <td>
                        <g:currency_format value="${sc_task.request_item.request.price}" />
                    </td>
                </tr>
            </table>
        </td>
    </tr>
    <j:set var="jvar_line_num" value="0" />
    <tr>
        <td width="100%">
            <table width="100%">
                <tr class="header">
                    <td colspan="2">
                        ${sc_req_labels.number.sys_meta.label}
                    </td>
                    <td>
                        ${sc_req_labels.description.sys_meta.label}
                    </td>
                    <td>
                        ${sc_req_labels.price.sys_meta.label}
                    </td>
                    <td>
                        ${sc_req_labels.quantity.sys_meta.label}
                    </td>
                    <td>
                        ${gs.getMessage('Total')}
                    </td>
                </tr>
                <j:set var="jvar_item_price" value="${sc_task.request_item.price * sc_task.request_item.quantity}"/>
                <j:set var="jvar_overall_total" value="${jvar_overall_total + jvar_item_price}"/>
                <j:set var="jvar_line_color" value="odd"/>
                <j:set var="jvar_line_num" value="${jvar_line_num + 1}"/>
                <j:if test="${jvar_line_num % 2 == 0}">
                    <j:set var="jvar_line_color" value="even"/>
                </j:if>
                <g:evaluate var="ni" expression="
                    var smart_description = sc_task.request_item.cat_item.short_description;
                    if (smart_description == null || smart_description == '' || smart_description == 'undefined')
                        smart_description = sc_task.request_item.cat_item.name;
                "/>
                <tr class="${jvar_line_color}">
                    <td valign="top">
                        <g2:evaluate var="jvar_pop_target" expression="$[ref].getRecordClassName()" />
                        <a class="linked" target="gsft_main"
                            href="sc_req_item.do?sys_id=${sc_task.request_item.sys_id}"
                            onmousemove="popListDiv(event, 'sc_req_item', '${sc_task.request_item.sys_id}','${sysparm_view}')"
                            onmouseout="lockPopup(event)">
                            <img src="images/icons/hover_icon.gifx" class="clsshort"/>
                        </a>
                    </td>
                    <td valign="top">
                        <a class="linked" target="gsft_main"
                            href="sc_req_item.do?sys_id=${sc_task.request_item.sys_id}">
                            ${sc_task.request_item.number}
                        </a>
                    </td>
                    <td valign="top" width="50%">
                        <g:call function="variable_summary_approval.xml" 
                            question_name="${sc_task.request_item.sys_id}"
                            question_help_tag="${smart_description}" 
                            sc_req_item="${sc_task.request_item.sys_id}"
                            help_class="${jvar_line_color}"/>
                    </td>
                    <td valign="top"> <g:currency_format value="${sc_task.request_item.price}"/> </td>
                    <td valign="top"> ${sc_task.request_item.quantity}</td>
                    <td valign="top"> <g:currency_format value="${jvar_item_price}"/></td>
                </tr>
            </table>
        </td>
    </tr>
</j:jelly>
```

