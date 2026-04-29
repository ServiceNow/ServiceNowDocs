---
title: Coaching with Learning
description: Use Coaching with Learning to train your agents with internal and external learning content. Organize similar content in catalogs. Assign learning tasks and track completion.Create a catalog to organize related content into categories.Create learning tasks for agents to keep track of their learning activities.Add internal courses so that agents can learn new content and enhance their skill set.Add courses from external sources such as Udemy, Pluralsight, or Cornerstone to enable your users to gain skills from external content.
locale: en-US
release: australia
product: Field Service Manager Workforce
classification: field-service-manager-workforce
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Coaching, Workforce Optimization, Managing workforce, Use, Field Service Management]
---

# Coaching with Learning

Use Coaching with Learning to train your agents with internal and external learning content. Organize similar content in catalogs. Assign learning tasks and track completion.

**Important:** Coaching with Learning is available when you enable the Coaching with Learning application from the ServiceNow® Store. To enable this application, see [Activate Workforce Optimization for Field Service](../task/activate-wfo-fsm.md).

## Create a learning library

Create a catalog to organize related content into categories.

### Before you begin

Role required: sn\_lc.catalog\_manager

### Procedure

1.  Navigate to **All** &gt; **Workspaces** &gt; **Manager Workspace**.

2.  Click the Coaching \(![Coaching icon](../../workforce-optimization-for-customer-service-configurable/image/coaching-new.png)\) icon.

3.  Click the **Learning** tab.

4.  Click **Learning libraries** and select **My learning libraries**.

5.  Create a learning library.

    1.  Click **New**.

    2.  In the **Title** field, enter a unique name for the catalog.

    3.  In the **Description** field, enter a description for the catalog.

    4.  Click **Save**.

    **Note:** The catalog is visible to all groups that you directly or additionally manage.

6.  Add course items to the library.

    1.  Click the **Content** tab.

    2.  Click **Add**.

    3.  In the **Add Learning Courses** pop-up window, select all course items you want to add to the catalog.

    4.  Click **Add**.

        The course items are added to the catalog.

    **Note:** To remove any course item you have added, select the course item and click Remove.

7.  Add a group to a library.

    1.  Click the **Applicable Groups** tab.

    2.  Click **New**.

    3.  In the **Group** field, select a group that you want to associate with the catalog.

    4.  Click **Save**.


## Create a learning task

Create learning tasks for agents to keep track of their learning activities.

### Before you begin

Role required: sn\_lc.task\_creator

### About this task

Set learning task completion due dates to include or exclude weekends using the **exclude\_weekends\_on\_learning\_task\_due\_date** system property. For more information, see [Workforce Optimization for Field Service components](../reference/components-wfo-fsm.md).

### Procedure

1.  Navigate to **Workspaces** &gt; **Manager Workspace**.

2.  Click the Coaching icon \(![Coaching icon](../../workforce-optimization-for-customer-service-configurable/image/coaching-new.png)\).

3.  Click **Learning Tasks** and select **All Tasks**.

4.  Create a learning task.

    1.  Click **New**.
    2.  Fill in the following fields.

<table id="table_pr4_zgk_bpb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Assigned to

</td><td>

Name of the agent to whom you want to assign the learning task.

</td></tr><tr><td>

Course item

</td><td>

The course that needs to be completed by the agent.

</td></tr><tr><td>

Due date

</td><td>

Date when the agent must complete the course. Default is 5 days after the creation of the learning task. This value is calculated from the **Days to Complete** field for the course item. The due date field is highlighted as follows:-   Green—if the task is due before the current day.
-   Yellow—if the task is due on the current day.
-   Red—if the task is due after the current day.


</td></tr><tr><td>

Catalog

</td><td>

The catalog that contains the course item for the learning task.

</td></tr></tbody>
</table>5.  Click **Save**.


## Create internal learning content

Add internal courses so that agents can learn new content and enhance their skill set.

### Before you begin

Role required: sn\_lc.content\_creator

### Procedure

1.  Navigate to **All** &gt; **Workspaces** &gt; **Manager Workspace**.

2.  Click the Coaching icon \(![Coaching icon](../../workforce-optimization-for-customer-service-configurable/image/coaching-new.png)\).

3.  Click **Learning Courses** and select **Internal Courses**.

4.  Create an internal learning course.

    1.  Click **Create new course**.
    2.  On the form, fill in the fields.

<table id="table_bdh_5jk_bpb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title

</td><td>

Name of the course.

</td></tr><tr><td>

Internal source

</td><td>

Type of content for the course.Here are the available types of courses:

 -   URL—YouTube, Vimeo, or any link for a video
-   Knowledge article
-   Free form


</td></tr><tr><td>

Days to complete

</td><td>

The number of days required to complete the course. Default value is set to 5.

</td></tr><tr><td>

Course catalog

</td><td>

The catalog associated with the course.

</td></tr><tr><td>

Knowledge article

</td><td>

If the internal source is a knowledge article, select the article.

</td></tr><tr><td>

Estimated duration

</td><td>

Length of time when the course has to be completed. For example, for a video, it is the duration of the video. For a KB article, the duration is estimated based on the length of the article.

</td></tr><tr><td>

Description

</td><td>

Description of the course.

</td></tr></tbody>
</table>5.  Click **Save**.

6.  Add a skill to the internal content.

    1.  Click the **Associated skills** tab.
    2.  Click **New**.
    3.  In the **Skill** field, select a skill you want to associate with the internal content.
    4.  In the **Skill level** field, select a skill level for the selected skill.
    5.  Click **Save**.
7.  Add a learning task to the internal content.

    1.  Click the **Learning Tasks** tab.
    2.  Click **New**.
    3.  In the **Assigned to** field, select a trainee to whom you want to assign the learning task.
    4.  In the **Catalog** field, select the catalog to associate with the learning task.
    5.  In the **Due date** field, click the calendar icon and select the date and time when you want to trainee to complete the learning task.
    6.  Click **Save**.

## Add external courses to coaching with learning

Add courses from external sources such as Udemy, Pluralsight, or Cornerstone to enable your users to gain skills from external content.

### Before you begin

Role required: sn\_lc.learning\_admin

### Procedure

1.  Navigate to **All** &gt; **Workspaces** &gt; **Manager Workspace**.

2.  Click the Coaching icon \(![Coaching icon](../../workforce-optimization-for-customer-service-configurable/image/coaching-new.png)\).

3.  Click the **Learning** tab.

4.  Click **Learning Courses** and select **External Courses**.

5.  Select a course.

6.  Click **Go to course**.


### Result

You can review and learn the external course.

