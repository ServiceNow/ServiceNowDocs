---
title: Provide entry points for mapping an application service
description: As an application service owner you may receive a request for information about entry points in an email notification. Provide information about entry points to enable administrators to start discovery of an application service.
locale: en-US
release: yokohama
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Map a single application service using classic Service Mapping, Application service mapping using classic Service Mapping, Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Provide entry points for mapping an application service

As an application service owner you may receive a request for information about entry points in an email notification. Provide information about entry points to enable administrators to start discovery of an application service.

## Before you begin

Role required: sm\_app\_owner or service\_mapping\_admin

## About this task

If information about service instance entry points is missing, an administrator cannot start mapping the service instance. In this case, the administrator sends a request for missing data from the service instance form, which creates a service process task assigned to you. You receive an email notification with the link to the Questionnaire page where you must enter the missing data. The most important information is about the entry points, however, any additional data about application service components, their connections, or usage is of help for the administrator. When you finish entering data in the Questionnaire and submit it, the system closes the service process task.

![Flow of creating a single application service.](../image/SingleBSFlow.png "Mapping an application service flow")

## Procedure

1.  Click the link in the notification email to access the **Questionnaire** page.

2.  Alternatively, open to the **Questionnaire** page from the list of tasks assigned to you.

    1.  Navigate to **Service Mapping** &gt; **Administration** &gt; **My Tasks**.

    2.  Sort the list of service process tasks as required.

    3.  Click the required task.

    4.  Click the service instance form link.

    5.  Click **Questionnaire** in the left pane.

3.  On the **Planned Custom Entry Points** tab, enter information about service instance entry points.

    **Note:**

    If you cannot specify the exact attributes of the entry points, such as the URL or the IP address, add general information which can guide the administrator. For example, the type of the application, like Tomcat server.

4.  To add information about any other components comprising this service instance, click the **Components** tab, and enter the relevant data there.

5.  When you finished entering the information, click **Actions**, and then select **Submit Questionnaire**.

    The data request task assigned to you closes. The service instance state changes to In Progress.

6.  If there is any other useful information concerning this service instance, enter it in the **Notes** field under **Worknotes** and press Enter to post your comment.


**Parent Topic:**[Map a single application service using classic Service Mapping](t_DefineNewBusinessService.md)

