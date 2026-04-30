---
title: Learn about audiences
description: Learn how to apply the correct audiences to your UI Builder pages.
locale: en-US
release: xanadu
product: UI Builder
classification: ui-builder
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Learning UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Learn about audiences

Learn how to apply the correct audiences to your UI Builder pages.

## Audiences

Understanding your audiences in UI Builder is an important part of creating pages. The audience defines who can see your pages. You create pages for targeted experiences tailored to audiences and roles such as agents and managers. For example, you may want to create a page for agents to solve issues for your employees. You want to ensure that only people who have the agent role can see the page.

Audiences are generally made of allow/deny lists based on role and domain. They can also target the following:

-   Role
-   Group
-   User
-   Company
-   Department
-   Location
-   Script

You can set audiences to fit a specific role based on one or more criteria. For example, you could create an audience for an ITSM user in Europe who is not a manager.

The **glide.ux.user\_criteria\_enabled** property needs to be set to **true** to configure access for users based on role, department, group, location, or company. See [Enable the user criteria property](../task/enable-user-criteria-property.md), for more information.

Set an audience in UI Builder when you create your page or page variant. You can also set the priority of the audience record. The lower the number the higher the priority. Ensure the **Active** check box is selected to make this page active.

![Edit audiences modal with options to set the audience or audiences and order.](../image/add-audience-form.png "Add audiences modal")

If you do not see an audience that you need, you can click **Open audiences in platform** to define an audience in the ServiceNow AI Platform®.

-   Choosing an audience from the list in the **Audience** field.

    ![UI Builder variant audience drop down list.](../image/UIB-varant-audience-drop-down.png "Audience list")

-   Selecting **Open audiences in platform** to edit or create an audience record in the ServiceNow AI Platform®.
-   If you have multiple audiences, define the **Order** for each audience record. The order defines the importance of each audience record. For example, a CSM Manager could have a higher priority than a CSM Consumer Agent. To give higher priority to an audience, enter a lower number.
-   Ensuring the **Active** check box is selected to make this page active.

**Parent Topic:**[Learning UI Builder](learning-uib.md)

