---
title: PolarisUI - Scoped
description: The PolarisUI API provides methods for enabling Next Experience on direct UI pages.Checks if the current page can use the Next Experience UI.Returns a list of CSS class names used by the Next Experience UI.Checks if the Next Experience UI is enabled for the current user.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# PolarisUI- Scoped

The PolarisUI API provides methods for enabling Next Experience on direct UI pages.

A UI page \[sys\_ui\_page\] is direct if the **Direct** field is **Selected**. A direct UI page doesn't include the common HTML page template and must include all CSS and JavaScript that you want to use in the page.

All non-direct UI pages use Next Experience by default.

For more information about Next Experience, see [the Next Experience UI](https://www.servicenow.com/docs/access?context=next-experience-landing-page&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

The PolarisUI API is provided within the `sn_ui` namespace.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## PolarisUI - canUsePolarisCSS\(\)

Checks if the current page can use the Next Experience UI.

This method returns `true` if all of the following conditions are met.

-   sn\_ui.PolarisUI.isEnabled\(\) is `true`.
-   The request URL parameter **sysparm\_use\_polaris** is not set to `false`.
-   The referrer HTTP request header does not contain `sysparm_use_polaris=false`.
-   The page or its parent plugin are not denied use of Next Experience by a record in the Page Theme Support \[sys\_page\_theme\] table.

Use this method to conditionally change behavior or [jelly](https://www.servicenow.com/docs/access?context=r_JellyTags&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US) output if Next Experience is enabled.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_wzz_nkq_prb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the current page can use the Next Experience UI.

 Valid values:

-   true: The current page can use the Next Experience UI.
-   false: The current page can't use the Next Experience UI.

</td></tr></tbody>
</table>This UI Action redirects to a different page if Next Experience is running on the current form.

```
var id = current.getUniqueValue();
if (sn_ui.PolarisUI.canUsePolarisCSS())
	action.setRedirectUrl("/now/custom/application/record/" + id);
return "/record.do?sys_id=" + id;

```

This jelly script sets a different style sheet for pages using Next Experience.

```
<g:evaluate var="jvar_css_path">
	// Core UI content css record
	var id = "5e8fde63d713310074304187ed61030d";

	if (sn_ui.PolarisUI.canUsePolarisCSS())
		id = "84f03cc87120a00cfab6dd207cb0b72";
	
	"/" + id + ".cssdbx";
</g:evaluate>
<link href="${jvar_css_path}" rel="stylesheet" type="text/css" />

```

## PolarisUI - getBodyClassNames\(\)

Returns a list of CSS class names used by the Next Experience UI.

Use this method in the HTML `<body>` tag of a UI page to set the CSS classes required for Next Experience to render correctly.

```
<body class="$[sn_ui.PolarisUI.getBodyClassNames()]">
```

The returned class names change depending on system properties and if session debug output exists.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|List of CSS class names used by the Next Experience UI.|

This jelly script adds Next Experience to a custom UI page.

```
<?xml version="1.0" encoding="utf-8" ?>
<j:jelly trim="true" xmlns:j="jelly:core" xmlns:g="glide" xmlns:g2="null">
    <g2:doctype name="html" />
    <g:inline template="dir_checker.xml"/>
    <html class="${jvar_text_direction}" lang="$[gs.getSession().getLanguage()]">
        <head>
            <g:inline template="set_theme_vars.xml" /> <!-- sets jvar_theme and jvar_css_cache_key -->
            <g:requires name="styles/css_includes_my_app.css" includes="true" params="$[jvar_css_cache_key]" /> 
            <g:if_polaris>
	<g:then><g:inline template="polarisberg_output.xml"/></g:when>
	<g:else><g:inline template="heisenberg_output.xml" type="css"/></g:else>
             </g:if_polaris>
        </head>
        <body class="$[sn_ui.PolarisUI.getBodyClassNames()]">
            Your UI page content here
        </body>
    </html>
</j:jelly>
```

## PolarisUI - isEnabled\(\)

Checks if the Next Experience UI is enabled for the current user.

This method checks if the **glide.ui.polaris.experience** system property and **glide.ui.polaris.use** user preference are both set to **true**.

-   **glide.ui.polaris.experience** enables Next Experience on the instance.
-   **glide.ui.polaris.use** disables Next Experience for specified users when set to **false**.

For more information about Next Experience system properties and user preferences, see [Next Experience system properties](https://www.servicenow.com/docs/access?context=pol-sys-properties&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

**Note:** This method returns true even if Next Experience is disabled for the current page. This method is useful for conditionally enabling entire experiences or redirecting to different pages when Next Experience is enabled globally.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_mjc_djq_prb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the Next Experience UI is enabled for the current user.

 Valid values:

-   true: The Next Experience UI is enabled for the current user.
-   false: The Next Experience UI isn't enabled for the current user.

</td></tr></tbody>
</table>This UI page displays a conditional message to the user if Next Experience is enabled for the current user.

```
<j:if test="${sn_ui.PolarisUI.isEnabled()}">
	<a href="...">Click here to learn more about the new UI changes</a>
</j:if>
```

This business rule shows an info message on record display that a user can click to view the record in Core UI instead of Next Experience. The business rule **Condition** field is set to `!current.isNewRecord() && sn_ui.PolarisUI.isEnabled() && sn_ui.PolarisUI.canUsePolarisCSS()`.

```
// business rule script field

(function executeRule(current, previous /*null when async*/) {

	var sysId = current.getUniqueValue();
	gs.addInfoMessage("<a href='/incident.do?sys_id="+ sysId +"&sysparm_use_polaris=false'>Click here to load this page in Core UI</a>");

})(current, previous);

```

