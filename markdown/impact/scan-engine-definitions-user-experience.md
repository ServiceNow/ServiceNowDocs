---
title: Scan Engine definitions: User Experience
description: Scan Engine user experience definitions evaluate the quality of user interactions with applications. Considers the ease of use, efficiency, design, responsiveness, accessibility, and its emotional and functional impact.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-05-08"
reading_time_minutes: 8
breadcrumb: [View and modify Scan Engine definitions, Scan Engine definitions, Scan Engine, Platform Health, Using Impact, Impact]
---

# Scan Engine definitions: User Experience

Scan Engine user experience definitions evaluate the quality of user interactions with applications. Considers the ease of use, efficiency, design, responsiveness, accessibility, and its emotional and functional impact.

## Australia definitions

The following user experience definitions have been added for the Australia 2026 release:

<table id="table_user_experience"><thead><tr><th>

Number

</th><th>

Active

</th><th>

Level of Finding

</th><th>

Unique ServiceNow Product

</th><th>

Short Description

</th><th>

Business Impact

</th><th>

Steps to Resolve

</th><th>

Supporting Documentation

</th></tr></thead><tbody><tr><td>

sn\_SE10026

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

JavaScript popups \(alert, confirm, prompt\) should be limited in use

</td><td>

Users may become frustrated with the tool with all the popups.

</td><td>

Use OOB methods such as **g\_form.addInfoMessage**\(\) and **g\_form.showFieldMsg**\(\) to display information to the user without popups. **GlideDialogWindow** is another method that can be utilized if we need to gather data from the user which doesn't reside on the form.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=c_GlideModalV3API.html)

</td></tr><tr><td>

sn\_SE10029

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Modules should not be linked to nonexistent tables

</td><td>

Users may become frustrated with ServiceNow.

</td><td>

Deactivate the module.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=test-steps-app-navigator-category.html)

</td></tr><tr><td>

sn\_SE10056

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Email Sending enabled on non-production system

</td><td>

User could become frustrated with the platform as well as time could be spent on a fictitious task.

</td><td>

Either disable email sending or provide a test user that will receive all emails.

</td><td>

[Documentation](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0725822)

</td></tr><tr><td>

sn\_SE10058

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

g\_form.setVisible should be replaced with g\_form.setDisplay

</td><td>

User may see blank areas on the form.

</td><td>

Use either a UI Policy or **g\_form.setDisplay** function in place of **g\_form.setVisible** function.

</td><td>

[Documentation](https://www.servicenow.com/community/developer-forum/difference-between-setvisible-and-setdisplay-on-g-form/m-p/1549622)

</td></tr><tr><td>

sn\_SE10140

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

First element on a global list shouldn't be a reference field

</td><td>

Users may experience frustration.

</td><td>

Update the list view to show something other than a reference field as its first element.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=t_ConfigureTheListLayout.html)

</td></tr><tr><td>

sn\_SE10249

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

Optional: Hints should be included for all fields

</td><td>

End users may become frustrated with the lack of how to use the system.

</td><td>

Add a hint describing any pertinent information about the field to help the end user better understand the field's purpose.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=t_ChangeFieldLabelOrHint.html)

</td></tr><tr><td>

sn\_SE10264

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

The meta field should not be empty on catalog items

</td><td>

User experience should improve.

</td><td>

Review the catalog item to determine the appropriate keywords for the catalog item and add those to the Meta field.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=search-catalog-item.html)

</td></tr><tr><td>

sn\_SE10267

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

Dirty form support should not be disabled

</td><td>

End users may become frustrated with the platform as a result of their modifications not being saved.

</td><td>

Enable dirty form support by setting the property **glide.ui.dirty\_form\_support** to **true**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=r_AvailableSystemProperties.html)

</td></tr><tr><td>

sn\_SE10269

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

System property glide.ui.max\_ref\_dropdown should not be greater than 100

</td><td>

Too many choices on a screen resulting a poor user experience.

</td><td>

Update the value on the **glide.ui.max\_ref\_dropdown** system property to be less than 100 \(preferably a value of 25\).

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=t_DisplayTheRefFieldAsAChoiceList.html)

</td></tr><tr><td>

sn\_SE10270

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

HTML Field Editor should be set to "tinymce"

</td><td>

Unexpected functionality may result in a poor user experience.

</td><td>

The value of "**glide.ui.html.editor**" should be set to "tinymce".

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=c_UseHTMLFields.html)

</td></tr><tr><td>

sn\_SE10271

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Maximum attachment size is greater than 5GB

</td><td>

Users may experience issues on the platform after loading a large attachment.

</td><td>

Review the attachment size and determine if allowing more than a 5GB attachment is necessary.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=r_AvailableSystemProperties.html)

</td></tr><tr><td>

sn\_SE10296

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Notifications should not have inactive recipients

</td><td>

Potential process delays due to notifications that are never received.

</td><td>

Replace inactive recipients or set notifications to be sent to groups that are maintained with only active users.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=notifications.html)

</td></tr><tr><td>

sn\_SE10297

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Child group does not contain all parent roles

</td><td>

Process delays due to insufficient access.

</td><td>

Review this group to understand why the roles have not been inherited from the parent group. Potential causes to this issue include business rules that did not execute, a clone that excludes the Group Role \[**sys\_group\_has\_role**\] table, or if roles have been deleted directly from the Group Role \[**sys\_group\_has\_role**\] table. Removing the parent from this group, saving, and then adding the parent back should resolve this issue.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=t_CreateAGroup.html)

</td></tr><tr><td>

sn\_SE10308

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Change Request conflict detection: blackout window

</td><td>

Change Requests will be unable to check against blackout windows which could jeopardize the success of the change.

</td><td>

The following Conflict Detection property should be set to **true**: change.conflict.blackout.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=configure-conflict-properties.html)

</td></tr><tr><td>

sn\_SE10309

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Change Request conflict detection: current CI

</td><td>

Change Requests will be unable to check against CI conflicts which could jeopardize the success of the change.

</td><td>

The following Conflict Detection property should be set to **true**: change.conflict.currentci.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=configure-conflict-properties.html)

</td></tr><tr><td>

sn\_SE10310

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Change Request conflict detection should be enabled for maintenance windows

</td><td>

Change Requests will be unable to check against the CI's maintenance window which could jeopardize the success of the change.

</td><td>

The following Conflict Detection system property should be set to **true**: change.conflict.currentwindow.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=configure-conflict-properties.html)

</td></tr><tr><td>

sn\_SE10311

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Change Request conflict detection: refresh conflicts

</td><td>

Change Requests that do not automatically run conflict detection when significant fields are updated risk missing a conflict which could jeopardize the success of the change.

</td><td>

The following Conflict Detection property should be set to **true**: change.conflict.refresh.conflicts.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=configure-conflict-properties.html)

</td></tr><tr><td>

sn\_SE10317

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Groups should have a manager

</td><td>

Groups with no manager's assigned can lead to difficulty with escalations, failure to meet SLAs, and poor data management.

</td><td>

Assign a manager to the group.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=t_CreateAGroup.html)

</td></tr><tr><td>

sn\_SE10422

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Multiple UI Policies with the same order for a particular field/variable

</td><td>

User could become frustrated with the platform and consider the inconsistent behavior a bug.

</td><td>

Differentiate the order on the UI Policies to ensure UI Policies are always fired in the same sequence which will keep the user experience consistent.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=t_CreateAUIPolicy.html)

</td></tr><tr><td>

sn\_SE10495

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

Query Business Rules filtering out records without your knowledge

</td><td>

Records you need access to could be filtered out unknowingly.

</td><td>

-   Redirect employees to the Portal, you will not need to create query business rule because there is a filter already in place.
-   If there is a need restrict query on the tables, try using fixed query on filters instead.
-   If the above two are not an option then ensure the following are considered when creating Query Business Rule.
-   Index the most common field in the filter.
-   Avoid negative operator like != or NOT IN.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=t_RestrictBreadcrmbsWFixedQueries.html)

</td></tr><tr><td>

sn\_SE10510

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

Duplicate task numbers

</td><td>

Duplicate task numbers may confuse users and create unnecessary effort.

</td><td>

Although duplicate numbers are rare, numbering does not enforce uniqueness, by default. Fix the number maintenance and re-number those who are duplicates. Enable unique number indexing on the table to ensure duplicate numbers are not created.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=c_EnforcingUniqueNumbering.html)

</td></tr><tr><td>

sn\_SE10514

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Avoid creating long module titles

</td><td>

Long module titles affect readability on the navigator.

</td><td>

Reduce the length of module titles.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=test-steps-app-navigator-category.html)

</td></tr><tr><td>

sn\_SE10515

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

Catalog Items should have a Name and Short description

</td><td>

Catalog Items may be difficult to identify without a Name or Short Description.

</td><td>

Add a Name and Short Description when configuring Catalog Items.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=t_DefineACatalogItem.html%23t_DefineACatalogItem)

</td></tr><tr><td>

sn\_SE10516

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Group exists with no users

</td><td>

Any objects referencing an empty group, such as reports, will not reach it's intended audience.

</td><td>

Add users to the group or set the group to inactive.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=t_AddAUserToAGroup.html)

</td></tr><tr><td>

sn\_SE10518

</td><td>

1

</td><td>

Review

</td><td>

 

</td><td>

Excessive use of fields on a form

</td><td>

User could become frustrated with the platform and consider the inconsistent behavior a bug.

</td><td>

Review the purpose of each field configured on a form and decide whether or not it is truly needed.

</td><td>

[Documentation](https://docs.servicenow.com/csh?topicname=configure-form-layout.html)

</td></tr><tr><td>

sn\_SE10519

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

HR Service should have a Fulfillment Instruction

</td><td>

Without fulfillment instructions, HR agents may have difficulty completing cases.

</td><td>

Use the condition builder to dynamically change what fulfillment instructions appear for an HR case when it is transferred from one HR service to another.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=hr-fulfillment-instructions.html)

</td></tr><tr><td>

sn\_SE10520

</td><td>

1

</td><td>

Review

</td><td>

 

</td><td>

Number of Related Lists on Project Form

</td><td>

User could become frustrated with the platform and consider the inconsistent behavior a bug.

</td><td>

Review number of related lists and determine which lists are required.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=c_RelatedLists.html)

</td></tr><tr><td>

sn\_SE10521

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Knowledge articles older than 12 months may be outdated

</td><td>

Information within the knowledge articles may be outdated and may not contain accurate and up-to-date information

</td><td>

Review the content contained within knowledge articles older than 12 months and determine if it should be edited, retired, or preserved.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=c_RetiredKnowledgeArticles.html)

</td></tr><tr><td>

sn\_SE10524

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Excessive Client Scripts

</td><td>

Users may experience reduced performance while loading or updating records.

</td><td>

Reduce and optimize the number of client scripts per table. Deactivate any unnecessary client scripts.

</td><td>

[Documentation](https://developer.servicenow.com/dev.do%23!/guides/latest/now-platform/tpb-guide/client_scripting_technical_best_practices)

</td></tr><tr><td>

sn\_SE10525

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

List Report without any columns selected

</td><td>

Reports could be unreadable and confusing without defined columns.

</td><td>

In the Columns window that opens after you select Choose columns, select fields in the Available list that you want to appear in your report and move them to the Selected list.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=t_CreateAListReport.html)

</td></tr><tr><td>

sn\_SE10527

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Populate Knowledge Base articles fully

</td><td>

Users may have difficulty finding relevant knowledge articles.

</td><td>

Update the KB article to populate relevant fields \(Short Description, Category, KB Article Body, Valid To and Author\).

</td><td>

[Documentation](http://docs.servicenow.com/csh?topicname=t_CreateAKnowledgeArticle.html)

</td></tr><tr><td>

sn\_SE10533

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

Inactive breakdown source associated with active indicators or collection jobs

</td><td>

The breakdown defined in the indicator or collection job may return incomplete or no data.

</td><td>

Set the breakdown source to active so the breakdown it is defined in can properly capture the elements needed for the collection job.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=t_DefiningABreakdownSource.html)

</td></tr><tr><td>

sn\_SE10535

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Human Resource Catalog Client scripts should have 'All' as UI type

</td><td>

The HR application experience between desktop and mobile may differ for users if catalog client scripts are not defined for both.

</td><td>

Set the UI type field to "All".

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=c_CatalogClientScriptCreation.html)

</td></tr><tr><td>

sn\_SE10537

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Instance URL should not be hard-coded

</td><td>

Objects referring to the hard-coded URL will not be dynamic and will only be useful for the hard-coded instance.

</td><td>

Use the method **gs.getProperty**\(**__instance\_name__**\); to dynamically retrieve the instance name, or **gs.getProperty**\(**__glide.servlet.uri__**\); to get the full URL.

</td><td>

[Documentation](https://docs.servicenow.com/csh?topicname=c_GlideSystemScopedAPI.html&version=latest%23title_r_ScopedGlideSystemGetProperty_String_Object)

</td></tr><tr><td>

sn\_SE10545

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Active session time should be greater than the inactive session time for Integrations

</td><td>

Inefficient session management creates a poor user experience and poor performance with integrations

</td><td>

Adjust the "**glide.integrations.active.session.life\_span**" property to have a greater value than the "**glide.integration.session\_timeout**" property.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=managing-integration-sessions.html)

</td></tr><tr><td>

sn\_SE10551

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Widgets not used in any dashboards

</td><td>

Without widgets, dashboards will appear empty and not convey important data.

</td><td>

Use the Widget Picker to add widgets to your dashboard.

</td><td>

[Documentation](https://docs.servicenow.com/csh?topicname=c_Widgets.html)

</td></tr><tr><td>

sn\_SE10575

</td><td>

1

</td><td>

Review

</td><td>

 

</td><td>

Change the favicon to a more representive picture of your company

</td><td>

The favicon is a visible representation of our IT department's attention to detail and commitment to providing a modern, user-friendly experience. An outdated favicon can lead to a perception that our IT services are outdated, slow to adapt, or unresponsive to user needs.

</td><td>

First, upload an image by navigating to System UI &gt; Images &gt; New. Once uploaded, navigate to System Properties &gt; System &gt; then in the Icon image displayed in the bookmarks and browser address bar, enter the file name of your uploaded image.The feature is controlled by a system property **__glide.product.icon__**, it should exist with a value set by admin.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=customize-favicon.html)

</td></tr></tbody>
</table>