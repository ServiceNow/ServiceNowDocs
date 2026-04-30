---
title: UI pages
description: UI pages can be used to create and display forms, dialogs, lists, and other UI components.Each UI page has a URL computed from the application scope, page name, and the .do file extension.See access controls directly from the UI Page form and add role-based access control when creating or editing a UI Page record.Access controls and related security messages are integrated on high risk UI Pages for increased security.If your UI page contains a form \(uses the &lt;g:form&gt; tag\), you can submit the form and have the process script run.
locale: en-US
release: zurich
product: Scripts
classification: scripts
topic_type: reference
last_updated: "2026-03-26"
reading_time_minutes: 7
breadcrumb: [Creating UI pages and macros, Scripting, API implementation, API implementation and reference]
---

# UI pages

UI pages can be used to create and display forms, dialogs, lists, and other UI components.

Use UI pages as widgets on dashboards. To find the UI pages, navigate to **System UI** &gt; **UI Pages**.

This functionality requires a knowledge of HTML or Jelly. You can also create simple AngularJS applications using UI pages.

The UI page form contains the following fields:

<table id="table_lxj_31h_y4"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name used to invoke the page via a URL \(must not contain spaces\).

</td></tr><tr><td>

Application

</td><td>

Displays the current application scope.

</td></tr><tr><td>

Description

</td><td>

The description of the UI page and what it’s used for.

</td></tr><tr><td>

Direct

</td><td>

Select this check box for a direct UI page \[sys\_ui\_page\]. A direct UI page doesn't include the common HTML, CSS, and scripts. This setting requires adding custom CSS and JavaScript to use in the page.

</td></tr><tr><td>

HTML

</td><td>

Main component of the page where you define what is rendered when the page is shown. It can contain either static XHTML, dynamically generated content defined as Jelly, or call script includes and UI Macros.**Note:** If GlideRecord/GlideDBQuery is used instead of GlideRecordSecure, a security recommendation message displays.

</td></tr><tr><td>

Client Script

</td><td>

Include client-side JavaScript that runs in the browser, such as functions called by buttons. It’s intended to handle any client-side processing needed, like setting focus to a field or other interactive DHTML features after a page is loaded. Client scripts for the UI page are deployed to the browser within a `<script/>` tag, so the content can similarly be defined within the HTML field. The Client Script field can be used instead to define these scripts concisely to maintain the Jelly and HTML manageability.

</td></tr><tr><td>

Processing Script

</td><td>

Script that runs on the server when the page is submitted. This is useful if your page has a form defined with the &lt;`g:ui_form/`&gt; or &lt;`g:form/`&gt; tags.**Note:** If GlideRecord/GlideDBQuery is used instead of GlideRecordSecure, a security recommendation message displays.

</td></tr><tr><td>

obsolete-custom-processors

</td><td>

**Note:** This feature is deprecated. While legacy, existing custom processors continue to be supported, creating new custom processors has been deprecated. Instead, use the [Scripted REST APIs](../../../integrate/custom-web-services/concept/c_CustomWebServices.md).

</td></tr><tr><td colspan="2">

Related lists on the form view:

</td></tr><tr><td>

Access Controls

</td><td>

View and configure access controls for the UI page. See [Use access controls on UI pages](r_UIPages.md#) for more information.

</td></tr><tr><td>

Versions

</td><td>

Shows all versions of the UI page. Use this list to compare versions or to revert to a previous version.

</td></tr></tbody>
</table>## Access control

You can secure a UI page by creating an ACL with the following parameters:

-   **Type**: `ui_page`
-   **Operation**: `read`
-   **Name**: Name of the UI page to protect
-   **Role**: User role that is allowed to access the record

When saving a new UI page, you are prompted to assign a role for access control.

**Note:** An entry with the same name as the UI page is created in the Access Control table.

For details on creating an ACL rule, see [Create an ACL rule](https://www.servicenow.com/docs/access?context=t_CreateAnACLRule&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

## High risk UI pages

UI pages are considered high risk with any of the following attributes:

-   Uses GlideRecord or GlideDBQuery instead of GlideRecordSecure.

    **Note:** This is applicable for HTML and Processing script fields and not Client scripts.

-   Doesn't have a corresponding ACL configured.
-   Indicates to be a public UI page and is entered in the sys\_public record.
-   Shows a message to indicate high risk UI page.
-   For instances with glide.installation.developer is set to **true**.
-   If resource is customized content for a customer instance.

**Parent Topic:**[Creating custom UI Pages and UI macros](../../general-scripting/concept/create-custom-ui-pages.md)

## UI page access

Each UI page has a URL computed from the application scope, page name, and the `.do` file extension.

For example, to display the page called glidewindow\_example on the demo system, you would navigate to `https://<instance name>.service-now.com/glidewindow_example.do`. If the page was part of a custom application called example\_app, you would instead navigate to `https://<instance name>.service-now.com/x_example_app_glidewindow_example.do`.

You can also add additional parameters to a URL that can be accessed within a page's HTML section as jelly variables. That is, appending arguments to the URL as follows: `/my_test_page.do?sysparm_verbose=true` creates jelly variables called **verbose** that can be accessed as follows:

```
<j2:if test="$[!empty(sysparm_verbose)]"> <span>show extra stuff </span> </j2:if >
```

A common practical example of this might be retrieving a database record for display. To build a list of a user's roles, pass in a parameter with the user's sys\_id. Invoke the following UI page to display a list of roles for that user with Jelly code:

`role_select.do?sysparm_user=5137153cc611227c000bbd1bd8cd2007`

```
<j:set var = "jvar_user_id" value = "${sysparm_user}" />
 
  <g:evaluate> var userRoles = new GlideRecord('sys_user_has_role');
    userRoles.addQuery('user','${jvar_user_id}');
    userRoles.query(); 
  </g:evaluate>
 
  <select id='select_role'> 
      <j:while test = "${userRoles.next()}"> 
          <option value = "${userRoles.sys_id}"> ${userRoles.role.name} </option> 
      </j:while> 
  </select>
```

An exception to be careful of, though, is the reserved variable name sys\_id. This variable always contains the ID of the UI page itself, regardless of what is specified in the URL. A common substitute variable name is sysparm\_id.

Do not use URL parameters to load client scripts in UI pages. The system no longer evaluates scripts that are passed by URL parameter. If your implementation depends on this behavior, you can [add the system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=zurich&pubname=zurich-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US) \[glide.security.disable\_ui\_pages\_sysparm\_client\_script\] and set it to **false** to temporarily allow the evaluation of URL parameters passing scripts in UI pages.

## Use access controls on UI pages

See access controls directly from the UI Page form and add role-based access control when creating or editing a UI Page record.

### Before you begin

Access controls that have been added to an existing UI page can be accessed and edited by opening the UI page record under related links.

Role required: security\_admin and admin

### Procedure

1.  Elevate to the **security\_admin** role.

    For details on role elevation, see [Elevate to a privileged role](https://www.servicenow.com/docs/access?context=t_ElevateToAPrivilegedRole&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

2.  Navigate to **All** &gt; **System UI** &gt; **UI Pages**.

3.  Select **New**.

4.  Complete the form.

    See [UI pages](r_UIPages.md#) for additional information for UI field descriptions.

5.  Select **Submit** or **Save**.

    A modal displays prompting you to create a role-based access control for the UI page.

6.  Select a role.

7.  Select **OK** to assign the role.

    You are returned to the UI pages list.

8.  Add, edit, or view access controls for an existing UI page:
9.  Open a UI page from the UI pages table.

10. View the **Access Controls** under the related lists.

11. Select **New** to create a new access control or select an existing entry for editing.

    The Access Control form loads. UI Page details are displayed.

12. Complete the form and assign a role to the UI page.

    For additional information on access control, see [Create an ACL rule](https://www.servicenow.com/docs/access?context=t_CreateAnACLRule&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

13. Select **Submit** for a new access control or **Update** for edits.

    **Note:** There can be multiple access controls per UI page.


### Secure UI pages

Access controls and related security messages are integrated on high risk UI Pages for increased security.

An informational message displays on high risk UI pages to inform the customer to add a role-based Access Control to the UI page.

![UI page security recommendation messages.](../image/new-ui-html-processing-errors.png)

The message displays under the following conditions:

-   If an ACL \(access control list\) is missing
-   If GlideRecord/GlideDBQuery is used instead of GlideRecordSecure in either the **HTML** or **Processing script** fields.
-   If the UI page is configured as public in sys\_public

    **Note:** Public UI Pages that are public or that use GlideRecord don’t show a missing ACL warning.


See [UI pages](r_UIPages.md#) for details on high risk UI pages.

#### Conditions that display the security recommendations message

The message displays under the following conditions:

-   All internal instances eclipse/IJ where glide.installation.developer=true.
-   All customer scoped UI Page resources.
-   Any customized UI Page when the **glide.script.ui\_page.customer\_scoped.security\_msgs\_enabled** property is set to true. \(The default value is true\).

#### Conditions that don’t display the security recommendations message

The message won’t display under the following conditions:

-   UI Page is public.
-   UI Page is in the **Global** scope.
-   The **glide.script.ui\_page.customer\_scoped.security\_msgs\_enabled** is set to false.

**Note:** To disable the role-based ACL creation prompt, set the **glide.ui\_page.enable\_acl\_create\_ux** property to **false**. The property is set to **true** by default.

## UI page process scripts

If your UI page contains a form \(uses the *&lt;g:form&gt;* tag\), you can submit the form and have the process script run.

The processing script can naturally access fields on the form. For example, if your form contained the *application\_sys\_id* field:

```
<g:ui_form>
  <p>Click OK to run the processing script.</p>
  <g:dialog_buttons_ok_cancel ok="return true" />
  <input type="hidden" name="application_sys_id" value="499836460a0a0b1700003e7ad950b5da" />
</g:ui_form>
```

You can access the field using *application\_sys\_id*:

```
var application = new GlideRecord('hr_application');
 application.get(application_sys_id);
 application.status = "Rejected";
 application.update();
 var urlOnStack = GlideSession.get().getStack().bottom();
 response.sendRedirect(urlOnStack);
```

**Important:** The preceding script is usable only with Global applications.

If you are using the UI page for a dialog, you can also reference the most recent URL on the stack using the code above and then send the response to that location. This is useful if you want to have the dialog's processing script update something and then redisplay the screen that brought up the dialog.

