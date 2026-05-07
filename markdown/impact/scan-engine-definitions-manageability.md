---
title: Scan Engine definitions: Manageability
description: Scan Engine Manageability definitions measure the extent to which ServiceNow instances, applications, or infrastructure can be effectively monitored, configured, and maintained.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-05-06"
reading_time_minutes: 26
breadcrumb: [View and modify Scan Engine definitions, Scan Engine definitions, Scan Engine, Platform Health, Using Impact, Impact]
---

# Scan Engine definitions: Manageability

Scan Engine Manageability definitions measure the extent to which ServiceNow instances, applications, or infrastructure can be effectively monitored, configured, and maintained.

## Australia definitions

The following manageability definitions have been added for the Australia 2026 release:

<table id="table_manageability"><thead><tr><th>

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

sn\_SE10002

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Multiple tables are using the same number prefix

</td><td>

Multiple tables sharing the same number prefix can result in confusion and wasted effort and time due to workflow, integration, or script malfunctions leading to incorrect record processing or data inconsistencies as well as in inaccurate searches and reports.

</td><td>

This prefix is being shared by multiple tables. Tables should either have their own prefix or share their extended table's prefix.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=c_ManagingRecordNumbering.html)

</td></tr><tr><td>

sn\_SE10021

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

onSubmit client script should not use asynchronous AJAX methods

</td><td>

Client side logic could be skipped without the user's knowledge. Further, this may result in inaccurate data.

</td><td>

Use a synchronous AJAX call \(**getXMLWait\(\)**\) to make a trip to the server within an onSubmit client script.

</td><td>

[Documentation](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0783579)

</td></tr><tr><td>

sn\_SE10022

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

onBefore transform scripts should not use target.update\(\)

</td><td>

Additional impact to database server which may impact other processes.

</td><td>

Remove target.**update\(\)**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=c_TroubleshootImportSetPerformance.html)

</td></tr><tr><td>

sn\_SE10030

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Remove Package calls from script

</td><td>

Functionality could break during an upgrade.

</td><td>

Replace the Package call with the appropriate **GlideScriptable** class.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=c_PackagesCallRemovalTool.html)

</td></tr><tr><td>

sn\_SE10034

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Scripts should not contain hard-coded sys\_ids

</td><td>

Unexpected results in production.

</td><td>

Consider using a property that references the record which had a hardcoded **sys\_id**.

</td><td>

[Documentation](https://developer.servicenow.com/dev.do%23!/guides/utah/now-platform/tpb-guide/scripting_technical_best_practices)

</td></tr><tr><td>

sn\_SE10036

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Access Controls are typically setup by role not group

</td><td>

Higher maintenance as well as group/role access conflicts.

</td><td>

Consider setting up the Access Control to restrict access based on what role the user has versus what group the user is in.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=access-control-rules.html)

</td></tr><tr><td>

sn\_SE10043

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Unnecessary Catalog UI Policy since it doesn't apply anywhere

</td><td>

Developer may need to spend time to figure out why this record exists.

</td><td>

Delete the Catalog UI Policy or check one of the Applies To check boxes.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=t_CreatUIPolicyForSvcCalgIt.html)

</td></tr><tr><td>

sn\_SE10044

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Unnecessary Catalog Client Script since it doesn't apply anywhere

</td><td>

Developer may need to spend time to figure out why this record exists.

</td><td>

Delete the Catalog UI Policy or check one of the Applies To check boxes.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=c_CatalogClientScriptCreation.html)

</td></tr><tr><td>

sn\_SE10049

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Avoid DOM Manipulation \(document, $, gel, or jQuery\)

</td><td>

Unexpected results in production.

</td><td>

Remove any references to document object calls.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=client-script-best-practices.html)

</td></tr><tr><td>

sn\_SE10055

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Aysnc business rules shouldn't use previous/changes/changesTo/changesFrom in the Script field

</td><td>

Unexpected results in production.

</td><td>

If the previous variable needs to be referenced or the business rule should only run when a field value changes then consider converting the business rule to run after.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=c_BusinessRules.html)

</td></tr><tr><td>

sn\_SE10057

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

GlideRecord's initialize\(\) or newRecord\(\) method should be called when inserting new records

</td><td>

Unexpected results in production.

</td><td>

After creating the **GlideRecord** object call the **initialize\(\)** or **newRecord\(\)** method. Use **newRecord\(\)** to include default values.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=c_GlideRecordAPI.html)

</td></tr><tr><td>

sn\_SE10059

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

g\_form.showErrorBox\(\)/hideErrorBox\(\) should be replaced with g\_form.showFieldMsg\(\)/hideFieldMsg\(\)

</td><td>

Future upgrades could limit the use of these legacy methods and break code in production.

</td><td>

Use **g\_form.showFieldMsg**\(\) or **g\_form.hideFieldMsg**\(\) functions in place of **g\_form.showErrorBox**\(\) and/or **g\_form.hideErrorBox**\(\) functions.

</td><td>

[Documentation](https://www.servicenow.com/docs/bundle/zurich-api-reference/page/app-store/dev_portal/API_reference/GlideForm/concept/c_GlideFormAPI.html)

</td></tr><tr><td>

sn\_SE10061

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Unnecessary UI Policy Action - all actions set to 'Leave Alone'

</td><td>

Developer may need to spend time to figure out why this record exists.

</td><td>

Delete the UI Policy Action.

</td><td>

[Documentation](https://developer.servicenow.com/dev.do%23!/learn/learning-plans/zurich/new_to_servicenow/app_store_learnv2_scripting_zurich_ui_policy_actions)

</td></tr><tr><td>

sn\_SE10071

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

gs.getProperty\(system Properties of type true\|false\) returns string values as in 'true'/'false'

</td><td>

If string values are treated as booleans, it might give an unexpected result

</td><td>

-   Add quotes around **true**/**false** inside the condition that's testing against the system property.
-   Broken: **gs.getProperty**\("**enable\_email**"\) == **true**.
-   Fixed: **gs.getProperty**\("**enable\_email**"\) == "**true**".

</td><td>

[Documentation](https://www.servicenow.com/community/developer-articles/system-properties-it-s-usage/ta-p/2300155)

</td></tr><tr><td>

sn\_SE10097

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Script Include names should be in Upper Camel Case

</td><td>

Development time may be increased.

</td><td>

-   Script Include names should follow the upper camel case format. Special characters should not be used.
-   Examples: MyScriptInclude or WorkflowUtils.
-   Note: If a change is made to the script include, then all scripts calling this script include will need to be updated as well.

</td><td>

[Documentation](https://www.servicenow.com/community/developer-articles/devbasics-give-me-names/ta-p/2323543)

</td></tr><tr><td>

sn\_SE10098

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Catalog Variables names should follow the snake\_case format with the first letter being lower case

</td><td>

Development time may be increased.

</td><td>

-   Follow the **snake\_case** format: only underscores, lower case letters, and numbers should be used.
-   Note: If a change is made to this variable, then all scripts calling this variable will need to be updated as well.

</td><td>

[Documentation](https://www.servicenow.com/community/developer-blog/community-code-snippets-variable-and-function-naming/ba-p/2291069)

</td></tr><tr><td>

sn\_SE10103

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Avoid configuring notifications to be sent to a specific user

</td><td>

Important notifications may be not be communicated to the correct user \(they may not be communicated to any user\). This could result in interrupted processes.

</td><td>

Consider sending the notification to a specific group or use derived fields from the record that's triggering the notification.

</td><td>

[Documentation](https://developer.servicenow.com/dev.do%23!/learn/courses/zurich/app_store_learnv2_automatingapps_zurich_automating_application_logic/app_store_learnv2_automatingapps_zurich_notifications/app_store_learnv2_automatingapps_zurich_notifications_objectives)

</td></tr><tr><td>

sn\_SE10104

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Users should not be granted roles directly

</td><td>

Unintended users may have access to certain functionality within the platform.

</td><td>

Consider creating a group, grant the group the desired roles, then associate the group to the user. The user will now inherit the role through the group.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=c_UserAdministration.html)

</td></tr><tr><td>

sn\_SE10118

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Mid server version should match the instance version

</td><td>

Configuration data may not be updated as discovery may not run correctly.

</td><td>

Attempt to auto upgrade the MID Server by using the **Upgrade MID Server** UI Action on the MID Server record. Use the **Validate** UI Action on the MID Server record. If an error occurred, then follow the below instructions. Download the latest MID Server \(in the Downloads module under the MID Server application\). Have your server admin install the latest MID Server zip file on the server. Use the **Validate** UI Action on the MID Server record.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=c_UpgradeAndTestMIDServer.html)

</td></tr><tr><td>

sn\_SE10135

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Workflows should not contain over 30 activities

</td><td>

Increased development time

</td><td>

Consider creating a subflow to remove some of the activities from the main workflow.

</td><td>

[Documentation](https://hi.service-now.com/kb_view.do?sysparm_article=KB0680098)

</td></tr><tr><td>

sn\_SE10136

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Workflows shouldn't call the notification activity

</td><td>

Increased development time and possibly inconsistent email notifications.

</td><td>

Replace the notification activity with a create event activity. Then create a notification based on the event triggered from the workflow.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=c_NotificationActivities.html)

</td></tr><tr><td>

sn\_SE10137

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Workflows should not contain over 3 branch activities

</td><td>

Workflows may break during execution resulting in incomplete processes.

</td><td>

Consider creating a subflow to remove some of the branch activities from the main workflow.

</td><td>

[Documentation](https://hi.service-now.com/kb_view.do?sysparm_article=KB0680098)

</td></tr><tr><td>

sn\_SE10145

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

UI Pages shouldn't have the same name as a table \(and vice versa\)

</td><td>

Can cause confusion when referencing the name of the table or the UI page.

</td><td>

Rename the UI Page to a unique name, since the Table name is an autogenerated value.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=r_UIPages.html)

</td></tr><tr><td>

sn\_SE10241

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Discovery schedule names should be related to what is being discovered

</td><td>

Saves time in administration of discovery by alleviating need to manually search schedules for specific targets or segments

</td><td>

Rename discovery schedules to reflect either the network segment in-scope, or items expected to be discovered.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=t_CreateADiscoverySchedule.html)

</td></tr><tr><td>

sn\_SE10244

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

UI Actions should have defined conditions for visibility

</td><td>

Prevents accidental running of UI Actions that could affect data

</td><td>

Edit the UI Action and provide conditions for when UI action should be visible.

</td><td>

[Documentation](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0546781)

</td></tr><tr><td>

sn\_SE10245

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

UI Actions should be kept simple

</td><td>

Simplifies maintenance and development of UI Actions

</td><td>

Create a business rule for advanced and complex logic. Edit the UI Action and reduce script complexity, calling a script include, or allowing business rule to react instead.

</td><td>

[Documentation](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0546781)

</td></tr><tr><td>

sn\_SE10252

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Scripts should not use gs.sql

</td><td>

Functionality may be impacted, resulting in poor user experience.

</td><td>

Convert any uses of **gs.sql** to **GlideRecord**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=p_GlideServerAPIs.html)

</td></tr><tr><td>

sn\_SE10254

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Script Include names should be unique

</td><td>

Functionality may be broken causing a poor user experience.

</td><td>

Take the newer script include \(or least used script include\) and rename it so it has a unique API Name. Any scripts referencing this script include will need to be updated to reference the new api name.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=c_ScriptIncludes.html)

</td></tr><tr><td>

sn\_SE10257

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Consider moving to the 2011 SLA Engine

</td><td>

Less control over SLA definitions that may result in inaccurate SLA calculations.

</td><td>

Set the value of the **com.snc.sla.engine.version** system property to 2011. Note: Activating the 2011 SLA engine will deactivate all business rules on the **task\_sla** table \(except for the rule Task SLA Empty Schedule Warning, which is part of the 2011 engine\). If you have added any additional business rules or customized the default business rules, these will not be automatically deactivated.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=t_MoveFromThe2010ToThe2011Engine.html)

</td></tr><tr><td>

sn\_SE10260

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

An item in the Product Catalog should be linked to a Product Model

</td><td>

Less visibility into the management of your assets

</td><td>

Create or associate an existing Product Model to the Product Catalog Item.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=c_ManagingProductCatalogItems.html)

</td></tr><tr><td>

sn\_SE10261

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

The newest version of Agile Development should be utilized

</td><td>

Possibility of not being able to utilize new features that could result in reduced development/management time.

</td><td>

Review Agile Development 2.0 to determine if it will be a good fit for your company's agile process.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=agile-landing-page.html)

</td></tr><tr><td>

sn\_SE10265

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Scheduled Jobs should not be run with inactive users.

</td><td>

Unnecessary burden on the system.

</td><td>

Determine if the scheduled job still needs to be run and if so update the Run As field to be an active user.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=t_ScheduleAScriptExecution.html)

</td></tr><tr><td>

sn\_SE10268

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Unsupported property "glide.ui11.show\_switch\_link" should not be set to true

</td><td>

Unexpected behavior that may result in invalid data or poor user experience.

</td><td>

Set the "**glide.ui11.show\_switch\_link**" property value to **false**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=r_AvailableSystemProperties.html)

</td></tr><tr><td>

sn\_SE10272

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Custom tables should not be extended from the Catalog Task, Problem, Change Request, or Incident.

</td><td>

Unnecessary time spent during upgrades.

</td><td>

Reevaluate the requirements behind this and remove the extended tables; process-related needs should be addressed by standardizing processes at the organizational level, with required data captured in variables rather than custom table attributes, and non-ITSM use cases \(e.g., Facility Problems, Changes, or Incidents\) implemented as custom apps or via existing &lt;ph conref="../reusables/conrefs.dita\#conrefs/company-no-reg-tm"/&gt; store applications.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=t_TableExtensionExample.html)

</td></tr><tr><td>

sn\_SE10283

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Variable Validation Regex should be used for data validation

</td><td>

Having a consistent method to validate your data will improve user experience.

</td><td>

Consider using Variable Validation Regex records to configure common data validation within the service catalog.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=define-regex-vrble.html)

</td></tr><tr><td>

sn\_SE10286

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Service Catalog User Criteria should be enabled

</td><td>

Less configuration and setup for service catalog access resulting in lower risk deployments.

</td><td>

Enable user criteria on your system by setting the service catalog property **__glide.sc.use\_user\_criteria__** to **true**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=c_MigrtSvcCatUserCriteria.html)

</td></tr><tr><td>

sn\_SE10288

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Transform maps should not have boolean fields in their import set table

</td><td>

Possibility of inaccurate data in the system.

</td><td>

Replace the True/False field on the import set table to string field and write the transformation script to populate the value on the target record if needed. This will make sure if this field is not part of the data provided for update, it won't be modified on the target record.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=t_CreateATransformMap.html)

</td></tr><tr><td>

sn\_SE10290

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Knowledge Articles with "Valid to" date in the past

</td><td>

Relevant articles may become expired or irrelevant articles may be maintained in the Knowledge Base.

</td><td>

Review any identified knowledge articles in this situation and update the "Valid To" date or retire the knowledge article.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=article-validity.html)

</td></tr><tr><td>

sn\_SE10291

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Duplicate fields on one form

</td><td>

Inaccurate data and user frustration.

</td><td>

Review and remove any duplicate form fields, as this could cause issues with saving.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=configure-form-layout.html)

</td></tr><tr><td>

sn\_SE10292

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Enable unique number indexing

</td><td>

Duplicate numbers can cause confusion and errors.

</td><td>

Enable a unique index on this table. Navigate to System Definition &gt; Tables, select the table of this scanned record, navigate to the Database Indexes related list and select New, then check the "Unique Index" box, move the "number" field into the selected box and press "Create Index".

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=c_EnforcingUniqueNumbering.html)

</td></tr><tr><td>

sn\_SE10294

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Strict mode should be enabled for GlideRecord queries

</td><td>

Unintended or unexplainable side effects from the use of allowing invalid queries.

</td><td>

Navigate to **sys\_properties** and add or review the property "**glide.invalid\_query.returns\_no\_rows**". Ensure the property value is set to **true**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=c_GlideRecordScopedAPI.html)

</td></tr><tr><td>

sn\_SE10299

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

All events should have a description

</td><td>

Having an event with an empty description will cause the purpose to be unclear.

</td><td>

Populate the Description field.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=t_RegisterAnEvent.html)

</td></tr><tr><td>

sn\_SE10300

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Reports with duplicate name

</td><td>

Increased confusion and corruption in the report library.

</td><td>

Consider using a unique naming convention for reports.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=c_GenerateReports.html)

</td></tr><tr><td>

sn\_SE10301

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Do not use ^NQ in a before query business rule

</td><td>

The NQ \(top-level OR\) operator will OR all previous query terms with following query terms. This may alter the results of the original query itself.

</td><td>

Remove the ^NQ \(top level OR\) from the script field. This might require refactoring the business rule to use a different approach.

</td><td>

[Documentation](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0564887)

</td></tr><tr><td>

sn\_SE10302

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Scripted REST service and their resources should have meaningful short descriptions

</td><td>

It may be difficult to find a specific scripted REST service without a short description.

</td><td>

Fill in the short description field on these resources for documentation purposes.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=t_CreateAScriptedRESTAPIResource.html)

</td></tr><tr><td>

sn\_SE10304

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Events should have the "Fired by" field populated

</td><td>

It may be difficult to track the business rule that runs the event without the Fired by field.

</td><td>

Populate the Fired by field with the name of the business rule that runs the event.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=t_RegisterAnEvent.html)

</td></tr><tr><td>

sn\_SE10305

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Dictionary entry present for a table that does not exist

</td><td>

Increased development/troubleshooting time.

</td><td>

Deactivate the orphaned dictionary entry.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=c_SystemDictionary.html)

</td></tr><tr><td>

sn\_SE10306

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

Enable LDAP listener

</td><td>

The instance may not receive information about users' accounts until the next scheduled refresh resulting in outdated user data.

</td><td>

Set the Listener flag on the record to **true**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=t_EnableAListener.html)

</td></tr><tr><td>

sn\_SE10307

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

JavaScript Mode should not be set to Compatibility Mode for Applications

</td><td>

Errors may slip through undetected with Compatibility Mode.

</td><td>

Set the JavaScript mode to ES5 Standards if editing a global application or to ECMAScript 2021 \(ES12\) if using a scoped application. Compatibility mode should not be selected.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=c_JS_modes.html)

</td></tr><tr><td>

sn\_SE10415

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Author elective updates should be processed from Store apps

</td><td>

If the property value is false, Deletes in your author\_elective\_update folder will not be written as Skip records in the Upgrade History entry for application upgrades.

</td><td>

Either create or update the system property "com.**glide.apps.include\_my\_deletes**" with the value of **true**.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=generation-skip-records-app-installs.html)

</td></tr><tr><td>

sn\_SE10451

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

REST Web Services should not write data directly

</td><td>

Scripted REST web services simply provide an interface for a transaction rather than maintaining CRUD operations. Maintaining these operations is more difficult within a web service as opposed to a script include.

</td><td>

Use a script include rather than a scripted REST web service to conduct CRUD operations.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=c_CustomWebServices.html)

</td></tr><tr><td>

sn\_SE10454

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

User defined in the "Run as" field is inactive or not valid

</td><td>

Scheduled job may not run as expected with invalid/inactive user credentials.

</td><td>

Update the "Run as" field to a different user, or ensure that the user record is active and the "User ID" field is populated.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=t_CreatASchedDataCollJob.html)

</td></tr><tr><td>

sn\_SE10456

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

SOAP Web Services should not write data directly

</td><td>

Scripted SOAP web services simply provide an interface for a transaction rather than maintaining CRUD operations. Maintaining these operations is more difficult within a web service as opposed to a script include.

</td><td>

Use a script include rather than a scripted SOAP web service to conduct CRUD operations.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=c_ScriptedWebServices.html)

</td></tr><tr><td>

sn\_SE10464

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Active Task SLA Definitions for Vulnerable Item \(VIT\) record

</td><td>

May cause unexpected behavior within the instance.

</td><td>

Disable all Task SLA definitions.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=t_CreateVulnSLA.html)

</td></tr><tr><td>

sn\_SE10477

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

gs.now\(\) should no longer be used in scripts

</td><td>

The gs.now\(\) call is unsupported and may cause unexpected behavior.

</td><td>

Replace "**gs.now**\(\)" with new "**GlideDate\(\).getDisplayValue\(\)**".

</td><td>

[Documentation](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0594666)

</td></tr><tr><td>

sn\_SE10481

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

The sys\_update\_xml table exceeds the recommended threshold

</td><td>

Performance issues may arise during upgrades.

</td><td>

Group the **sys\_update\_xml** table by the "Type" column, and take note of the largest groups. Often, there will be just one or two update types constituting the majority of the records. Once you have identified the type\(s\) of updates contributing the most, determine if those updates could be a result of some customization. If that's the case, recreate the table without extending **sys\_metadata**, or figure out a way to avoid creating/deleting records on it so frequently. There could also be a custom script responsible for the excess updates. Disable the customization and carefully clean up the excess records that were generated. If you are unable to identify the cause, contact &lt;ph conref="../reusables/conrefs.dita\#conrefs/company-no-reg-tm"/&gt; support for assistance.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=r_CustomerUpdatesTable.html)

</td></tr><tr><td>

sn\_SE10482

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

Checks for direct calls to Java packages

</td><td>

Additional impact to database server which may impact other processes.

</td><td>

It is recommended to run the Package Call Removal Tool, and replace all Java package calls with the Glide alternative.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=c_PackagesCallRemovalTool.html)

</td></tr><tr><td>

sn\_SE10484

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Checks if ATF test/test suite execution is enabled on non-production instances

</td><td>

Without ATF, testing may not be performed to ensure important functionality behaves as expected.

</td><td>

Navigate to Automated Test Framework &gt; Administration &gt; Properties, then select the property "Enable test/test execution suite".

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=atf-enable-tests.html)

</td></tr><tr><td>

sn\_SE10485

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Can Contribute / Cannot Contribute user criteria should be defined on each knowledge base

</td><td>

Any user would be able to contribute content when no user criteria is defined.

</td><td>

Define Can Contribute or Cannot Contribute user criteria for each knowledge base.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=select-user-criteria-for-knowledge-block.html)

</td></tr><tr><td>

sn\_SE10486

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Check for server/client scripts that differ from baseline

</td><td>

Prevent scripts from unnecessary skips during upgrade.

</td><td>

Review the changes to these server/client scripts and revert to the baseline version if appropriate. Otherwise, thoroughly test after an upgrade.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=upgrademon-process-skip-list.html)

</td></tr><tr><td>

sn\_SE10487

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

Check for usage of an unsupported API

</td><td>

APIs that are no longer supported may behave unexpectedly.

</td><td>

Replace unsupported API calls with supported APIs such as **GlideQueryGlobalAPI** or **GlideRecordAPI**. Alternatively, search from the **sys\_dictionary** table for field validation.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=api-server.html)

</td></tr><tr><td>

sn\_SE10496

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

HR Template has an assignment group mapping that will conflict with Assignment Rules

</td><td>

HR users without the required skills may be assigned to a case.

</td><td>

Review the HR Template and remove the group if needed or disable the assignment rule if that is no longer needed.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=configure-hr-case-template.html)

</td></tr><tr><td>

sn\_SE10528

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

Minimize canceled discoveries

</td><td>

Vital discovery schedules and processes may be canceled if the max run-time value is reached. Not completing Discovery will lead to innacurate data in the CMDB.

</td><td>

Schedule discoveries during times that are offset, allocate more resources, or increase the defined maximum run time.

</td><td>

[Documentation](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0676340)

</td></tr><tr><td>

sn\_SE10530

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Breakdowns should be named uniquely

</td><td>

Users may get confused on the correct Breakdown to use for Indicators due to duplicate names.

</td><td>

Rename the Breakdown with an appropriate and unique name.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=t_CreatingABreakdownForIndicators.html)

</td></tr><tr><td>

sn\_SE10531

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

Collection job without indicators

</td><td>

Jobs without indicators may be inefficiently collecting non-relevant data.

</td><td>

In the Indicators tab, select the name of the job indicator that you want to configure or define a new one.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=configure-job-indicator.html)

</td></tr><tr><td>

sn\_SE10532

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

Indicator used in multiple active collection jobs

</td><td>

The collection job may collect irrelevant data.

</td><td>

Review the idicators defined in collection jobs to ensure they are not defined for multiple jobs.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=configure-job-indicator.html)

</td></tr><tr><td>

sn\_SE10544

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Dashboards should have at least one tab

</td><td>

Content may become disorganized without the use of tabs.

</td><td>

Investigate the root cause for the dashboard to have no tabs. If the dashboard was transported using Update Sets, make sure you follow the steps provided in the documentation to unload all the required pieces. Else select the configuration icon on a dashboard to open the Configuration pane, then select Create Tab.

</td><td>

[Documentation](http://docs.servicenow.com/csh?topicname=t_MoveDashboardWithUpdateSet.html)

</td></tr><tr><td>

sn\_SE10546

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Ensure default states are used for releases

</td><td>

Custom states can be difficult to maintain/enforce if documentation is not created for them.

</td><td>

Use the default states on the Releases table.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=default-state-categories-for-release-and-release-task-tables.html)

</td></tr><tr><td>

sn\_SE10547

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Avoid using non-internationalized strings in HTML templates.

</td><td>

Use the $\{\} or gs.getMessage\(\) syntax in the HTML Template, Client Script, or Server Script fields of a widget to tag strings for translation so you can localize your Service Portal content.

</td><td>

Use the $\{\} or **gs.getMessage**\(\) syntax in the HTML Template, Client Script, or Server Script fields of a widget to tag strings for translation so you can localize your Service Portal content.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=c_WidgetLocalization.html)

</td></tr><tr><td>

sn\_SE10550

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Baseline HR States have been modified

</td><td>

Custom states can be difficult to maintain/enforce if documentation is not created for them.

</td><td>

Use the default states for HR-related records.

</td><td>

[Documentation](https://docs.servicenow.com/csh?topicname=c_BPForStateFieldChoiceValues.html%23t_StateModificationExamples)

</td></tr><tr><td>

sn\_SE10552

</td><td>

1

</td><td>

Review

</td><td>

 

</td><td>

Workflow\(s\) checked out for an extended time

</td><td>

Workflow\(s\) checked out for an extended time period represent either abandoned work or data sanitation that is not being completed.

</td><td>

Publish the workflows which are checked out for more than 7 days.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=workflow-editor.html)

</td></tr><tr><td>

sn\_SE10553

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Breakdown sources should have valid Facts table and field values

</td><td>

Using a non-valid facts table or field value will result in unexpected data collection.

</td><td>

For the Facts Table, select the table that the breakdown source gets elements from. In the Field table, select a field that contains a unique value for every record.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=t_DefiningABreakdownSource.html)

</td></tr><tr><td>

sn\_SE10554

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Interactive filters that are based on a reference should be mapped to a reference table and field

</td><td>

The interactive filter will be incomplete and not reference specific reports/fields without a reference.

</td><td>

Add a mapping to the interactive filter on the "Interactive Filter References" related list.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=t_CreateAReferenceFieldPublisher.html)

</td></tr><tr><td>

sn\_SE10555

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

Report assigned to a user which is not active

</td><td>

The user will not receive the report since they are inactive.

</td><td>

Activate the user or assign the report to an already active user.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=t_ShareASetting.html)

</td></tr><tr><td>

sn\_SE10556

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

Widget with an automated indicator that is no longer scheduled

</td><td>

The widget will no longer display accurate or timely data that the automated indicator collects.

</td><td>

Re-schedule the automated indicator so that it continues to run.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=t_CreateAnAutomatedIndicator.html)

</td></tr><tr><td>

sn\_SE10557

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

Unused breakdown source

</td><td>

Data collected by the breakdown source serves no purpose as it is not used by any breakdowns.

</td><td>

Create a breakdown that uses the breakdown source or remove the breakdown source. If not needed, delete the breakdown source.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=t_DefiningABreakdownSource.html)

</td></tr><tr><td>

sn\_SE10558

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Active HR Record Producer must have Category and Catalog defined to show up in HR portal and Search

</td><td>

The record producer would not appear on the portal if the category and catalog are not populated

</td><td>

Add a category and catalog to the record producer.

</td><td>

[Documentation](https://docs.servicenow.com/csh?topicname=configure-hr-service.html%23configure-hr-service)

</td></tr><tr><td>

sn\_SE10560

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

Reports should not be shared with roles that have no users

</td><td>

No users would receive the report since there are no users assigned the role defined in the report.

</td><td>

Assign the role to the users which need access to the report.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=t_ShareASetting.html)

</td></tr><tr><td>

sn\_SE10561

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Scoped app uses logging utils or depreciated methods for logging rather than the verbosity method.

</td><td>

Restricted to only global scope and inaccessible from a private application scope.

</td><td>

Use **gs.error**, **gs.warn**, **gs.info** or **gs.debug**.

</td><td>

[Documentation](https://www.servicenow.com/community/developer-forum/how-to-add-logging-for-a-scoped-application/m-p/1897357)

</td></tr><tr><td>

sn\_SE10562

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

Use Notification Categories

</td><td>

Users have the option to subscribe or unsubscribe to notifications based on the category. Having these values will allow users to self-service their notification preferences.

</td><td>

Add a category value to the notification.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=create-notification-categories.html)

</td></tr><tr><td>

sn\_SE10564

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Duplicate foundation/core data found.

</td><td>

Duplicate data may create confusion for CSM admins and users.

</td><td>

Review the duplicate data and remove data that is deemed as unnecessary.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=configure-csm-foundation-data.html)

</td></tr><tr><td>

sn\_SE10565

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Business rules "Copy Incident State to State" &amp; "Copy State to Incident State" should remain active

</td><td>

Avoid issues if you use the "State" or "Incident State" fields on the Incident form while creating or updating an incident record because both of these fields are synced in the back end. The fields are synced only when the following business rules are activated: Copy State to Incident State Copy Incident State to State

</td><td>

Re-activate these business rules: "Copy Incident State to State" and "Copy State to Incident State". If they have been removed, obtain copies from another instance.

</td><td>

[Documentation](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0697327)

</td></tr><tr><td>

sn\_SE10566

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

Workflow activity references an empty or invalid group

</td><td>

Activities that run a script, send notifications, or request approvals will not execute as expected and will point to the invalid or empty group. This can cause objects created by these activities to be lost.

</td><td>

Make sure the correct group is assigned to the activity and that there are active users in the group.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=wf-activity-overview.html)

</td></tr><tr><td>

sn\_SE10569

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

No breakdown mapping found for breakdown

</td><td>

Without a breakdown mapping, the breakdown cannot be used

</td><td>

Create a breakdown mapping.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=t_CrtBkdnBreakdownMpngs.html)

</td></tr><tr><td>

sn\_SE10570

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

Avoid use of inline templates in widgets

</td><td>

Might increase the likelihood of production issues in Service Portal

</td><td>

Create a related Angular ng-template record for the widget.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=widget-best-practices.html)

</td></tr><tr><td>

sn\_SE10572

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

Report shared with a group which has no users

</td><td>

Either the correct users should have access to this report, or the report is no longer needed. If an organizational change is not correctly reflected in your groups and sharing for these reports, the users who need them will likely request new reports, leading to duplification. A large number of reports adds overhead for the system and administrators.

</td><td>

Investigate this Report to ensure that the group sharing on this report is accurate. Deactivate the report if nobody requires access to it. Investigate this Group to ensure that any recent organizational changes didn't orphan it.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=t_ShareASetting.html)

</td></tr><tr><td>

sn\_SE10573

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

Core fields on the Incident table should be read-only

</td><td>

If the auto-generated information that is captured within an incident is edited, then that could cause confusion and data loss.

</td><td>

-   The following fields should always be read-only on Incident:.
-   Number.
-   Opened.
-   Opened by.
-   Updated by.
-   Resolved by.
-   Closed.
-   Closed by.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=create-an-incident.html)

</td></tr><tr><td>

sn\_SE10576

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

Indicators should have unique names

</td><td>

Duplicate indicator names may cause confusion and become harder to maintain.

</td><td>

Ensure indicators have unique names.

</td><td>

[Documentation](https://www.servicenow.com/community/performance-analytics-blog/make-life-easy-quot-create-unique-names-quot/ba-p/2272116)

</td></tr><tr><td>

sn\_SE10579

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Data Collector jobs with errors or warnings

</td><td>

Important benchmark data may not be captured with errors or warnings present.

</td><td>

Review and resolve outstanding errors and warnings within the data collector job.

</td><td>

[Documentation](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0725151)

</td></tr><tr><td>

sn\_SE10580

</td><td>

1

</td><td>

Review

</td><td>

 

</td><td>

Consider making fields on the Change Task table mandatory

</td><td>

Without mandatory fields, data collection on the Change Task table can be less effective, leading to incomplete or inconsistent information.

</td><td>

-   Make the following fields mandatory on the Change Task table:.
-   Configuration Item.
-   Planned Start Date.
-   Planned End Date.
-   Assignment Group.
-   Short Description.
-   Description.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=t_MakingAFieldMandatory.html)

</td></tr><tr><td>

sn\_SE10581

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

All interactive filters that are based on a cascading filter should be mapped to cascading filter

</td><td>

The interactive filter will be incomplete and not reference specific reports/fields without the cascading filter.

</td><td>

Add a mapping to the interactive filter on the "Cascading Filter" related list.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=create-cascading-filter.html)

</td></tr><tr><td>

sn\_SE10584

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Check for automatic indicators with no scores entered

</td><td>

Indicators that lack scores aren't serving their purpose of providing a metric for business processes.

</td><td>

Review and resolve automatic indicators that are not entering scores.

</td><td>

[Documentation](https://docs.servicenow.com/csh?topicname=t_CreateAnAutomatedIndicator.html)

</td></tr><tr><td>

sn\_SE10586

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

sn\_grc\_metric\_base\_definition table field Deprecation

</td><td>

From Vancouver release, the 'latest\_data' &amp; 'previous\_data' in sn\_grc\_metric\_base\_definition &amp; sn\_grc\_metric\_metric will be deprecated.

</td><td>

Set up percentage-based thresholds for metric data. Use the new role **sn\_grc\_metric**.developer to edit the script in automated metric definition.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=rn-summary-removed-features.html)

</td></tr><tr><td>

sn\_SE10588

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

GlideEncrypter Deprecation

</td><td>

Beginning with the Vancouver family release, the GlideEncrypter API is not recommended for use, as this API is deprecated according to NIST guidelines

</td><td>

Consider using **GlideElement** API or the Key Management Framework as alternatives.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=GlideEncrypterAPI.html)

</td></tr><tr><td>

sn\_SE10589

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Workforce Optimization for ITSM

</td><td>

System errors and performance degradation may occur due to unnecessary conditional checks

</td><td>

-   Migrate the data for the fields.
-   Manager Access.
-   Allow Agent Create.
-   Allow Agent Edit.
-   Allow Agent Delete.
-   Access control for event types should now be performed by using User Criteria.

</td><td>

[Documentation](https://docs.servicenow.com/csh?topicname=include-or-exclude-user-access-for-event-types.html)

</td></tr><tr><td>

sn\_SE10590

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Deprecation of Instance Security Center

</td><td>

Instance Security Center \(ISC\) will reach the end of sales by September 2024. SSC is the recommended solution going forward.

</td><td>

Get the application Security Center from &lt;ph conref="../reusables/conrefs.dita\#conrefs/company-no-reg-tm"/&gt; store.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=instance-security-center-to-security-center-migration.html)

</td></tr><tr><td>

sn\_SE10591

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Table m2m\_user\_consent\_info will be deprecated &amp; migrated to sys\_analytics\_user\_consent\_decision

</td><td>

The deprecation and migration of the m2m\_user\_consent\_info table to sys\_analytics\_user\_consent\_decision in ServiceNow 's Vancouver release may require updates to custom applications and data migration, impacting compatibility and reporting functionalities.

</td><td>

Consider using the new table **sys\_analytics\_user\_consent\_decision** instead of the deprecated m2m\_user\_consent\_info.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=rn-summary-removed-features.html)

</td></tr><tr><td>

sn\_SE10598

</td><td>

1

</td><td>

Review

</td><td>

 

</td><td>

Article paragraph too lengthy

</td><td>

Lengthy paragraphs can overwhelm AI and result in fragmented or unclear summaries.

</td><td>

Separate lengthy paragraphs into multiple paragraphs and consider shortening paragraphs to the most relevant information.

</td><td>

[Documentation](https://www.servicenow.com/community/knowledge-management-articles/best-practices-to-use-your-knowledge-articles-with-now-assist/ta-p/2824219)

</td></tr><tr><td>

sn\_SE10617

</td><td>

1

</td><td>

Review

</td><td>

 

</td><td>

Now Assist works best when articles are complete with Ownership Groups

</td><td>

Knowledge articles are poorly maintained with no clear owners.

</td><td>

Check that **sys\_property** **__glide.knowman.ownership\_group.enabled__** exists and is set to "**true**". Create and/or change if necessary.

</td><td>

[Documentation](https://www.servicenow.com/community/knowledge-management-articles/best-practices-to-use-your-knowledge-articles-with-now-assist/ta-p/2824219)

</td></tr><tr><td>

sn\_SE10620

</td><td>

1

</td><td>

Review

</td><td>

 

</td><td>

Stale Article Metrics

</td><td>

The "Valid To" field on knowledge articles controls whether articles can be browsed, searched, and used by generative AI. Articles not being updated may contain outdated information.

</td><td>

The **Valid To** date should ideally be set to less than 1 year into the future. On a periodic basis, have the article author or a member of the ownership group look through these articles to determine if they are relevant or need updates.

</td><td>

[Documentation](https://www.servicenow.com/community/knowledge-management-articles/best-practices-to-use-your-knowledge-articles-with-now-assist/ta-p/2824219)

</td></tr><tr><td>

sn\_SE10622

</td><td>

1

</td><td>

Review

</td><td>

 

</td><td>

View Metrics

</td><td>

Articles which aren't being used very often may have outdated information and they needlessly take up space in the database.

</td><td>

Review articles with fewer views to ensure the content is relevant and up-to-date. Consider retiring articles with no views.

</td><td>

[Documentation](https://www.servicenow.com/community/knowledge-management-articles/best-practices-to-use-your-knowledge-articles-with-now-assist/ta-p/2824219)

</td></tr><tr><td>

sn\_SE10623

</td><td>

1

</td><td>

Review

</td><td>

 

</td><td>

Articles with images should have alternative text.

</td><td>

Users with accessibility needs, such as visual disabilities, may not be able to view images and videos without the alternate text.

</td><td>

Locate images in knowledge articles and ensure the attribute alternative description is populated with meaningful text.

</td><td>

[Documentation](https://www.servicenow.com/community/knowledge-management-articles/best-practices-to-use-your-knowledge-articles-with-now-assist/ta-p/2824219)

</td></tr><tr><td>

sn\_SE10624

</td><td>

1

</td><td>

Review

</td><td>

 

</td><td>

Article with No Meta and No Tags

</td><td>

Article relevancy may be under or over stated without use of meta tags to help with relevancy.

</td><td>

Create tags that match the user's potential query and enter them in to the Meta field on the Knowledge form.

</td><td>

[Documentation](https://www.servicenow.com/community/knowledge-management-articles/best-practices-to-use-your-knowledge-articles-with-now-assist/ta-p/2824219)

</td></tr><tr><td>

sn\_SE10625

</td><td>

1

</td><td>

Review

</td><td>

 

</td><td>

Reduce creation of duplicate articles as much as possible

</td><td>

Generative AI responses will be skewed, giving more importance to duplicated data than is desired.

</td><td>

Locate duplicate knowledge articles and consolidate them. Make use of user criteria. If you need to show articles in multiple places, consider using Unified Taxonomy in Employee Center.

</td><td>

[Documentation](https://www.servicenow.com/community/knowledge-management-articles/best-practices-to-use-your-knowledge-articles-with-now-assist/ta-p/2824219)

</td></tr><tr><td>

sn\_SE10626

</td><td>

1

</td><td>

Review

</td><td>

 

</td><td>

Knowledge blocks don't work with Now Assist, don't use in articles with Now Assist

</td><td>

Now Assist can't properly parse content in knowledge blocks, so they need to be removed and the functionality replaced with field-level security. This can be templatized using article templates

</td><td>

remove knowledge blocks from flagged articles. Replace with field-level security via article templates if desired.

</td><td>

[Documentation](https://www.servicenow.com/community/knowledge-management-articles/best-practices-to-use-your-knowledge-articles-with-now-assist/ta-p/2824219)

</td></tr><tr><td>

sn\_SE10629

</td><td>

1

</td><td>

Recommend

</td><td>

 

</td><td>

Do not use gs.nowDateTime\(\) to set a GlideDateTime object.

</td><td>

Do not use gs.nowDateTime\(\) to set a GlideDateTime object. The nowDateTime\(\) method returns the date time in local format and the local time zone. The GlideDateTime object uses the date time in the internal format and UTC time zone.

</td><td>

Replace var gdt = new **GlideDateTime**\(**gs.nowDateTime**\(\)\); with var gdt = new **GlideDateTime\(\)**;.

</td><td>

[Documentation](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0594666)

</td></tr><tr><td>

sn\_SE10630

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

FD\_DATA References Non-Existent Fields or Objects

</td><td>

This will result in errors and incorrect data retrieval.

</td><td>

Update the object name or field name in the flow step script.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=inline-scripts.html)

</td></tr><tr><td>

sn\_SE10631

</td><td>

1

</td><td>

Act

</td><td>

 

</td><td>

Invalid Column in Flow or Action

</td><td>

This will result in undefined data if the field does not exist in the table.

</td><td>

Update the field name in the flow step script.

</td><td>

[Documentation](https://www.servicenow.com/docs/csh?topicname=inline-scripts.html)

</td></tr><tr><td>

sn\_SE10632

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Missing description in flow and/or hierarchy items

</td><td>

Missing descriptions might cause confusion as to what the purpose of the flow/subflow/action is

</td><td>

Flows, Subflows, and Actions should contain descriptions.

</td><td>

[Documentation](https://www.servicenow.com/community/workflow-automation-articles/flows-best-practices-general-workflow-automation-coe/ta-p/2359985)

</td></tr><tr><td>

sn\_SE10634

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Too many actions in a single flow

</td><td>

If a flow contains more than 25 actions, it would make it less readable and less reusable

</td><td>

If a flow contains more than 25 actions, consider using a subflow instead of the actions.

</td><td>

[Documentation](https://www.servicenow.com/community/workflow-automation-articles/flows-best-practices-general-workflow-automation-coe/ta-p/2359985)

</td></tr><tr><td>

sn\_SE10635

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Legacy "Send Email" action in a flow

</td><td>

Using the newer "Send Notification" action is preferred over the legacy "Send Email" action.

</td><td>

Using the newer "Send Notification" action is preferred over the legacy "Send Email" action.

</td><td>

[Documentation](https://www.servicenow.com/community/workflow-automation-articles/flows-best-practices-general-workflow-automation-coe/ta-p/2359985)

</td></tr><tr><td>

sn\_SE10636

</td><td>

1

</td><td>

Suggest

</td><td>

 

</td><td>

Missing log step in flow

</td><td>

Missing log would make debugging challenging

</td><td>

Add a LOG step to each branch of a flow to make debugging easier.

</td><td>

[Documentation](https://www.servicenow.com/community/workflow-automation-articles/flows-best-practices-general-workflow-automation-coe/ta-p/2359985)

</td></tr></tbody>
</table>