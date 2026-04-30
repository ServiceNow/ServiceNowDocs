---
title: Extensions to Jelly syntax
description: Apache's Jelly syntax is used to render forms, lists, UI pages, and many other things rendered in ServiceNow.Jelly often includes multiple namespaces when invoking tags.Usually, there are two phases indicated by namespaces &lt;j&gt; versus &lt;j2&gt; and &lt;g&gt; versus &lt;g2&gt;.You can use if statements in Jelly scripts.Sets a variable to one of two different values depending on whether a test is true or false.This page provides a comparative explanation of three tags: &lt;g:insert&gt;, &lt;g:inline&gt;, and &lt;g:call&gt;.The &lt;g:evaluate&gt; tag is used to evaluate an expression written in Rhino JavaScript and sometimes to set a variable to the value of the expression.This tag can be used to display the current Jelly variables and their values in the log.This tag defines a form on the UI page.This tag adds a reference to a UI macro that creates an input field on a page that allows users to input information. The ui\_input\_field passes a label, name, value, and size into the UI macro.This tag puts a user-editable check mark on a page. The name and value are passed into the UI macro.This tag puts buttons on the UI page that run a specified processing script if the tag returns true.This tag adds a reference to a page that can be referenced by a Processing Script.Ampersands in Jelly can cause you grief because Jelly is XML.Use $\{AND\} to insert a JavaScript and in Jelly.Similar to ampersands, less than \("&lt;"\) signs can also cause problems due to Jelly being XML. This can be resolved by reversing your test such that it is not necessary or by using $\{AMP\}lt; in place of the less than sign.Normally, white space is removed by Jelly. To keep it, you must specify that it not be trimmed.To encode a non-breaking space \(&amp;nbsp;\), you can use $\[SP\].ServiceNow has a feature that allows the evaluation of Jelly to be traced.
locale: en-US
release: xanadu
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 10
breadcrumb: [Jelly tags, Creating custom UI Pages and UI macros, Scripting, Building pro-code applications, Developing your application, Building applications]
---

# Extensions to Jelly syntax

Apache's Jelly syntax is used to render forms, lists, UI pages, and many other things rendered in ServiceNow.

With Jelly, logic can be embedded within static content and computed values may be inserted into the static content.

**Important:** This functionality requires a knowledge of Apache Jelly \(a Java and XML based scripting and processing engine for turning XML into executable code\).

This page from Apache has a summary of the standard Jelly tags: [http://commons.apache.org/jelly/tags.html](http://commons.apache.org/jelly/tags.html)

**Parent Topic:**[Jelly tags](../reference/r_JellyTags.md)

## Namespaces

Jelly often includes multiple namespaces when invoking tags.

The "j" namespaces are standard Jelly whereas the "g" namespaces are unique to ServiceNow scripts. For example, the &lt;g:evaluate&gt; tag is supplied by ServiceNow to allow you to compute a value using JavaScript. The standard Jelly tag &lt;j:test&gt; is used to evaluate a condition.

## Phases

Usually, there are two phases indicated by namespaces &lt;j&gt; versus &lt;j2&gt; and &lt;g&gt; versus &lt;g2&gt;.

The namespaces without the "2" happen in the first phase of processing and these are cached except when used in a UI page. Those with the "2" are never cached. Care must be taken when selecting whether to use phase 1 or phase 2 for efficiency and correct results.

In addition to the namespaces, the syntax used to insert values into static content differs depending on which phase is to supply the value. A dollar with braces surrounding a value inserts the value in phase 1. For example, `${jvar_ref}` inserts the value `jvar_ref` during phase 1 of the jelly process. A dollar with brackets surrounding a value inserts the value in phase 2. For example, `$[jvar_ref]` inserts the value `jvar_ref` during phase 2. A value surrounded by quotes is treated as a string. For example, `'[jvar_ref]'` inserts the value `jvar_ref` as a string during phase 2.

```
 <script>
if (confirm("$[gs.getMessage('home.delete.confirm') ]"))
   ...
</script>
```

```
<input type="hidden" id="${jvar_name}" name="${jvar_name}" value="${jvar_value}" class="${jvar_class}" />
```

## If tests

You can use if statements in Jelly scripts.

Testing whether something is true or not can be done as follows:

```
<j:if test="${jvar_something}">...do something...</j:if>
<j:if test="${!jvar_something}">...do something...</j:if>
```

The reason this statement works, is that, in Jelly, a term like jvar\_something is "truthful" in an if tag if:

1.  it is Boolean and true
2.  it is a String and = "true", "yes", "on", or "1"

Testing whether something exists can be done as follows:

```
<j:if test="${empty(jvar_something)}">...do something...</j:if>
```

The reason this statement works is that the JEXL empty function returns true if its argument is:

1.  null
2.  an empty string
3.  a zero length collection
4.  a map with no keys
5.  an empty array

**Note:** You cannot mix javascript and jvar variables in a JEXL expression. They must be broken into separate expressions.

## Set\_If

Sets a variable to one of two different values depending on whether a test is true or false.

```
<g2:set_if var="jvar_style" test="$[gs.getPreference('table.compact') != 'false']" 
   true="margin-top:0px; margin-bottom:0px;" 
   false="margin-top:2px; margin-bottom:2px;" />
```

## &lt;g:insert&gt; versus &lt;g:inline&gt; versus &lt;g:call&gt;

This page provides a comparative explanation of three tags: &lt;g:insert&gt;, &lt;g:inline&gt;, and &lt;g:call&gt;.

### &lt;g:insert&gt;

The &lt;g:insert&gt; tag inserts a Jelly file into your Jelly in a new context. This means you cannot access the variables previously established in your Jelly.

```
<g:insert template="get_target_form_function.xml" />
```

### &lt;g:inline&gt;

The &lt;g:inline&gt; tag inserts a Jelly file into your Jelly in the same context. This means that the inserted Jelly can access the variables you previously established and it can change the values of those variables.

```
<g:inline template="element_default.xml" />
```

### &lt;g:call&gt;

For better encapsulation, the &lt;g:call&gt; tag may be used. Your function will only have access to the values passed to it. The Jelly context will look the same after a call as before the call. This means you cannot set a global variable here and read it later. This also means you can't mistakenly set a global variable called "jvar\_temp" and overwrite a variable that somebody else was relying on.

Passing values, if needed, is done explicitly by including the name of the parameter on the &lt;g:call&gt; line followed by the equal sign followed by the value in quotes:

```
<g:call function="collapsing_image.xml" id="${jvar_section_id}" image="$[jvar_cimg]" 
   first_section_id="${jvar_first_section_id}" image_alt="${jvar_cimg_alt}"/>
```

If values are passed, and you want to have defaults or required parameters, your Jelly referenced in the function must then include a line to declare whether the parameters are required or have a default value:

```
<g:function id="REQUIRED" image="REQUIRED" image_prefix="" image_alt="REQUIRED"/>
```

The example above indicates that 3 of the parameter are required and one parameter is option with a blank default value. Note that if you are not passing values or if you do want to have default or required values, you do not need to include the &lt;g:function&gt; line at all. In general, however, you will want to include a &lt;g:function&gt; line.

The value can then be referenced in your template by prepending the "jvar\_" prefix to the parameter's name:

```
<img id="img.${jvar_id}" src="images/${jvar_image}" alt="${jvar_image_alt}" 
   onclick="toggleSectionDisplay('${jvar_id}', '${jvar_image_prefix}','${jvar_first_section_id}');"/>
```

For &lt;g:call&gt;, parameters may also be pass implicitly as a list of named variables in an "arguments" parameter:

```
 <g:call function="item_link_default.xml" arguments="sysparm_view,ref_parent,jvar_target_text"/>
```

As an alternative to passing variables into the function via separate tag arguments, it is possible to pass a list of variables in a single 'arguments' argument. All variables identified by name \(comma separated\) in the **argument** parameter are re-introduced within the function under the exact same name \(e.g. inside the function template, we'd have variables sysparm\_view, ref\_parent, and jvar\_target\_text available to us\).

The function template may return a value to the calling template using the `return=` attribute. Within the function the `jvar_answer` variable sets the return value.

```
<g:call function="item_body_cell_calc_style.xml" arguments="jvar_type" return="jvar_style"/>
```

## &lt;g:evaluate&gt;

The &lt;g:evaluate&gt; tag is used to evaluate an expression written in Rhino JavaScript and sometimes to set a variable to the value of the expression.

The last statement in the expression is the value the variable will contain.

```
<g2:evaluate var="jvar_page" jelly="true">
     var page = "";
     var pageTitle = "";
     var pageGR = new GlideRecord("cmn_schedule_page");
     pageGR.addQuery("type", jelly.jvar_type");
     pageGR.query();
     if (pageGR.next()) {
        page = pageGR.getValue("sys_id");
        pageTitle = pageGR.getDisplayValue();
     }
     page;
</g2:evaluate>
```

```
<g2:evaluate var="not_important" expression="sc_req_item.popCurrent()"/>
```

### object="true"

If you would like to have the evaluate return an object \(for example an array\), use the argument object="true".

```
<g2:evaluate object="true" var="jvar_items" expression="SncRelationships.getCMDBViews()" />
```

### jelly="true"

If you would like to access Jelly variables inside an evaluate, include jelly="true" in the evaulate and add "jelly." before the Jelly variable's name. For example, to access the GlideJellyContext:

```
<g2:evaluate var="jvar_row_no" jelly="true">
   var gf = jelly.context.getGlideForm();
   var row = gf.getRowNumber();
   row;
</g2:evaluate>
```

Another example of accessing a jvar using the jelly="true" parameter. The value of `jvar_h` was set previously and we can access it inside the `evaluate`:

```
$[NLBR:jvar_h.getHTMLValue('newvalue')]
<g2:evaluate var="jvar_fix_escaping" jelly="true">
    var auditValue = jelly.jvar_h.getHTMLValue('newvalue');
    gs.log("************ " + auditValue);
</g2:evaluate>
```

### copyToPhase2="true"

If you have a need to take the results of an evaluation that occurs in phase 1 and propagate it to phase 2, use copyToPhase2="true". There is some protection for escaping in this use. For example:

```
<g:evaluate var="jvar_has_special_inc" copyToPhase2="true">
   var specialInc = gs.tableExists("special_incident");
   specialInc;
</g:evaluate>
$[jvar_has_special_inc]
```

If you do not need to evaluate something, you can do this more directly. Beware of escaping issues here \(double quotes in jvar\_rows would cause a problem in the example\):

```
<j2:set var="jvar_rows" value="${jvar_rows}"/>
```

## &lt;g:breakpoint/&gt;

This tag can be used to display the current Jelly variables and their values in the log.

Be sure to remove this tag before going to production.

## &lt;g:ui\_form/&gt;

This tag defines a form on the UI page.

For example, if your form contained the `application_sys_id` field, the g:ui\_form might benefit from a processing script.

```
<g:ui_form>
    <p>Click OK to run the processing script.</p>
    <g:dialog_buttons_ok_cancel ok="return true" />
    <input type="hidden" name="application_sys_id" value="499836460a0a0b1700003e7ad950b5da"/>
 </g:ui_form>
```

For more information, see [UI macros](../../server-scripting/concept/c_UIMacros.md#).

## &lt;g:ui\_input\_field /&gt;

This tag adds a reference to a UI macro that creates an input field on a page that allows users to input information. The `ui_input_field` passes a label, name, value, and size into the UI macro.

Here is an example from a UI page:

```
<g:ui_input_field label="sys_id" name="sysid" value="9d385017c611228701d22104cc95c371" size="50"/>
```

For more information, see [UI macros](../../server-scripting/concept/c_UIMacros.md#).

## &lt;g:ui\_checkbox/&gt;

This tag puts a user-editable check mark on a page. The name and value are passed into the UI macro.

Here is an example from a table on a UI page:

```
<table>
    <tr>
      <td nowrap="true">
          <label>Time Card Active:</label>
      </td>
      <td>
          <g:ui_checkbox name="timecard_active" value="${sysparm_timecard_active}"/>
      </td>
   </tr>
</table>
```

For more information, see [UI macros](../../server-scripting/concept/c_UIMacros.md#).

## &lt;g:dialog\_buttons\_ok\_cancel/&gt;

This tag puts buttons on the UI page that run a specified processing script if the tag returns true.

If your UI page contains a form \(uses the &lt;g:form&gt; tag\), you can submit the form and have the Processing Script run. The Processing Script can naturally access fields on the form. For example, if your form contained the application\_sys\_id field:

```
<g:ui_form>
    <p>Click OK to run the processing script.</p>
    <g:dialog_buttons_ok_cancel ok="return true" />
    <input type="hidden" name="application_sys_id" value="499836460a0a0b1700003e7ad950b5da"/>
 </g:ui_form>
```

## &lt;g:ui\_reference/&gt;

This tag adds a reference to a page that can be referenced by a Processing Script.

The following example creates a reference defined by name, ID, and table parameters in the tag:

```
<g:ui_reference name="QUERY:active=true^roles=itil" id="assigned_to" table="sys_user" />
```

Then in the Processing Script, reference the name field like this:

```
newTask.assigned_to = request.getParameter("QUERY:active=true^roles=itil");
```

You can specify a reference qualifier, so that the "name" attribute can be unique. The following example creates a reference defined by name, ID, and table parameters in the tag.

**Note:** The "columns" attribute only applies to the auto-completer.

```
<g:ui_reference name="parent_id" id="parent_id" table="pm_project" query="active=true" completer="AJAXTableCompleter" 
columns="project_manager;short_description"/>
```

## Ampersand

Ampersands in Jelly can cause you grief because Jelly is XML.

Use `${AMP}` to insert an ampersand in Jelly. If you are writing JavaScript that appears in the HTML part of say a UI page or UI macro that is actually going to run on the browser you are better off putting this code in the "client script" field and that way you can avoid escaping issues. However, if you really must put it in the "HTML" field, you will need to do something like this:

```
ta = ta[1].split('$[AMP]');
```

## And

Use `${AND}` to insert a JavaScript and in Jelly.

For example:

```
if (d ${AND} e)
   var color = d.value;
```

Alternately, in a Jelly test you would use `&amp&amp`. For example:

```
<j:if test="${jvar_form_name == 'sys_form_template' &amp;&amp; !RP.isDialog()}">
```

## Less than

Similar to ampersands, less than \("&lt;"\) signs can also cause problems due to Jelly being XML. This can be resolved by reversing your test such that it is not necessary or by using `${AMP}lt;` in place of the less than sign.

```
<g2:evaluate var="jvar_text">
     var days = "";
     var selectedDays = '$[${ref}]';
     for (var i = 1; i ${AMP}lt;= 7; i++) {
        if (selectedDays.indexOf(i.toString()) >= 0) {
           days += gs.getMessage("dow" + i);
           days += " ";
        }
     }
     days;
 </g2:evaluate>
```

Many times you can avoid the "less than" operator all together by just using "not equals" which doesn't have escaping issues. For example:

```
for (var i=0; i != ta.length; i++) {
}
```

## Whitespace

Normally, white space is removed by Jelly. To keep it, you must specify that it not be trimmed.

For example, the following keeps the space after the colon.

```
<j2:whitespace trim="false">${gs.getMessage('Did you mean')}: </j2:whitespace>
```

## Spaces

To encode a non-breaking space \(&amp;nbsp;\), you can use `$[SP]`.

For example:

```
<span id="gsft_domain" style="display: inline">
    ${gs.getMessage('Domain')}:$[SP]
    <span id="domainDD" class="drop_down_element" style="text-decoration: none; color: white">
        ${gs.getMessage("Loading...")}
   </span>
</span>
```

## Tracing Jelly

ServiceNow has a feature that allows the evaluation of Jelly to be traced.

The trace is sent to the log. This should only be turned on during debugging as this produces a lot of logging. To turn on the trace, set the property glide.ui.template.trace to true. For example, the following script can be executed to do this:

```
GlideProperties.set ( 'glide.ui.template.trace' , true ) ;
```

If you want to see your log entries on your web browser at the bottom of each page, navigate to **System Diagnostics** &gt; **Debug Log**.

