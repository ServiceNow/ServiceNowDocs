---
title: Create an application record in Guided Application Creator
description: Create an application record in Guided Application Creator to identify a custom application.
locale: en-US
release: xanadu
product: Guided Application Creator
classification: guided-application-creator
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Setting up an application in Guided Application Creator, Guided Application Creator, Building pro-code applications, Developing your application, Building applications]
---

# Create an application record in Guided Application Creator

Create an application record in Guided Application Creator to identify a custom application.

## Before you begin

By default, developers can't create applications in the global scope in Guided Application Creator. You can limit global application development to certain developers by assigning them an additional role. For more information, see [Allow global application development in Guided Application Creator](gac-activate-global.md).

Role required: sn\_g\_app\_creator.app\_creator or admin

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **Studio**, and then select **Create Application**.

    If you are launching Guided Application Creator for the first time, select **Let's get started** on the welcome screen.

2.  On the screen, fill in the fields.

<table id="table_rqq_nz1_5hb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of your application.

</td></tr><tr><td>

Description

</td><td>

Description of your application.

</td></tr><tr><td>

Scope

</td><td>

Scope of your application. The application scope is set automatically when you name your application.

 If available, you can also select to create your application in the global scope.

 For more information on application scopes, see [Application scope](../../applications/concept/c_ApplicationScope.md).

</td></tr></tbody>
</table>3.  Give your application a logo image.

    You can drag and drop an image on the logo field, or you can select **Drag and drop or browse to upload logo**.

    ![Logo field](../image/logo-field.png)

4.  Select **Create** to assign roles for your application.

    To continue building your application in Guided Application Creator, follow the steps in [Define roles in Guided Application Creator](gac-create-roles.md).

    You can optionally exit Guided Application Creator on the **Let's create some roles for this app** screen to save the application and add more functions to it later. To exit, select **X** to close the screen and then select **Yes, close**.

    **Tip:** Complete the entire process of setting up an application in Guided Application Creator. If you exit, you have to continue setting up your application in Studio and across various forms. You can't pick up where you left off in Guided Application Creator.


## Result

Your application record is saved in the Custom Application \[sys\_app\] table. You are added as a delegated developer for the application. To view your application later, navigate to **System Applications** &gt; **My Company Applications**.

**Parent Topic:**[Setting up an application in Guided Application Creator](set-up-app.md)

