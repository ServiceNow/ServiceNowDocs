---
title: Application Navigator category
description: Verify the functionality of menus and modules in the application navigator.Verifies the visibility, or lack thereof, of selected application menus in the application navigator \(left navigation bar\). For example, you create a test that first impersonates a user, then verifies that specified application menus \(such as Self-Service and Reports\) are visible, or are not visible, to that user.Application menus define the main content that users can access in the application navigator. You can configure which applications appear in the application navigator.Modules are the children, or the second tier navigation options to the applications in the application navigator. Modules often link to other pages or records in the platform. You can configure which modules appear in the application navigator using Application Menus module.The Link type field on the Module form specifies what type of link the module opens.Clicking a module name in the navigation pane executes a URI that opens the module's page in the content pane. All the characters in module URIs must be URL-encoded or the link breaks.Verify the visibility, or lack thereof, of selected modules in the application navigator \(left navigation bar\). For example, create a test that first impersonates a user, then verifies that specified modules \(such as Homepage and My Requests\) are visible, or are not visible, to that user.Open a module from the application navigator, as if a user had clicked it. The module must be visible to the currently executing user to navigate to it.
locale: en-US
release: australia
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 15
breadcrumb: [Automated Test Framework \(ATF\) test step categories, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Application Navigator category

Verify the functionality of menus and modules in the application navigator.

## Application Menu Visibility

Verifies the visibility, or lack thereof, of selected application menus in the application navigator \(left navigation bar\). For example, you create a test that first impersonates a user, then verifies that specified application menus \(such as Self-Service and Reports\) are visible, or are not visible, to that user.

<table id="table_knc_vgs_mcb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Execution order

</td><td id="atf-exec-order">

Integer specifying the order in which the test executes this step.As you create steps, the system automatically assigns each step an incremental value. This value causes the test to execute steps in the order that you created them in. You can change this default order by editing the **Execution order** values.

</td></tr><tr><td>

Active

</td><td id="atf-active">

Option to activate this test step for use.

</td></tr><tr><td>

Application

</td><td id="application-scope-suite">

The application scope in which the system runs this test or test suite.

</td></tr><tr><td>

Test

</td><td id="atf-test">

Read-only name of the test that you're adding the step to.

</td></tr><tr><td>

Step config

</td><td id="atf-step-config">

Read-only name of the step.

</td></tr><tr><td>

Description

</td><td id="atf-description">

Description of the test step. This field value is automatically set based on the field values of the test step. This field appears after the test step is submitted.

</td></tr><tr><td>

Notes

</td><td id="atf-notes">

Notes about the test step.

</td></tr><tr><td>

Navigator

</td><td id="atf-navigator">

Navigator version to assert against-   Core UI \(UI16\): If you are creating new steps, you will have Core UI by default.
-   Next Experience: If you have Next Experience enabled, Next Experience is the default navigator. If it is disabled, Core UI is the default navigator.

</td></tr><tr><td>

Visible assert type

</td><td id="atf-visible-assert-type">

Specifies how application menus selected in the **Visible application menus** field should be tested for visibility in the application navigator.-   **At least these application menus are visible**: At minimum, all the selected application menus are visible in the application navigator.
-   **Only these application menus are visible**: Only the selected application menus are visible in the application navigator.

</td></tr><tr><td>

Visible application menus

</td><td id="atf-visible-application-menus">

Application menus whose visibility in the application navigator is being verified.

</td></tr><tr><td>

Not visible assert type

</td><td id="atf-not-visible-assert-type">

Specifies how application menus selected in the **Not visible application menus** field should be tested for lack of visibility in the application navigator.-   **At least these application menus are not visible**: At minimum, all the selected application menus are not visible in the application navigator.
-   **Only these application menus are not visible**: Only the selected application menus are not visible in the application navigator.

</td></tr><tr><td>

Not visible application menus

</td><td id="atf-not-visible-application-menus">

Application menus whose lack of visibility in the application navigator is being verified.

</td></tr></tbody>
</table>**Related topics**  


[Create an application menu](test-steps-app-navigator-category.md#)

## Create an application menu

Application menus define the main content that users can access in the application navigator. You can configure which applications appear in the application navigator.

### Before you begin

Role required: admin

### About this task

When creating an application menu, consider grouping like modules into a consolidated application menu. When editing an existing menu, add more useful modules to the application menu, and remove unneeded ones.

### Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Application Menus**.

2.  Click **New**.

3.  Complete the form.

    |Field|Description|
    |-----|-----------|
    |Title|Defines the display name of the application menu.|
    |Roles|Restricts access to the specified roles. All users can view the application menu when it is active.|
    |Category|Specifies the menu category that defines the navigation menu style \(default value is **Custom Applications**\).|
    |Hint|Defines the text that appears in a tooltip when a user points to this application menu.|
    |Active|Select the check box to activate the application menu. Only active application menus appear in the application navigator.|
    |Description|Provide a more detailed explanation of what this application does.|
    |Other fields|
    |Order|Defines the relative position of the application menu in the application navigator. If you do not specify an order, the default order of the menu category is used.|
    |Default device type|This field is not used. You can define application menus for mobile devices in a separate table.|

    **Note:** You may need to [configure the form](https://www.servicenow.com/docs/access?context=configure-form-layout&version=australia&pubname=australia-platform-administration&ft:locale=en-US) to see all fields.

4.  Click **Submit**.

5.  [Create modules](test-steps-app-navigator-category.md#) to appear in the application menu.

    Only application menus that contain modules appear in the application navigator.


## Create a module

Modules are the children, or the second tier navigation options to the applications in the application navigator. Modules often link to other pages or records in the platform. You can configure which modules appear in the application navigator using Application Menus module.

Watch this five-minute video to learn about adding application menus and modules to the application navigator.Shows how to add application menus and modules to the application navigator.

### Before you begin

Role required: admin

### Procedure

1.  Open the application menu record using one of the following methods.

    -   Navigate to **System Definition** &gt; **Application Menus** and select the application menu from the list.
    -   Point to the application menu and click the edit application \(pencil\) icon.


2.  Scroll down to the **Modules** related list and click **New**.

3.  Define the module by completing the fields on the Module form.

<table id="table_bns_lpx_xhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title

</td><td>

Defines the module name. Choose a title that clearly identifies the module.

</td></tr><tr><td>

Application menu

</td><td>

Specifies the name of the application menu under which the module appears.

</td></tr><tr><td>

Hint

</td><td>

Defines the tooltip that appears when a user points to the module name.**Note:** Module Hints are deprecated in Core UI

</td></tr><tr><td>

Order

</td><td>

The order in which the module displays relative to other modules.

</td></tr></tbody>
</table>4.  On the **Visibility** tab, complete the fields.

    |Field|Description|
    |-----|-----------|
    |Roles|Restricts module access to the specified roles. If this field is left blank, the module is visible to all users who have access to the application menu.|
    |Active|Defines whether the module appears in the application navigator.|
    |Override application menu roles|Allows users to access this module even if they do not have permission to view the containing application menu. Users must still meet the role requirements for this module.|

5.  On the **List Type** tab, complete the fields.

    The fields displayed depend on the **Link type** you choose. All module URIs must be encoded. If you supply arguments to the module URI, either you or ServiceNow. For more information about encoding module URIs, see [Encoding module URIs](test-steps-app-navigator-category.md#).

<table id="table_rh5_vrx_xhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Link type

</td><td>

Specifies what type of link this module opens. You must specify additional information based on the link type. See [Module link types](test-steps-app-navigator-category.md#).

</td></tr><tr><td>

Table

</td><td>

Specifies the table used by the module.**Note:** The list shows only tables and database views that are in the same scope as the module.

</td></tr><tr><td>

Filter

</td><td>

Conditions for the items presented in the module, for example, **Active is true**.

</td></tr><tr><td>

Argument

</td><td>

String appended to the URI to create the module URI. Can be a sysparm\_query. These values must be encoded either by you or ServiceNow. For more information about encoding module URIs, see [Encoding module URIs](test-steps-app-navigator-category.md#).

</td></tr><tr><td>

Order

</td><td>

Specifies the order in which the modules appear under the application.

</td></tr></tbody>
</table>
### Module link types

The **Link type** field on the Module form specifies what type of link the module opens.

<table id="table_g1m_jdq_p4"><thead><tr><th>

Link Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Assessment

</td><td>

Links to the assessment-based survey you select in the **Assessment** reference field. See [Create a survey module](https://www.servicenow.com/docs/access?context=t_CreatingASurveyModule&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

Content Page

</td><td>

Displays the content page you select in the **Content page** reference field. See [Create a content page](https://www.servicenow.com/docs/access?context=t_CreateAContentPage&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

</td></tr><tr><td>

Documentation Link

</td><td>

Links to a documentation page and opens in a new tab or window. This link type is used with embedded metadata in documentation topics. To open an internal document from a module, use the **URL \(from Arguments\)** module link type.

</td></tr><tr><td>

Homepage

</td><td>

Displays the homepage you select in the **Homepage** reference field.

</td></tr><tr><td>

HTML \(from Arguments\)

</td><td>

Places HTML in the application navigator. This link type is used for more complicated links, where a flat URL is not customizable enough.**Note:**

-   The **HTML \(from Arguments\)** link type is supported in the legacy UI15 and UI11 interfaces only. In Core UI, use the **URL \(from Arguments\)** link type instead.
-   Enter a value for the **Arguments** field.

</td></tr><tr><td>

List Filter

</td><td>

Displays an unpopulated list view for the table you select in the **Table** field. Allows users to specify a filter without loading the list first. Use the **Filter** field to define the default filter for the list. Use the **View name** field to specify a [View management](https://www.servicenow.com/docs/access?context=view-management-overview&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

</td></tr><tr><td>

List of Records

</td><td>

Displays the list view for the table you select in the **Table** field. Use the **Filter** field to define the default filter for the list. Use the **View name** field to specify a view.

</td></tr><tr><td>

Map Page

</td><td>

Displays the map page you select in the **Map page** reference field.

</td></tr><tr><td>

New Record

</td><td>

Displays a form for creating a record in the table you select in the **Table** field.-   Use the **View name** field to specify a view.
-   Use the **Arguments** field to apply a template. See [Create a module for a template](https://www.servicenow.com/docs/access?context=t_CreateAModuleForATemplate&version=australia&pubname=australia-platform-administration&ft:locale=en-US) .

</td></tr><tr><td>

Run a Report

</td><td>

Runs the saved report you select in the **Report** field.

</td></tr><tr><td>

Script \(from Arguments\)

</td><td>

Runs a script, as defined in the **Arguments** field.**Note:** Enter a value for the **Arguments** field.

</td></tr><tr><td>

Search Screen

</td><td>

Link that displays a blank form for searching records in the table. Use the **View name** field to specify a view.**Note:** Use the parameter **&amp;sysparm\_result\_view=view\_name** to define the view the results are rendered in.

All searches use a **\[starts with\]** query to search for matching text. Other query types are not supported in search screens.

</td></tr><tr><td>

Separator

</td><td>

Creates a division between modules. Enter a name in the **Title** field to add a section name that users can collapse or expand.

</td></tr><tr><td>

Single Record

</td><td>

Displays a form for a single record on the table. Use the **View name** field to specify a view.

</td></tr><tr><td>

Survey

</td><td>

Links to the legacy survey you select in the **Survey** reference field. Use the **Survey overwrite** check box to determine whether the survey can be taken multiple times. **Note:** The **Survey** link type is for use with legacy surveys only, which assessment-based surveys replace. Select the **Assessment** link type to link the module to an assessment-based survey.

</td></tr><tr><td>

Timeline Page

</td><td>

Displays the timeline page you select in the **Timeline Page** reference field. See [Timeline pages](https://www.servicenow.com/docs/access?context=c_TimelinePages&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

URL \(from Arguments\)

</td><td>

Opens any URL, as defined in the **Arguments** field.\[Optional\] Use the **Window name** field to define a link that opens in a new window.

 **Note:**

-   For internal links, always use a relative link such as `./catalog_home.do?sysparm_view=catalog_default` or `catalog_home.do?sysparm_view=catalog_default`. Do not use an absolute link to a ServiceNow instance. It creates problems when you move an update set from a development instance to a production instance because the URL still references the development instance.
-   Enter a value for the **Arguments** field.

</td></tr></tbody>
</table>### Encoding module URIs

Clicking a module name in the navigation pane executes a URI that opens the module's page in the content pane. All the characters in module URIs must be URL-encoded or the link breaks.

**Note:** If you're upgrading to the New York release or later from a pre-New-York release, your module UIs may break if they do not follow the conventions presented in this topic.

When you create modules, you have the option of adding arguments and filter conditions that sort and/or reduce the number of results displayed in the content pane. When you click a module name in **System Definitions** &gt; **Application Definitions**, you can see those conditions and arguments on the **Link Type** tab.

![Link type tab](../../navigation-and-ui/image/link-type-tab.png)

The argument definition in **Arguments** and filter conditions defined in **Filter** become part of the module's URI and must be URL-encoded. ServiceNow automatically URL-encodes filter conditions and appends them to the module URI using sysparm\_query. For example, adding the filter condition, **Active is true** appends `sysparm_query=active%3Dtrue` to the module's URI; %3D is the URL-encoding for the equals sign \(=\).

The following table shows when you must URL-encode the argument in the **Arguments** field and when ServiceNow URL-encodes the argument.

<table id="table_w4y_k2s_yhb"><thead><tr><th>

Has a filter condition?

</th><th>

Argument definition starts with

</th><th>

Who encodes the argument?

</th><th>

How argument is handled

</th></tr></thead><tbody><tr><td>

No

</td><td>

^

</td><td>

ServiceNow

</td><td>

Removes the caret \(^\) from the argument, encodes it and uses sysparm\_query to append it to the module URI.

</td></tr><tr><td>

No

</td><td>

&amp;

</td><td>

You

</td><td>

Removes the ampersand \(&amp;\) from the argument and appends it to the module URI.

</td></tr><tr><td>

No

</td><td>

Anything else

</td><td>

ServiceNow

</td><td>

Encodes the argument and uses sysparm\_query to append it to the module URI.

</td></tr><tr><td>

Yes

</td><td>

^

</td><td>

ServiceNow

</td><td>

URL-encodes the filter definition and the argument and uses sysparm\_query to append the combination to the module URI.

</td></tr><tr><td>

Yes

</td><td>

Anything else

</td><td>

You

</td><td>

URL-encodes the filter definition and uses sysparm\_query to append it and the \(unaltered\) arguments to the module URI.

</td></tr></tbody>
</table>You can turn on \(the default\) and off the URL-encoding requirement for module UIs using the **glide.ui.encode\_module\_uri** property.

#### Examples

The following examples demonstrate when you have to URL-encode the argument definition in **Arguments**:

-   There are no filter conditions and the argument definition in **Arguments** starts with an ampersand, for example,`&sysparm_fixed_query=assigned_to=javascript:gs.user_id()`.

    This argument breaks the module URI because the equals sign and the colon are not URL-encoded, and the ampersand prevents ServiceNow from URL-encoding the argument. URL-encode the argument: `&sysparm_fixed_query=assigned_to%3Djavascript%3Ags.user_id()`.

-   There are filter conditions and the argument definition in **Arguments** does not start with a caret \(^\), for example, `sysparm_name=Barnes & Noble's`.

    This argument breaks the module URI because the ampersand and spaces are not URL-encoded. URL-encode the argument: `sysparm_name=Barnes%20%26%20Nobel's`


## Module Visibility

Verify the visibility, or lack thereof, of selected modules in the application navigator \(left navigation bar\). For example, create a test that first impersonates a user, then verifies that specified modules \(such as Homepage and My Requests\) are visible, or are not visible, to that user.

<table id="table_knc_vgs_mcb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Execution order

</td><td id="atf-exec-order">

Integer specifying the order in which the test executes this step.As you create steps, the system automatically assigns each step an incremental value. This value causes the test to execute steps in the order that you created them in. You can change this default order by editing the **Execution order** values.

</td></tr><tr><td>

Active

</td><td id="atf-active">

Option to activate this test step for use.

</td></tr><tr><td>

Application

</td><td id="application-scope-suite">

The application scope in which the system runs this test or test suite.

</td></tr><tr><td>

Test

</td><td id="atf-test">

Read-only name of the test that you're adding the step to.

</td></tr><tr><td>

Step config

</td><td id="atf-step-config">

Read-only name of the step.

</td></tr><tr><td>

Description

</td><td id="atf-description">

Description of the test step. This field value is automatically set based on the field values of the test step. This field appears after the test step is submitted.

</td></tr><tr><td>

Notes

</td><td id="atf-notes">

Notes about the test step.

</td></tr><tr><td>

Navigator

</td><td id="atf-navigator">

Navigator version to assert against-   Core UI \(UI16\): If you are creating new steps, you will have Core UI by default.
-   Next Experience: If you have Next Experience enabled, Next Experience is the default navigator. If it is disabled, Core UI is the default navigator.

</td></tr><tr><td>

Visible assert type

</td><td id="atf-module-visible-assert-type">

Specifies how modules selected in the **Visible modules** field should be tested for visibility in the application navigator.-   **At least these modules are visible**: At minimum, the modules selected in the **Visible modules** field are visible in the application navigator.
-   **Only these modules are visible**: Only the specific modules selected in the **Visible modules** field are visible in the application navigator.

</td></tr><tr><td>

Visible modules

</td><td id="atf-visible-modules">

Modules whose visibility in the application navigator is being verified.

</td></tr><tr><td>

Not visible assert type

</td><td id="atf-module-not-visible-assert-type">

Specifies how modules selected in the **Not visible modules** field should be tested for lack of visibility in the application navigator.-   **At least these modules are not visible**: At minimum, the modules selected in the **Not visible modules** field are not visible in the application navigator.
-   **Only these modules are not visible**: Only the specific modules selected in the **Not visible modules** field are not visible in the application navigator.

</td></tr><tr><td>

Not visible modules

</td><td id="atf-not-visible-modules">

Modules whose lack of visibility in the application navigator is being verified.

</td></tr></tbody>
</table>**Related topics**  


[Create a module](test-steps-app-navigator-category.md#)

## Navigate to Module

Open a module from the application navigator, as if a user had clicked it. The module must be visible to the currently executing user to navigate to it.

**Note:** Not all pages are currently testable. Wherever the module takes you is your responsibility.

<table id="table_knc_vgs_mcb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Execution order

</td><td id="atf-exec-order">

Integer specifying the order in which the test executes this step.As you create steps, the system automatically assigns each step an incremental value. This value causes the test to execute steps in the order that you created them in. You can change this default order by editing the **Execution order** values.

</td></tr><tr><td>

Active

</td><td id="atf-active">

Option to activate this test step for use.

</td></tr><tr><td>

Timeout

</td><td id="atf-timeout">

Number of seconds allowed before the step fails. If the validation fails, the system repeats the step until it reaches the duration of the timeout. If the validation fails after the timeout duration has passed, the step fails.

</td></tr><tr><td>

Application

</td><td id="atf-application-scope">

Application scope in which the system runs this step.

</td></tr><tr><td>

Test

</td><td id="atf-test">

Read-only name of the test that you're adding the step to.

</td></tr><tr><td>

Step config

</td><td id="atf-step-config">

Read-only name of the step.

</td></tr><tr><td>

Description

</td><td id="atf-description">

Description of the test step. This field value is automatically set based on the field values of the test step. This field appears after the test step is submitted.

</td></tr><tr><td>

Notes

</td><td id="atf-notes">

Notes about the test step.

</td></tr><tr><td>

Module

</td><td id="atf-module">

Module that should be opened. To navigate to the selected module, the module must be visible to the currently executing user in the application navigator.The following modules are not supported and cannot be tested:

-   Modules that are separators
-   Modules that do not link to a specific page, but instead execute client-side JavaScript \(such as Studio and the Script Debugger\)
-   Modules that link to external websites, such as the ServiceNow documentation site \(servicenow.com/docs\)
-   Modules that reload or redirect the entire page

</td></tr></tbody>
</table>**Related topics**  


[Create a module](test-steps-app-navigator-category.md#)

