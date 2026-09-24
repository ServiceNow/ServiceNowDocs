---
title: \(Legacy\) Localization roles for Virtual Agent
description: Assign localization roles according to a user's scope in the localization process. Users may request translations, fulfill translation requests, and edit translations, based on their role.Requests translations for all the Virtual Agent components into one or more languages. Can also view localization insights. The Virtual Agent admin \[virtual\_agent\_admin\] role contains this role by default.Provides translations for the requested Virtual Agent topics. Depending on the flow, duties may include editing the translations in the Localization Framework task, interacting with third parties, and loading, verifying, and publishing translations.Edits the translations directly in Virtual Agent Designer. The NLU admin \[nlu\_admin\] and Virtual Agent admin \[virtual\_agent\_admin\] roles contain this role by default.Contains the localization requestor and localization editor roles by default.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/localization-roles-va.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Localizing NLU conversations, Localization options for NLU conversations, Build and deploy NLU conversations, \(Legacy\) Virtual Agent for NLU, Conversational Interfaces]
---

# \(Legacy\) Localization roles for Virtual Agent

Assign localization roles according to a user's scope in the localization process. Users may request translations, fulfill translation requests, and edit translations, based on their role.

The localization process follows this basic flow:

1.  Topics are developed and released in the source language \(for example, English\).
2.  Topics are translated, either by request or by editing them directly in Virtual Agent Designer.

    If you are using NLU models, the models must be translated as well. For more information about that process, see [Multilingual model management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/multilingual-model-managent.md).

3.  Translations are tested and published.

Virtual Agent role privileges vary with the user's function in this process. These roles are also defined in the Localization Framework. For more information, see [Localization Framework roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/roles-localization-framework.md).

To learn more about managing subscriptions, see [Managing per-user subscriptions in Subscription Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/managing-user-subscriptions-v2.md) and contact your account representative.

## Virtual Agent admin permissions

The Virtual Agent admin role contains the localization requestor and localization editor roles by default. Users can do the following:

-   Request translations
-   View existing translated content
-   Unlock and edit translated content \(unless translation is in process\)

The localization task is not available to this user.

\[Omitted image "loc-editor-role-view.png"\] Alt text: With the virtual\_agent\_admin role, you can request, view, and edit translations, but you do not have access to the localization task.

## Localization fulfiller permissions

The localization fulfiller role may not have Virtual Agent privileges. In that case, the user would only have access to assigned Localization Framework tasks.

If a Virtual Agent admin has the localization fulfiller role, the **Manage languages** page lets the user view the localization task that was created.

\[Omitted image "loc-fulfiller-role-view.png"\] Alt text: With both of the virtual\_agent\_admin and localization\_fulfiller roles, you can request, view, and edit translations and view the localization task details.

Click **View requested item** to open the localization fulfillment task in a new window.

\[Omitted image "loc-task-view-number.png"\] Alt text: A Localization request task is created when you submit a translation request.

**Parent Topic:**[\(Legacy\) Localizing Virtual Agent NLU conversations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/localize-va-topic.md)

## \(Legacy\) Localization requestor \[localization\_requestor\]

Requests translations for all the Virtual Agent components into one or more languages. Can also view localization insights. The Virtual Agent admin \[virtual\_agent\_admin\] role contains this role by default.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

None.

## \(Legacy\) Localization fulfiller \[localization\_fulfiller\]

Provides translations for the requested Virtual Agent topics. Depending on the flow, duties may include editing the translations in the Localization Framework task, interacting with third parties, and loading, verifying, and publishing translations.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

None.

## \(Legacy\) Localization editor \[localization\_editor\]

Edits the translations directly in Virtual Agent Designer. The NLU admin \[nlu\_admin\] and Virtual Agent admin \[virtual\_agent\_admin\] roles contain this role by default.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

None.

## \(Legacy\) Virtual Agent admin \[virtual\_agent\_admin\]

Contains the localization requestor and localization editor roles by default.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

**Note:** Avoid granting an admin role when more specialized roles are available.

