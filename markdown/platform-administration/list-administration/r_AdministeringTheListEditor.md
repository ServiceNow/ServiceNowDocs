---
title: List editor administration
description: The list editor allows users to edit field values directly from a list without navigating to a form.
locale: en-US
release: xanadu
product: List Administration
classification: list-administration
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [List administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# List editor administration

The list editor allows users to edit field values directly from a list without navigating to a form.

Administrators can manage this feature by using the following options. Some of the options are not supported in List v3.

-   Configure global properties
-   Configure list control settings for a table
-   Configure contextual security rules
-   Manage user preferences \(List v2 only\)

**Warning:** In List v2, the list editor does not enforce client scripts or UI policies. In List v3, the list editor enforces UI policies and mandatory dictionary attributes, but not client scripts. Allowing list editing with client scripts running on fields in a form can result in incorrect data being saved to the record. For systems in which client scripts or UI policies apply to forms, consider disabling list editing or creating appropriate business rules or access control to control the setting of values in the list editor. See [Use business rules and client scripts to control field values](https://www.servicenow.com/docs/access?context=c_BusinessRules&version=xanadu&pubname=xanadu-application-development&section=r_BsnsRlClntScptsCntrlFldVl&ft:locale=en-US) for information on managing form and list editing.

**Warning:** You cannot edit state fields that are extended from the Task \[task\] table from a list of task records. Examples include:

-   problem\_state
-   incident\_state
-   phase\_state
-   request\_state

While these fields are visible from the task list, they must be edited from the extended table.

-   **[Configure list editor properties](../task/t_ConfigureListEditorProperties.md)**  
Configure list editor properties that control whether lists can be edited and, in List v2, which field types cannot be edited.
-   **[Configure list control settings for the list editor](../task/t_ConfigListEditorControlSettings.md)**  
You can configure the list control settings that affect the list editor.
-   **[Configuring contextual security for the list editor](r_ConfigListEditorContextSecurity.md)**  
The list editor enforces existing access control rules \(ACLs\) and additional security controls to restrict editing from a list.
-   **[User preferences for list editing](r_ManagingUserPreferences.md)**  
Users can set user preferences for list editing by personalizing a list \(available when the list mechanic is activated\).

**Parent Topic:**[List administration](../../core-configuration/concept/p_ListAdministration.md)

**Related topics**  


[Use the list editor](https://www.servicenow.com/docs/access?context=t_UseTheListEditor&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)

