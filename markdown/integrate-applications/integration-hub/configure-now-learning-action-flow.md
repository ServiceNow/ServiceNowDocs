---
title: Configure the ServiceNow University action flow in Workflow Studio
description: Integrate the ServiceNow instance and ServiceNow University by using the Oauth credentials to authenticate ServiceNow requests.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [ServiceNow University Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Configure the ServiceNow University action flow in Workflow Studio

Integrate the ServiceNow instance and ServiceNow University by using the Oauth credentials to authenticate ServiceNow requests.

## Before you begin

-   Have ITSM Enterprise license subscription.
-   Integrate Coaching with Learning with ServiceNow University. For more information, see [External Content Integration Sources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/workforce-optimization-for-it-service-management/integration-source-coaching-with-learning-coaching-wfo-itsm.md).
-   Role required: admin.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Select the **Actions** tab.

3.  Get the course details from ServiceNow ServiceNow University.

    1.  Select **Look up Courses Stream**.

    2.  In the **Inputs** action outline, select **Test** and specify the input value for the following fields:

        |Field|Description|
        |-----|-----------|
        |Type|Type of course; for example, a path.|
        |Updated|Fetches courses updates from the specified date.|
        |Created|Fetches courses created from the specified date.|
        |Order|The order in which the course must be displayed.|
        |Page Size|The number of courses per page.|
        |Offset|Fetches the item from the specified offset. For example, if the offset is 10, the application fetches it from the 10th item.|

    3.  Select **Run Test**.

    The **Outputs** action outline displays the following course details:

    |Field|Description|
    |-----|-----------|
    |Number|Course identification number.|
    |Name|Name of the content.|
    |Short description|Short description for the content.|
    |Description|Content description.|
    |Type|Course type; for example, whether the course is a path or collection.|
    |State|The status of each course; for example, whether it is in draft or published state.|
    |Portal link|URL to access the course.|

4.  Configure the course activity for all users for a specific time period.

    **Note:** The default time period for course activities is 30 days.

    1.  Select **Look up User Course Activity Stream**.

    2.  In the **Inputs** tab, specify the data type for the following fields:

        |Field|Description|
        |-----|-----------|
        |States|The status of each course; for example, whether it is in draft or published state.|
        |User Emails|Email of the users associated with the course activity.|
        |Enrolled|Date the user enrolled in the course.|
        |Completed|Fetches courses that were completed after the specified date.|
        |Updated|Fetches courses updates from the specified date.|
        |Order|The order in which the course must be displayed.|
        |Page Size|The number of pages to fetch.|
        |Offset|Fetches the item from the specified offset. For example, if the offset is 10, the application fetches it from the 10th item.|

    3.  Select **Run Test**.

    In the **Outputs** tab, specify the output value for the following fields:

    |Field|Description|
    |-----|-----------|
    |User Email|User emails associated with the course activity.|
    |Content Name|Name of the content.|
    |Content Number|The content identification number.|
    |Percent Complete|Course percentage completion.|
    |State|Course status.|
    |Completion Date|The date when the course was completed.|
    |Enrollment Date|The date when the user enrolled in the course.|


**Related topics**  


[Building actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/actions.md)

