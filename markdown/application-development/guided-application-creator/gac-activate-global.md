---
title: Allow global application development in Guided Application Creator
description: By default, developers can't create applications in the global scope in Guided Application Creator. You can limit global application development to certain developers by assigning them an additional role.
locale: en-US
release: yokohama
product: Guided Application Creator
classification: guided-application-creator
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Guided Application Creator, Building pro-code applications, Developing your application, Building applications]
---

# Allow global application development in Guided Application Creator

By default, developers can't create applications in the global scope in Guided Application Creator. You can limit global application development to certain developers by assigning them an additional role.

## Before you begin

**Important:** Applications that you create in the global scope bypass scope protections and may cause licensing issues. For information on what to expect when you create an application in the global scope, see [Application scope](../../applications/concept/c_ApplicationScope.md).

Role required: admin

## About this task

You designate someone to use Guided Application Creator by assigning them the sn\_g\_app\_creator.app\_creator role. You can allow this user to create applications in the global scope by also assigning the sn\_g\_app\_creator.global role.

Alternatively, to allow all users with the sn\_g\_app\_creator.app\_creator role to create applications in the global scope, add the **sn\_g\_app\_creator.allow\_global** system property and set it to **true**. For more information on adding a property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Note:** Users with the admin role can create applications in the global scope, regardless of whether or not they have the sn\_g\_app\_creator.global role.

## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Users** and open the user record of the developer.

2.  On the Roles related list, select **Edit...**.

3.  On the Edit Members page, move the sn\_g\_app\_creator.global role from **Collection** to **Roles List**.

    ![The appropriate roles are selected](../image/gac-global-role.png)

    Ensure that the sn\_g\_app\_creator.app\_creator role is also selected. The developer needs both the sn\_g\_app\_creator.app\_creator and sn\_g\_app\_creator.global roles to create applications in the global scope in Guided Application Creator.

4.  Select **Save**.

5.  On the user record, select **Update**.


## Result

The option to create an application in the global scope is available to developers with the sn\_g\_app\_creator.global role. Developers can use, for example, ServiceNow Studio, to create an app.

**Parent Topic:**[Guided Application Creator](../concept/guided-app-creator.md)

