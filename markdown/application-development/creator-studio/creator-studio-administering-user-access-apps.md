---
title: Administering user access for deployed Creator Studio apps
description: After users build apps in Creator Studio and you deploy them to production, as an admin, you are responsible for granting access to those apps to users.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/creator-studio/creator-studio-administering-user-access-apps.html
release: zurich
product: Creator Studio
classification: creator-studio
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Administer, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Administering user access for deployed Creator Studio apps

After users build apps in Creator Studio and you deploy them to production, as an admin, you are responsible for granting access to those apps to users.

## Assign user access in production

Applications must be deployed to the production instance, which is where you assign user access.

Users with the agent role are fulfillers, and should automatically get access to apps built in Creator Studio.

Assign users the agent role for the app's scope, for example, `x_snc_jd_it_fulf_0.agent` for an app with the scope `x_snc_jd_it_fulf_0`. For details on assigning roles to users, see .

## Restricting user access to forms

By default, all users on the production instance get access to forms built in Creator Studio, but Creator Studio developers can choose from existing access criteria if they want to restrict access. The **Available For** and **Not Available For** form settings are lists of User Criteria Records. For more information, see .

Developers can work with admins to define new access criteria for their app's forms to define the proper access from within Creator Studio. For more information, see [Edit the settings for a form in Creator Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/creator-studio/creator-studio-edit-form-settings.md).

## Personas for apps built in Creator Studio

-   **Requester**

    Someone requesting something, like a piece of equipment or permission to do something.

-   **Fulfiller**

    Someone who works on requests. Fulfillers may also approve or deny requests, depending on any approval automation for the app.


**Parent Topic:**[Administering Creator Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/creator-studio/administering-creator-studio.md)

