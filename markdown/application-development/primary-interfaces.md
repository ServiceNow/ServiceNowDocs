---
title: Primary interfaces
description: The primary way for users to interact with a data model is through forms and lists or through mobile.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Create design elements, Build your application, Exploring professional development, Building pro-code applications, Developing your application, Building applications]
---

# Primary interfaces

The primary way for users to interact with a data model is through forms and lists or through mobile.

## Forms and lists

The standard method of accessing data in ServiceNow is through the default forms and lists. A form displays information from one record in a data table and a list displays a set of records from a table. When configuring forms and lists:

1.  Keep the number of fields on a form to a minimum. The more fields on a form, the longer the form takes to load resulting in a poor user experience. Use form views to create different sets of fields for different situations.
2.  Use form sections to logically group fields together and to keep users from scrolling. The top section of the form should contain the fields that are always needed or used, while the other form sections contain less frequently utilized fields.
3.  Make sure fields appear in the right order. For example, the start date field should always come right before an end date field.
4.  Use seven or fewer columns in a default list. Users can add more by [personalizing their lists](https://servicenow.com/docs/bundle/paris-platform-user-interface/page/use/using-lists/task/t_PersonalizeAList.html).
5.  Avoid using a reference field as the first item in the list view, because it is shown as hyperlinked text. Clicking on the reference field will redirect the user to the referenced record instead of the list record, resulting in a poor user experience.

This example shows a poorly designed form.

-   The form has no sections. Users need to scroll through the entire form to see all the fields.
-   Similar fields are not grouped together. For example, Assignment group and Assigned to are on different sides of the form.

    ![Poorly designed form](../image/bad-form.png)


This example shows a well-designed form.

-   Fields are grouped together logically.
-   The form has been broken into sections for easier viewing and data entry.

    ![Well-designed form](../image/good-form.png)


## Mobile

If users will interact with the application on their mobile devices and will need native iOS or Android functionality, such as geolocation or offline access to application data, use the ServiceNow Agent app. Use Studio to create a mobile application for the application.

Create applets in the mobile application. Applets are tiles within an application. Include a main screen, such as a map or a list, and various details screens, such as an activity stream or related lists. Applets should have focused experiences.

**Note:** Individual applets can be secured by role as well as made available in offline mode.

Self-paced training: [Mobile Applications](https://developer.servicenow.com/dev.do#!/learn/courses/paris/app_store_learnv2_mobileapps_paris_mobile_applications)

Other resources: [Mobile Resources](https://community.servicenow.com/community?id=community_blog&sys_id=98855a4edba9fbc0fece0b55ca9619e0)

**Parent Topic:**[Create design elements](create-design-elements.md)

