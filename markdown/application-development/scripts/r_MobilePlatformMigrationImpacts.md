---
title: Mobile client GlideForm \(g form\) scripting and migration
description: Client scripting for mobile is identical to scripting for the web, with some exceptions. All new scripts must conform to certain guidelines. The following items are affected on the mobile platform: client scripts, UI policies, navigator modules, and UI actions.
locale: en-US
release: xanadu
product: Scripts
classification: scripts
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Client-side scripting, Scripting, Building pro-code applications, Developing your application, Building applications]
---

# Mobile client GlideForm \(g form\) scripting and migration

Client scripting for mobile is identical to scripting for the web, with some exceptions. All new scripts must conform to certain guidelines. The following items are affected on the mobile platform: client scripts, UI policies, navigator modules, and UI actions.

## Client scripts

For new or existing scripts to be valid for mobile, they must conform to the following requirements:

-   Use the new mobile methods in place of g\_form.getControl\(\).
-   Do not use deprecated methods.
-   Do not reference unsupported browser objects.
-   Do not make synchronous JavaScript, GlideAjax, and GlideRecord calls.
-   Do not call methods that are not available for mobile.
-   Enable scripts to run on the mobile UI.

<table id="table_Requirements"><tbody><tr><td>

Use the new mobile methods

</td><td>

Several new methods are available for modifying form fields instead of directly manipulating the HTML. These methods replace previous usages of g\_form.getControl\(\), which is deprecated for the mobile platform. In your existing scripts, ensure that the new methods are used in place of methods that are not valid on the mobile platform. For information on these new methods, refer to [Mobile GlideForm\(\) API](https://www.servicenow.com/docs/access?context=c_MobileGlideForm_API&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US).

</td></tr><tr><td>

Do not use deprecated methods

</td><td>

The following methods have been deprecated for the mobile platform because direct access to HTML elements is not allowed:

 -   g\_form.getControl\(\)
-   g\_form.getFormElement\(\)
-   g\_form.getElement\(\)

 To ensure that existing scripts are compatible, remove all calls to deprecated methods from your code. For new scripts, do not use deprecated methods if you want the script to be valid for mobile.

 For g\_form.getControl\(\), some of the functionality previously included with this method has been extracted to individual methods. Instead of g\_form.getControl\(\), use the new methods described on the developer site.

</td></tr><tr><td>

Do not reference unsupported browser objects

</td><td>

The following browser objects are not supported in mobile scripts:

 -   Window
-   jQuery or Prototype \($, $j, or $$\)
-   Document

 Make sure that new scripts do not use these objects, and remove any usage of these objects from your existing scripts. Use GlideForm \(g\_form\) instead, which provides methods such as setLabel\(\), addDecoration\(\), and hasField\(\) for accomplishing the same tasks.

</td></tr><tr><td>

Do not make synchronous JavaScript calls

</td><td>

The mobile platform does not allow synchronous JavaScript calls. The g\_form.getReference\(\) method must now have the callback parameter defined. For example:

 ```
 g_form.getReference(fieldName, callback)
```

 Be sure that all g\_form.getReference\(\) calls include the callback parameter. For example, the following script does not include a callback and is incompatible with the mobile platform:

 ```
 var userName = g_form.getReference('assigned_to').user_name;
 g_form.setValue('u_assigned_user_name', userName);
```

 The following script has been updated to include the callback and is compatible with the mobile platform:

 ```
 g_form.getReference('assigned_to', function(now_GR) {
     g_form.setValue('u_assigned_user_name', gr.user_name);
 });
```

</td></tr><tr><td>

Do not make synchronous Ajax calls

</td><td>

The mobile platform does not allow synchronous GlideAjax calls. Any use of getXMLWait\(\) in a GlideAjax call will not work on the mobile platform. Be sure that all GlideAjax calls are asynchronous. For more on synchronous versus asynchronous GlideAjax calls and getXMLWait\(\), see [AJAX](../../ajax/topic/p_AJAX.md#). For information on the available GlideAjax methods, refer to the [GlideAjax API](https://www.servicenow.com/docs/access?context=c_GlideAjaxAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US).

</td></tr><tr><td>

Do not make synchronous GlideRecord calls

</td><td>

The mobile platform does not allow synchronous [GlideRecord](https://www.servicenow.com/docs/access?context=c_GlideRecordScopedAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US) calls. Make sure that any existing GlideRecord calls include a callback. For example, the following script does not include a callback and is incompatible with the mobile platform:

 ```
 var now_GR = new GlideRecord('incident');
 gr.addQuery('number', g_form.getValue('related_incident'));
 gr.query();
 gr.next();
 g_form.setValue('u_related_incident_description', gr.short_description);
```

 The following script has been updated to include the callback, and is compatible with the mobile platform:

 ```
 var now_GR = new GlideRecord('incident');
 gr.addQuery('number', g_form.getValue('related_incident'));
 gr.query(function(now_GR) {
     gr.next();
     g_form.setValue('u_related_incident_description', gr.short_description);
 });
```

</td></tr><tr><td>

Do not use methods unavailable on the mobile platform

</td><td>

Due to the limitations and reduced functionality that is imposed by the mobile platform, the following methods are not deprecated but are not available on the mobile platform. If these run on the mobile platform, no action occurs:

-   showRelatedList \(\)
-   hideRelatedList \(\)
-   showRelatedLists \(\)
-   hideRelatedLists\(\)
-   flash\(\)
-   getSections\(\)
-   enableAttachments\(\)
-   disableAttachments\(\)
-   setReadonly\(\) \(Note that setReadOnly\(\) is available\)
-   getParameter\(\)

</td></tr><tr><td>

Enable scripts for mobile

</td><td>

Scripts must be enabled for the mobile platform.

</td></tr></tbody>
</table>**Note:** Focusing an element on a mobile form is not supported.

## UI policies

Use the **Run scripts in UI type** field to determine whether scripts run on the mobile platform, the desktop, or both. Update existing policies so that they apply to either the mobile platform or both. For new scripts, also ensure that the mobile option or both is selected.

## Navigator modules

For existing code, modules must be transferred to either the sys\_ui\_application or sys\_ui\_module tables to be available on the mobile platform. When developing new code, be sure that all modules are created in the sys\_ui\_application or sys\_ui\_module tables.

## UI actions

UI actions must be transferred to the sys\_ui\_ng\_action table to appear on the mobile platform. UI action scripts that do not use deprecated methods do not require changes to the script itself. For new UI actions, be sure that they are created in the sys\_ui\_ng\_action table.

**Parent Topic:**[Client-side scripting](../concept/client-side-scripting-overview.md)

