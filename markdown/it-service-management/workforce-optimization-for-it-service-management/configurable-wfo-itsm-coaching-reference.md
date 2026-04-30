---
title: Coaching components in Workforce Optimization for ITSM
description: Workforce Optimization for ITSM installs the roles and tables when you enable the Workforce Optimization for ITSM plugin \(sn\_wfo\_cfg\_itsm\).
locale: en-US
release: xanadu
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Coaching in Workforce Optimization for ITSM, Workforce Optimization for ITSM, IT Service Management]
---

# Coaching components in Workforce Optimization for ITSM

Workforce Optimization for ITSM installs the roles and tables when you enable the Workforce Optimization for ITSM plugin \(sn\_wfo\_cfg\_itsm\).

## Roles

<table id="table_q14_lwc_llb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Coaching Admin \[sn\_coaching.admin\]

</td><td>

Grants administrative rights to create, read, update, and delete \(CRUD\) coaching opportunities, assessments, training, and skills.

</td><td>

-   sn\_coaching.coach
-   sn\_lc.learning\_admin

</td></tr><tr><td>

Coaching Coach \[sn\_coaching.coach\]

</td><td>

Grants administrative rights to create, read, or update coaching opportunities, assessments, training, and skills.

</td><td>

-   sn\_coaching.trainee
-   pa\_viewer
-   sn\_lc.catalog\_manager

</td></tr><tr><td>

Coaching Trainee \[sn\_coaching.trainee\]

</td><td>

Grants access to add training, assessments, and skill records.

</td><td>

-   skill\_user
-   pa\_viewer
-   survey\_reader

</td></tr></tbody>
</table>## Coaching Opportunities

|This coaching opportunity|Triggers when|
|-------------------------|-------------|
|Coaching on Incident SLA Breach|An SLA is breached.|
|Coaching on interaction long call time|A phone call lasts longer than 10 minutes.|
|Coaching on interaction long chat time|A chat interaction lasts longer than 30 minutes.|
|Coaching on interaction long walk-up time|A walk-up interaction lasts longer than 60 minutes.|

## Coaching surveys

|Name|Description|
|----|-----------|
|Phone Quality Survey|Survey associated with the Phone Interaction coaching opportunity. The coach assesses the agent using this survey after the agent completes a phone interaction.|
|Chat Quality Survey|Survey associated with the Chat Interaction coaching opportunity. The coach assesses the agent using this survey after the agent completes a chat interaction.|
|Walk-up Quality Survey|Survey associated with the Walk-up Interaction coaching opportunity. The coach assesses the agent using this survey after the agent completes a walk-up interaction.|

## Business rule

|Business rule|Table|Description|
|-------------|-----|-----------|
|Calculate coaching survey score|Assessment Instance \[asmt\_assessement\_instance\]|Sets the feedback rating based on the survey score.|

## Coaching with Learning

**Important:** This feature is available with the Coaching with Learning plugin \(sn\_coach\_lrn\) from the ServiceNow Store. To enable this feature, see [Activate Workforce Optimization for ITSM configurable workspace](../task/activate-configurable-workforce-optimization-itsm.md).

## Roles in Coaching with Learning

<table id="table_fk4_mwq_npb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains Roles

</th></tr></thead><tbody><tr><td>

Learning admin \[sn\_lc.learning\_admin\]

</td><td>

Grants administrative rights to create, read, update, and delete \(CRUD\) catalog, learning content, roles, and configure learning source.

</td><td>

-   sn\_lc.catalog\_manager
-   sn\_hr.integr\_fw.admin

</td></tr><tr><td>

Learning course catalog admin \[sn\_lc.learning\_course\_catalog\_admin\]

</td><td>

Grants administrative rights to create, read, or update learning course catalogs.

</td><td>

 

</td></tr><tr><td>

Learning catalog manager \[sn\_lc.catalog\_manager\]

</td><td>

Grants administrative rights to create, read, or update learning libraries.

</td><td>

-   sn\_lc.task\_creator
-   sn\_lc.content\_writer

</td></tr><tr><td>

Learning catalog group manager \[sn\_lc.catalog\_group\_manager\]

</td><td>

Grants administrative rights to create, read, or update learning libraries based on groups.

</td><td>

-   sn\_lc.task\_creator
-   sn\_lc.content\_writer

</td></tr><tr><td>

Learning content writer \[sn\_lc.content\_writer\]

</td><td>

Grants read or write access for learning courses.

</td><td>

sn\_lc.content\_creator

</td></tr><tr><td>

Learning content advisor \[sn\_lc.learning\_advisor\]

</td><td>

Can assign learning tasks.

</td><td>

 

</td></tr><tr><td>

Learning task creator \[sn\_lc.task\_creator\]

</td><td>

Grants read or write access for learning tasks.

</td><td>

 

</td></tr></tbody>
</table>## Tables in Coaching with Learning

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Learning External Content\[sn\_lc\_external\_content\]

</td><td>

Stores details of external course items that are pulled from third-party systems.

</td></tr><tr><td>

Learning User Course Activity\[sn\_lc\_user\_course\_activity\]

</td><td>

Stores details of learning course activities such as user to whom the course is assigned, status, due date, and name of the learning course.

</td></tr><tr><td>

Learning Content\[sn\_lc\_content\]

</td><td>

Stores details of internal learning content such as knowledge articles, videos that are created in ServiceNow.

</td></tr><tr><td>

Learning Course Item\[sn\_lc\_course\_item\]

</td><td>

Stores details of learning course items, such as the source to which the learning course belongs.

</td></tr><tr><td>

Learning Catalog\[sn\_lc\_catalog\]

</td><td>

Stores details of learning catalog items with its course items.

</td></tr><tr><td>

Learning Task\[sn\_lc\_learning\_task\]

</td><td>

Stores details of learning tasks, such as user to whom the learning task assigned, and due date by when the learning task must be completed.

</td></tr><tr><td>

Learning System Configuration\[sn\_lc\_learning\_system\_configuration\]

</td><td>

Stores configuration parameters of sources \(third-party learning management systems\).

</td></tr></tbody>
</table>## Properties in Coaching with Learning

<table id="table_bzr_kkw_dpb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

glide.ui.sn\_coaching\_assessment\_activity.fields

</td><td>

Edit coaching assessment activities.-   **Type:** string
-   **Default value:** assigned\_to,cmdb\_ci,state,impact,priority,opened\_by,work\_notes,comments,\*Attachments\*,assessment\_of

</td></tr><tr><td>

sn\_coaching.recommended\_learning\_deprecated

</td><td>

Coaching Recommended Trainings is being deprecated and replaced with the Learning Tasks and course items from Coaching with Learning.-   **Type:** string
-   **Default value:** true

</td></tr><tr><td>

sn\_coach.lrn.exclude\_weekends\_on\_learning\_task\_due\_date

</td><td>

Enable property to exclude weekends while setting the due date for learning tasks.-   **Type:** true\|false
-   **Default value:** true

</td></tr><tr><td>

sn\_coach\_lrn.learning\_list\_menu\_props

</td><td>

Data array properties for the now-list-menu component on the Learning Tasks tab, coaching module.-   **Type:** string
-   **Default value:** script for data array

</td></tr><tr><td>

com.glide.transform.json.max-partial-length

</td><td>

Transforms JSON objects to internal objects and sets the word limit for records fetched through an API call.-   **Type:** integer
-   **Default value:** 16384

 **Note:**

You must [Add this system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US) to set the desired value.

When you [synchronize](../task/integrate-learning-third-party-configurable-wfo-itsm.md) third-party learning content with your ServiceNow instance, if the word count of the content being pulled into your instance exceeds the value set for this property, the synchronization will fail.

</td></tr><tr><td>

com.snc.process\_flow.reporting.serialized.val\_size\_limit

</td><td>

Specify the number of bytes allowed for runtime values in each step in the flow execution details. To prevent truncation, set the value to an integer equal to or less than zero.-   **Type:** integer
-   **Default value:** 16384

 **Note:** When you [synchronize](../task/integrate-learning-third-party-configurable-wfo-itsm.md) third-party learning content with your ServiceNow instance, if the word count of the content being pulled into your instance exceeds the value set for this property, the synchronization will fail.

</td></tr><tr><td>

sn\_coach\_lrn.learningpath\_detail\_viewmore

</td><td>

Number of course item records on learning path page that will display in Service Operations Workspace.  -   **Type:** integer
-   **Default value:** 50

</td></tr><tr><td>

sn\_coach\_lrn.sn\_lc\_enable\_discover

</td><td>

Enables the **Discover** tab in the Service Operations Workspace learning application. -   **Type:** Yes\|No
-   **Default value:** Yes

</td></tr><tr><td>

sn\_coach\_lrn.sn\_lc\_enable\_recommendations

</td><td>

Enables learning path recommendations in the Service Operations Workspace learning application. -   **Type:** Yes\|No
-   **Default value:** Yes

</td></tr></tbody>
</table>## Surveys in Coaching with Learning

|Name|Description|
|----|-----------|
|Phone Quality Survey|Survey associated with the Phone Interaction coaching opportunity. The coach assesses the agent using this survey after the agent completes a phone interaction.|
|Chat Quality Survey|Survey associated with the Chat Interaction coaching opportunity. The coach assesses the agent using this survey after the agent completes a chat interaction.|
|Walk-up Quality Survey|Survey associated with the Walk-up Interaction coaching opportunity. The coach assesses the agent using this survey after the agent completes a walk-up interaction.|

## Recommendation grouping

The recommendation groups listed in the table below are available by default to the logged-in user's primary assignment groups.

**Note:** You can deactivate the recommendations for the recommendation groups provided by default, but you cannot delete them. To deactivate the recommendations, in the Recommendations related list in the Context form, change the **Active** field value to **false**.

You can create additional recommendations and recommendation groups and associate them with recommendation contexts. For more information, see [Recommended Actions application](https://www.servicenow.com/docs/access?context=nba&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)

|Recommendation group name|Recommendation provided based on this criteria|
|-------------------------|----------------------------------------------|
|Based on your work items|The work you’ve done in the past.|
|Based on your team's activity|The activities from the teams to which you belong.|
|Based on your previous courses|Courses you’ve completed in the past.|
|Most popular in your team|Courses that are considered the most popular by your team.|
|New from your library|Courses in your learning library.|
|Most popular in your organization|Courses that are most popular in your organization.|
|New from your catalogs|New courses in your course catalog.|

## Deleting course activity records

Course activity records are used for learning recommendations and are retained for 365 days by default. Do the following to change the number of days, represented as Age in seconds, for which you want to retain the record.

1.  In the application filter navigator, enter `sys_auto_flush.LIST` and press **Enter**. The **Auto Flushes** list displays.
2.  In the **Tablename** column, select the Learning User Course Activity \[sn\_lc\_user\_course\_activity\] table.
3.  In the **Age in seconds** field, change the value to the time you desire to retain the records.

