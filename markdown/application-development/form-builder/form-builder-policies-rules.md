---
title: Policies and rules in Table Builder
description: Policies and rules define how information appears to users based on role and entries, as well as who can access tables and forms built in Table Builder.Configure UI policies in Table Builder to adjust how forms appear based on roles and user input.Edit UI policies to change how forms appear based on roles and user input in Table Builder.
locale: en-US
release: australia
product: Form Builder
classification: form-builder
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Using Table Builder, Table Builder, Builder library, Developing your application, Building applications]
---

# Policies and rules in Table Builder

Policies and rules define how information appears to users based on role and entries, as well as who can access tables and forms built in Table Builder.

## Sections for working with policies and rules

The **Policies and rules** tab in Table Builder has several sections, but you can edit only UI policies within Table Builder. The other sections are read-only and contain links to manage their content in other parts of the ServiceNow AI Platform.

|Section|Description|Editable within Table Builder|
|-------|-----------|-----------------------------|
|UI Policies|Dynamically change the behavior of information on a form and control custom process flows for tasks.|Yes.|
|Access control rules|Control access to the specified resource based on role, condition, and script criteria being met.|No.|
|Client Scripts|Create scripts that control how form fields appear based on defined criteria.|No.|
|Business Rules|Create business rules to accomplish tasks like automatically changing values in form fields when certain conditions are met.|No.|
|Workspace view rules|Define rules to control how users view workspaces based on criteria.|No.|

To manage a rule or policy script outside of Table Builder, select ![View external link icon.](../image/view-external-link-icon.png) for the entry. Or, you can view the full list of rules and scripts outside of Table Builder by selecting the **Full list** ![View external link icon.](../image/view-external-link-icon.png) link for each section of the **Policies and rules** tab:

-   **Full ACL list**
-   **Full client scripts list**
-   **Full business rule list**
-   **Full workspace view rules list**

## UI policies for tables and forms

Configure UI policies to adjust how forms appear based on roles and user input.

For example, you can use UI policies to make a field on a form read-only or required or hide certain fields depending on a user's role. Basic UI policies do not require any scripting. For more advanced actions, use the **Run scripts** option.

You can also use client scripts to perform all these actions, but for faster load times use UI policies when possible.

**Parent Topic:**[Using Table Builder](using-fb.md)

## Create a UI policy in Table Builder

Configure UI policies in Table Builder to adjust how forms appear based on roles and user input.

### Before you begin

-   Launch Table Builder. For more information, see [Accessing Table Builder](accessing-form-builder.md).
-   \(Optional\) Choose a domain to work within \(if not global\). For more information, see [Domain separation and Table Builder](form-builder-domain-separation.md).
-   \(Optional\) Choose an application scope to work within \(if not global\). For more information, see [Using an application scope with Table Builder](fb-application-scope.md).

Role required: personalize\_rules or AES user role and delegated developer permissions. For more information, see [Delegate developers using AES](../../../build/app-engine-studio/concept/aes-app-dev-workflow.md).

### About this task

You can create and edit UI policies only for applications that you own. For more information on application scope, see [Domain separation and Table Builder](form-builder-domain-separation.md).

### Procedure

1.  On the Table Builder screen, choose a table to work with.

2.  Select the **Policies and rules** tab.

    Alternatively, you can add a UI policy for a field directly in the **Forms** tab of Table Builder in the right pane that appears when you select a field.

3.  Select the UI Policies section to display a list of UI policies.

4.  Select the **Add new policy** link to display the policy details.

    -   If the link is inactive, you must change the scope that you're working with on the **Forms** tab.
    -   If a field has policy and appears in the view, the active icon appears on the top corner of the field as shown in the following example.
    ![Add new policy link in UI policies section.](../image/fb-ui-policy-add.png)

5.  On the form, fill in the fields for the Policy details section.

    For more information on field definitions, see [Policies and rules properties in Table Builder](../reference/ui-policy-fields.md).

6.  In the When these conditions are met section, specify the conditions that, if fulfilled, cause the UI policy to be applied using the condition builder.

    To add multiple sets of conditions, select **New condition set**.

7.  In the Do the following section, create field actions that should be performed when the conditions are met.

8.  To finish adding the policy, select **Add UI policy**.


### Result

After you add the UI policy, you can configure scripts and the related list actions for it. For more information on client scripts and UI policies, see [Client scripts for UI policies](https://www.servicenow.com/docs/access?context=t_CreateAUIPolicy&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

## Modify a UI policy in Table Builder

Edit UI policies to change how forms appear based on roles and user input in Table Builder.

### Before you begin

-   Launch Table Builder. For more information, see [Accessing Table Builder](accessing-form-builder.md).
-   \(Optional\) Choose a domain to work within \(if not global\). For more information, see [Domain separation and Table Builder](form-builder-domain-separation.md).
-   \(Optional\) Choose an application scope to work within \(if not global\). For more information, see [Using an application scope with Table Builder](fb-application-scope.md).

Role required: personalize\_rules or AES user role and delegated developer permissions. For more information, see [Delegate developers using AES](../../../build/app-engine-studio/concept/aes-app-dev-workflow.md).

### About this task

You can create and edit UI policies only for applications that you own. For more information on application scope, see [Domain separation and Table Builder](form-builder-domain-separation.md).

### Procedure

1.  In the UI policies section, on the **Policies and rules** tab, select the policy that you want to edit.

    You can also edit a field's UI policy directly in the form by selecting it in the **UI policies** tab of the right pane that appears when you select a field.

2.  Change the UI policy fields and attributes as needed.

    For more information on field definitions, see [Policies and rules properties in Table Builder](../reference/ui-policy-fields.md).

3.  Click **Update UI policy**.


