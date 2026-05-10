---
title: User preference settings
description: User preferences primarily track the way individual users interact with various features so that new sessions activate the user's last settings. For example, user preferences track whether the user activates the tabbed or scrolling interface for multi-section forms. Other user preference records enable users with the admin role to adjust certain feature settings.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 14
breadcrumb: [User preferences, User interface configuration, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# User preference settings

User preferences primarily track the way individual users interact with various features so that new sessions activate the user's last settings. For example, user preferences track whether the user activates the tabbed or scrolling interface for multi-section forms. Other user preference records enable users with the admin role to adjust certain feature settings.

## View settings

To view the user preference settings, navigate to **User Administration** &gt; **User Preferences**.

## User preference list

This table describes user preference records in the base system.

|User preference record|Description|
|----------------------|-----------|
|User Only|User action sets and updates the value. Manual changes through the User Preference record don't affect the user experience.|
|Admin Only|The administrator can change the value through the User Preference record to modify the user experience.|
|Admin or User|User action sets and updates the value, but the administrator can change the user experience by manually updating the User Preference record.|
|System Only|The system sets and updates the value. Administrators should not modify these records.|

This table provides the default value and a description for each preference. The Updated By column indicates how the preference is set.

<table id="table_r5h_fnf_vt"><thead><tr><th>

Preference

</th><th>

Category

</th><th>

Updated by

</th><th>

Details

</th></tr></thead><tbody><tr><td>

&lt;table&gt;.db.order

</td><td>

List Sort

</td><td>

Admin or User

</td><td>

For the identified table, indicates which column is used to sort the records in a list. This record updates automatically each time the user changes the sort order for the table.**Type**: **String**

 **Default value**: User selection or the **Number** column if the user doesn't select a column. If the **Number** column is empty, the **Name** field is used to sort the records.

</td></tr><tr><td>

&lt;table&gt;.db.order.direction

</td><td>

List Sort

</td><td>

Admin or User

</td><td>

For the identified table, indicates whether the list shows records in ascending \(ASC\) or descending \(DESC\) order by the field identified in &lt;table&gt;.db.order. This record is updates each time the user changes the sort direction for the table.**Type**: **String**

 **Default value**: **None**

</td></tr><tr><td>

bsm\_map.default\_ci

</td><td>

BSM

</td><td>

User Only

</td><td>

Contains the sys\_id of the last configuration item the user viewed in the business service management \(BSM\) map. This record updates automatically each time the user views a new configuration item in the BSM map.**Type**: **String**

 **Default value**: **None**

</td></tr><tr><td>

ci\_manage\_relationships\_filter\_hint.cmdb\_ci

</td><td>

CMDB

</td><td>

Admin Only

</td><td>

Constrains what appears in the **Available CIs** list when defining a relationship for a configuration item. The value is in the format of an encoded query string.**Type**: **String**

 **Default value**: locationANYTHING^operational\_statusANYTHING

</td></tr><tr><td>

ci\_manage\_relationships\_filter\_hint.sys\_user

</td><td>

CMDB

</td><td>

Admin Only

</td><td>

Constrains what appears in the **Available User** list when defining a relationship for a configuration item. The value is in the format of an encoded query string.**Type**: **String**

 **Default value**:**active=true**

</td></tr><tr><td>

ci\_manage\_relationships\_filter\_hint.sys\_user\_group

</td><td>

CMDB

</td><td>

Admin Only

</td><td>

Constrains what appears in the **Available Groups** list when defining a relationship for a configuration item. The value is in the format of an encoded query string.**Type**: **String**

 **Default value**: **active=true**

</td></tr><tr><td>

collapse.&lt;related table&gt;.&lt;related field&gt;

</td><td>

Forms

</td><td>

User Only

</td><td>

Indicates that a related list is collapsed. The same related list is collapsed when the user's next session begins. This record updates automatically whenever the user expands or collapses the same related list.**True** = collapse the identified related list.

 **False** = expand the identified related list.

 **Type**: **String**

 **Default value**: **None**

</td></tr><tr><td>

collapse.section.&lt;sys\_id&gt;

</td><td>

Forms

</td><td>

User Only

</td><td>

Indicates the sys\_id of a form section that is collapsed. The same form section is collapsed when the user's next session begins. This record updates automatically whenever the user expands or collapses the same section of the same form.**True** = collapse the identified section.

 **False** \(or blank\) = expand the identified section.

 **Type**: **True/False**

 **Default value**: **False or blank**

</td></tr><tr><td>

glide.debugger.log\_messages\_limit

</td><td>

UI

</td><td>

Admin or User

</td><td>

Specifies the maximum number of messages to be displayed in the script debugger Session Log UI.

</td></tr><tr><td>

glide.debugger.console.cached\_stmt\_limit

</td><td>

UI

</td><td>

Admin or User

</td><td>

Specifies the maximum number of statements to be cached in the browser for Script Debugger Console.

</td></tr><tr><td>

glide.debugger.log.transaction.count

</td><td>

UI

</td><td>

Admin or User

</td><td>

Specifies the maximum number of transactions displayed in the script debugger Session Log UI.

</td></tr><tr><td>

glide.ui11.use

</td><td>

UI11

</td><td>

Admin or User

</td><td>

Indicates whether UI11 is active for this user. UI11 is no longer available.

</td></tr><tr><td>

glide.ui.navpage\_state

</td><td>

Menus

</td><td>

System Only

</td><td>

**DO NOT MODIFY.**Indicates the user's UI11 configuration.**Type**: **String**

 **Default value**: **None**

</td></tr><tr><td>

glide.ui.javascript\_editor

</td><td>

UI

</td><td>

Admin or User

</td><td>

Indicates whether the JavaScript editor and formatting controls are enabled or disabled for the user. The JavaScript editor icon \(![JavaScript editor icon](../image/jscript-icon.png)\) and formatting controls are available only in instances where the Syntax Editor plugin is active. This record updates automatically when a user clicks the icon to enable or disable script editing. For more information, see [JavaScript syntax editor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/scripts/c_SyntaxEditor.md).**True** = enable script editor.

 **False** = disable script editor.

 **Type**: **True/False**

 **Default value**: **True** \(if syntax editor feature is active\)

</td></tr><tr><td>

glide.ui.response\_ time

</td><td>

UI

</td><td>

Admin or User

</td><td>

Determines whether the response time information is expanded or collapsed at the bottom of a list or form. This record updates automatically whenever the user clicks the response time indicator icon ![Clock indicator icon](../image/clock.png) at the bottom of a v2 list or form.**True** = expand the response time information.

 **False** = collapse the response time information.

 **Type**: **String**

 **False**: **False**

</td></tr><tr><td>

homepage

</td><td>

Homepages

</td><td>

Admin or User

</td><td>

Indicates which dashboard appears when a user first logs in to the instance or clicks the homepage icon \(![Homepage icon](../image/HomeIcon.png)\). The value indicates the sys\_id of the selected dashboard.**Type**: **String**

 **Default value**: **None**

</td></tr><tr><td>

knowledge.search.sort.field

</td><td>

List Sort

</td><td>

Admin or User

</td><td>

Determines the sort order for results when searching the knowledge base. This record updates each time the user selects a different **Sort by** option in the search results header. Available options are: Number of Views \(views\), Relevancy \(relevancy\), and Last Modified \(sys\_updated\_on\).**Type**: **String**

 **Default value**: **Views**

</td></tr><tr><td>

list\_edit\_double

</td><td>

Lists

</td><td>

Admin or User

</td><td>

Indicates what action opens the list editor in List v2. This record updates automatically when the user personalizes any v2 list and changes the **Double click to edit** setting. For more information, see [List editor administration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/list-administration/r_AdministeringTheListEditor.md) . This preference does not apply to v3 lists. Single-click list editing is not supported in List v3.**True** = open the list editor when the user double-clicks a field in a v2 list.

 **False** = open the list editor when the user single-clicks a field in a v2 list.

 **Type**: **True/False**

 **Default value**: **True**

</td></tr><tr><td>

list\_edit\_enable

</td><td>

Lists

</td><td>

Admin or User

</td><td>

Indicates whether the list editor is available for editing fields directly in a list. This record updates automatically when the user personalizes any list \(gear icon \(![Gear icon](../image/GearIconUI14.png)\) above the first column in the list\) and changes the **Enable list edit** setting. This preference doesn't apply to v3 lists.**True** = enable use of the list editor.

 **False** = disable use of the list editor.

 **Type**: **True/False**

 **Default value**: **True**

</td></tr><tr><td>

live\_message.feed.last\_display

</td><td>

Live

</td><td>

Admin or User

</td><td>

Stores the last feed the user viewed: **My Feed** \(sysparm\_feed\_type=myfeed\) or **Company Feed** \(sysparm\_feed\_type=company\_feed\). This record updates automatically each time the user selects a different feed. **Type**: **String**

 **Default value**: **sysparm\_feed\_type=company\_feed**

</td></tr><tr><td>

live\_tag.feed.order

</td><td>

Live

</td><td>

Admin or User

</td><td>

Tracks the user's choice of sorting for tag display. This record updates automatically when a user selects a different **Tag Option** in Live. Available options are **Order by Created**\(sys\_created\_on\) and **Order by Last Activity** \(last\_activity\). **Type**: **String**

 **Default value**: **None** \(defaults to sys\_created\_on\)

</td></tr><tr><td>

menu.&lt;identifier&gt;.expanded

</td><td>

Menus

</td><td>

User Only

</td><td>

Indicates the sys\_id of a section of the application navigator menu that is open \(expanded\) for the user. The same section is open when the user's next session begins. This record updates automatically each time the user expands or collapses the same section of the application navigator.**Type**: **String**

 **Default value**: **None**

</td></tr><tr><td>

mobile\_rowcount

</td><td>

Mobile

</td><td>

Admin or User

</td><td>

Indicates the number of rows displayed in a list on a mobile device. This record updates automatically each time the user chooses a different number of rows per page from the mobile screen.**Type**: **Integer**

 **Default value**: **20**

</td></tr><tr><td>

mobile\_use\_full.android

</td><td>

Mobile

</td><td>

Admin or User

</td><td>

Indicates which user interface appears on the user's Android mobile device. This record updates automatically each time the user clicks the gear icon \(![Gear icon](../image/GearIconUI14.png)\) above the mobile homepage to display the full desktop interface, or clicks the cell phone icon in the welcome bar to display the mobile interface. **True** = display the full desktop interface on Android mobile devices.

 **False** = display the mobile interface on Android mobile devices.

 **Type**: **True/False**

 **Default value**: **False**

</td></tr><tr><td>

mobile\_use\_full.iphone

</td><td>

Mobile

</td><td>

Admin or User

</td><td>

Indicates which user interface appears on the user's iPhone mobile device. This record updates automatically each time the user clicks the gear icon \(![Gear icon](../image/GearIconUI14.png)\) above the mobile homepage to display the full desktop interface or clicks the cell phone icon in the welcome bar to display the mobile interface. **True** = display the full desktop interface on an iPhone mobile device.

 **False** = display the mobile user interface on an iPhone mobile device.

 **Type**: **True/False**

 **Default value**: **False**

</td></tr><tr><td>

module

</td><td>

Menus

</td><td>

User Only

</td><td>

Records the sys\_id of the last module the user accessed.**Type**: **String**

 **Default value**: **sys\_id**

</td></tr><tr><td>

owned\_by\_indicator.form

</td><td>

Update Sets

</td><td>

Admin Only

</td><td>

Shows or hides the update indicator icon In form headers when customer updates to that form are being tracked by update sets.**True** = show the customer updates indicator icon.

 **False** = hide the customer updates indicator icon.

 **Type**: **True/False**

 **Default value**: **False**

</td></tr><tr><td>

recent.impersonations

</td><td>

Administration

</td><td>

User Only

</td><td>

**DO NOT MODIFY.** Shows who the administrator most recently impersonated. For more information, see [Impersonate a user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/user-administration/c_ImpersonateAUser.md).**Type**: **String**

 **Default value**: **None**

</td></tr><tr><td>

report.expanded

</td><td>

Reporting

</td><td>

Admin or User

</td><td>

Works with the UI property **List of roles \(comma-separated\) that can expand the report header** to determine whether the report header is open when viewing a report.For users whose role permits them to access the report header, the **report.expanded** user preference indicates whether reports open with the header expanded or collapsed. Expanding the report header reveals the report builder which is used to modify the report definition. This user preference record updates automatically each time the user expands or collapses the report header. If the user's role doesn't have permission to view the report header, the report header is never accessible, regardless of this user preference setting.

 **True** = expand the report header when displaying a report.

 **False** = collapse the report header when displaying a report.

 **Type**: **String**

 **Default value**: **True**

</td></tr><tr><td>

rowcount

</td><td>

Lists

</td><td>

User Only

</td><td>

Indicates the maximum number of rows that display on a single page in a list. This value also determines the maximum number of records that display in a list report on a dashboard. This record updates automatically when a user chooses a different number. **Type**: **Integer**

 **Default value**: **20**

</td></tr><tr><td>

sys\_update\_set

</td><td>

Update Sets

</td><td>

User Only

</td><td>

**DO NOT MODIFY.** Indicates the update set that is currently active. This value update automatically when a user selects a different update set.**Type**: **GUID**

 **Default value**: sys\_id of default update set

</td></tr><tr><td>

tabbed.forms

</td><td>

Forms

</td><td>

User Only

</td><td>

Indicates whether forms that contain more than two sections use a tabbed interface or a scrolling list of sections. This setting applies to all forms. It's not set on a form-by-form basis. This record updates automatically when a user clicks the Toggle Tabs icon in the banner bar. For more information, see [Configure the form layout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/configure-form-layout.md) .**True** = display multi-section forms as tabs.

 **False** or blank = display multi-section forms as a scrolling list of sections.

 **Type**: **True/False**

 **Default value**: **False**

</td></tr><tr><td>

table.compact

</td><td>

Lists

</td><td>

User Only

</td><td>

Indicates whether lists appear with more or less blank space above and below each row. This setting applies to all lists. It's not set on a list-by-list basis. This record updates automatically when a user personalizes any list and changes the **Compact rows** option.**True** = reduce the blank space above and below each row in a list to show more rows on the screen at one time.

 **False** = add blank space above and below each row in a list to improve readability.

 **Type**: **True/False**

 **Default value**: **False**

</td></tr><tr><td>

table.wrap

</td><td>

Lists

</td><td>

User Only

</td><td>

Indicates whether long text in a list is wrapped onto multiple lines or truncated. This setting applies to all lists. This setting is not set on a list-by-list basis. This record updates automatically when a user changes the **Wrap column text** option in the List v2 personalization interface or the **Wrap longer text in list columns** option in the Core UI system settings.**True** = wrap long text in a list. All text is seen in list view, but each row may occupy more vertical space.

 **False** = don't wrap the long text in a list. Text is truncated in list view, but each row takes less vertical space. Full text can be seen in form view.

 **Type**: **True/False**

 **Default value**: **True**

</td></tr><tr><td>

ts.match

</td><td>

Text Search

</td><td>

Admin or User

</td><td>

Indicates whether the task record should be returned by a global text search in which the search text exactly matches a task number. This record updates automatically when a user clicks the **Search tips and preferences** link on the search results page and changes the **Return task record if searching for exact number** setting. For more information, see [Global text search finds records from multiple tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/c_GlobalTextSearch.md).**True** = return the task record. A link is provided for full search results.

 **False** = return full search results, even if the search term matches a task number.

 **Type**: **True/False**

 **Default value**: **True**

</td></tr><tr><td>

ts.remember.expanded

</td><td>

Text Search

</td><td>

Admin or User

</td><td>

Indicates whether to remember which search groups were expanded and collapsed during the previous search. The search groups available depend on the user's access rights and selections. This record updates automatically when the user clicks the **Search tips and preferences** link on the search results page and changes the **Use remembered expand / collapse preferences** setting.**True** = remember the expand/collapse setting and use it for subsequent searches.

 **False** = do not remember the expand/collapse setting. Expand all groups for subsequent searches.

 **Type**: **String**

 **Default value**: **True**

</td></tr><tr><td>

ts.show\_empty\_groups

</td><td>

Text Search

</td><td>

Admin or User

</td><td>

Indicates whether global text search results include groups with no matches. The search groups available depend on the user's access rights. This record updates automatically when the user clicks the **Search tips and preferences** link on the search results page and changes the **Show groups with no search matches** setting.**True** = include empty groups when displaying global text search results.

 **False** = hide empty groups when displaying global text search results.

 **Type**: **String**

 **Default value**: **True**

</td></tr><tr><td>

ts.show\_negative\_result\_info

</td><td>

Text Search

</td><td>

Admin or User

</td><td>

Indicates whether group headers in the global text search results page should identify tables that had no matches. The search groups available depend on the user's access rights. This record updates automatically when the user clicks the **Search tips and preferences** link on the search results page and changes the **In search group header, list tables with no search matches** setting.**True** = show tables that returned no matches in the group header.

 **False** = hide tables that returned no matches in the group header.

 **Type**: **String**

 **Default value**: **True**

</td></tr><tr><td>

ts.show\_search\_groups

</td><td>

Text Search

</td><td>

Admin or User

</td><td>

Indicates whether the global text search results page includes check boxes that let the user indicate which groups to search and display. The search groups available depend on the user's access rights and settings. This record updates automatically when the user clicks the **Search tips and preferences** link on the search results page and changes the**Show selectable search groups** setting. **True** = show the check boxes for enabling or disabling individual search groups.

 **False** = hide the check boxes for enabling or disabling individual search groups.

 **Type**: **String**

 **Default value**: **True**

</td></tr><tr><td>

user.can.logout

</td><td>

Security

</td><td>

Admin Only

</td><td>

Indicates whether users see a **Logout** button. If this is False, users are automatically logged out when their session times out. This user preference does not apply to Core UI.**True** = show the **Logout** button, which enables manual logout.

 **False** = hide the **Logout** button, which disables manual logout.

 **Type**: **True/False**

 **Default value**: **True**

</td></tr><tr><td>

use.concourse

</td><td>

Core UI

</td><td>

Admin Only

</td><td>

Indicates whether users see UI15 or Core UI \(UI16\). The Core UI plugin \[com.glide.ui.ui16\] must be enabled for users to see Core UI. **True** = show Core UI by default

 **False**= show legacy UI15 by default

 **Type**: **String**

 **Default value**: **True**

</td></tr></tbody>
</table>**Parent Topic:**[User preferences](../concept/c_UserPreferences.md)

**Related topics**  


[Turn off the Next Experience welcome screen after upgrading your instance](../task/remove-welcome-splash-screen.md)

[Configure available keyboard shortcuts](../task/configure-keyboard-shortcuts.md)

