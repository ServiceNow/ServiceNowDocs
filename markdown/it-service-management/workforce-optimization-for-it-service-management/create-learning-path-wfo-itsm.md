---
title: Create a learning path in Workforce Optimization for ITSM
description: Create a learning path, add relevant skills and course items, and publish the path. When your agents complete the path, any skills associated with the path are automatically added to the agent's profile.
locale: en-US
release: australia
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Learning, Training your teams, Coaching, Workforce Optimization for ITSM, IT Service Management]
---

# Create a learning path in Workforce Optimization for ITSM

Create a learning path, add relevant skills and course items, and publish the path. When your agents complete the path, any skills associated with the path are automatically added to the agent's profile.

## Before you begin

Role required: sn\_wfo\_cfg\_ws.manager​

This video walks you through the steps for creating a learning path.Create a learning path

## Procedure

1.  Navigate to **Workspaces** &gt; **Manager Workspace**.

2.  Select the Coaching icon \(![Coaching icon](../image/coaching-icon-uib.png)\).

3.  Select the **Learning** tab.

4.  Navigate to **Learning Paths** &gt; **All learning paths**.

    -   You can search a path based on keywords using the **Search** field or narrow down the display of the paths based on skills using the **Filter by skill** field.
    -   You can select a learning path to view the details. You can analyze the path objective, the skills associated with the course items, the total number courses in the path, and the duration to complete them.
    -   You can select the link that displays the skills and view all skills associated with the learning path. The list of skills will display if there are more than 5 skills associated with the learning path.
5.  Select **Create new path**.

    The **New learning path** screen displays.

6.  Create a learning path.

    1.  In the **Path name** field, enter a unique name for the learning path.
    2.  In the **Course Catalog** field, select the catalog to which you want to associate the learning path.

        **Important:** You can customize the publish flow for any catalog other than the **Default Catalog**. For information on publish flow, see [Create a course catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/learning-core/create-course-catalog.md) and the [Course catalog form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/learning-core/course-catalog-table.md).

    3.  Select **Next**.
    The learning path that is created is in **Draft** state. You can choose to complete it later.

7.  Add or remove course items.

    -   You can search courses based on keywords using the **Search** field or narrow down the display of the courses based on skills using the **Filter by skill** field.
    -   You can select a course and preview the details.
    **Note:** You can add a quiz as a course item.

    1.  Enable or disable the check box for the course items that you want to add or remove from the learning path.

    2.  Select **Add items**.

    The **Review** screen appears. A learning path consists of a list of courses that a trainee takes in a given order. You can drag the courses in the list to set the order in which the trainee has to complete the path. In the **Items in the learning path** list, the added course items display in the order you have selected them. You can drag and reorder these items.

8.  Review the learning path.

    The skills associated with the selected courses are automatically populated in the **Course skills** field.

    1.  Review and edit any required details.

        You can also add additional skills to the learning path.

    2.  To remove items that you no longer want to associate with the learning path, select the item and then select **Remove selected items**.

    3.  Select **Next**.

        The **Publish** screen appears.

        -   The screen displays the agent view of the learning path.
        -   The **Curriculum** section displays the course items in the order that you have selected in the **Review** screen.
        -   If you do not want to publish the learning path, you can select **Save** and come back to it later.
9.  Select **Submit** to publish the learning path.

    The learning path is published based on the Publish flow.


**Parent Topic:**[Learning in Workforce Optimization for ITSM](../concept/workforce-learning-configurable-wfo-itsm.md)

