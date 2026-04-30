---
title: Training your agents using Coaching With Learning
description: Use Coaching with Learning to train your agents with internal and external learning content. Organize similar content in learning libraries. Assign learning tasks and track completion.Create a learning library to organize related content into categories.Add internal courses so that agents can learn new content and enhance their skills set.Add a learning task to an internal content and track the task completion.Add courses from third-party applications such as Udemy, Pluralsight, Cornerstone, or ServiceNow University to enable your users to gain skills from external learning content.Enhance your skills set by completing learning tasks from internal or external learning content.
locale: en-US
release: xanadu
product: Coaching
classification: coaching
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Coaching, IT Service Management]
---

# Training your agents using Coaching With Learning

Use Coaching with Learning to train your agents with internal and external learning content. Organize similar content in learning libraries. Assign learning tasks and track completion.

**Important:** Coaching With Learning is available when you enable the Coaching With Learning application from the ServiceNow® Store. To enable this application, see [Request Coaching](../task/request-coaching.md).

## Organize related learning content

Create a learning library to organize related content into categories.

### Before you begin

Role required: sn\_coaching.coach

### Procedure

1.  Navigate to **All** &gt; **Learning** &gt; **Content** &gt; **Learning Libraries**.

2.  Create a learning library.

    1.  Click **New**.
    2.  In the **Title** field, enter a unique name for the learning library.
    3.  In the **Description** field, enter a description for the learning library.
    4.  Right-click the form header and click **Save**.
    **Note:** The learning library is visible to all groups that you directly or additionally manage.

3.  Add course items to the learning library.

    1.  Click the **Content** related list.
    2.  Click **Add**.
    3.  In the **Add Learning Courses** pop-up window, select all course items you want to add to the learning library.
    4.  Click **Add Selected**. The course items are added to the learning library.
    **Note:** To remove any course item you have added, select the course item and click **Remove**.

4.  Add user to the library.

    1.  Click the **Applicable Users** related list.
    2.  Click **Edit**.
    3.  Move the desired users to the **Applicable Users List** field.
    4.  Click **Save**.

## Add internal learning content

Add internal courses so that agents can learn new content and enhance their skills set.

### Before you begin

Role required: sn\_coaching.coach

### Procedure

1.  Navigate to **All** &gt; **Learning** &gt; **Content** &gt; **Learning Content**.

2.  Create an internal learning content.

    1.  Select **New**.
    2.  Fill in the following fields.

<table><thead><tr><th>

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

Select the type of content for the course.Here are the available types of courses:

 -   URL—Youtube, Vimeo, or any link for a video
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

URL Domain

</td><td>

If the internal source is URL, select the domain for the URL. Here are the available URL domain types:

 -   Youtube
-   Vimeo
-   Other


</td></tr><tr><td>

URL

</td><td>

If the internal source is URL, enter the URL for the selected domain.

</td></tr><tr><td>

Estimated duration

</td><td>

Length of time when the course has to be completed. For example, for a video, it is the duration of the video. For a KB article, the duration is estimated based on the length of the article.

</td></tr></tbody>
</table>3.  Select **Save**.

4.  Add a skill to the internal learning content.

    1.  Select the **Associated skills** related list.
    2.  Select **New**.
    3.  In the **Skill** field, select a skill you want to associate with the internal content.
    4.  In the **Skill level** field, select a skill level for the selected skill.
    5.  Select **Save**.

### Add a learning task to the internal content

Add a learning task to an internal content and track the task completion.

#### Before you begin

Role required: sn\_coaching.coach

#### Procedure

1.  Navigate to **All** &gt; **Learning** &gt; **Content** &gt; **Learning Content**.

2.  Add a learning task to the internal learning content.

    1.  Select the **Learning Tasks** related list.
    2.  Select **New**.
    3.  In the **Assigned to** field, select a trainee to whom you want to assign the learning task.
    4.  In the **Course item** field, select the course item to associate with the learning task.
    5.  In the **Due date** field, select the calendar icon and select the date and time when you want to trainee to complete the learning task.
    6.  Select **Save**.

## Add external learning content

Add courses from third-party applications such as Udemy, Pluralsight, Cornerstone, or ServiceNow University to enable your users to gain skills from external learning content.

### Before you begin

To add external learning content:

-   You must have the [Workforce Optimization for ITSM](../../configurable-workforce-optimization-itsm/task/activate-configurable-workforce-optimization-itsm.md) application installed.
-   You must integrate Coaching With Learning with third-party learning management systems. For information on how to perform this integration, see [Integrating Learning Core with third-party learning management systems](https://www.servicenow.com/docs/access?context=setup-learning-third-party-1&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US).

Role required: sn\_coaching.coach

### Procedure

1.  Navigate to **All** &gt; **Learning** &gt; **Content** &gt; **External Content**.

2.  Select a course.

3.  Click **Go to course**.

    You can review and learn the external course.


## Complete a learning task

Enhance your skills set by completing learning tasks from internal or external learning content.

### Before you begin

Role required: sn\_coaching.trainee

### Procedure

1.  Navigate to **All** &gt; **Learning** &gt; **Tasks** &gt; **Learning Tasks**.

2.  Select a learning task.

3.  Complete the learning task.

4.  Click **Mark as Complete**.


