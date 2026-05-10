---
title: Generate modules using Now Assist
description: Use Now Assist to generate modules for your application by entering natural language prompts instead of manually configuring them.
locale: en-US
release: australia
product: Now Assist for Creator
classification: now-assist-for-creator
topic_type: task
last_updated: "2026-05-09"
reading_time_minutes: 3
breadcrumb: [Use, UI generation, Use generative AI, Now Assist for Creator, Vibe coding and AI app development on the ServiceNow AI Platform, Building applications]
---

# Generate modules using Now Assist

Use Now Assist to generate modules for your application by entering natural language prompts instead of manually configuring them.

## Before you begin

Make sure that you install UI generation and that you have the ui\_builder\_admin role. For more information, see [Install UI generation](install-ui-generation.md) and [Grant UI Builder admin role](grant-ui-builder-admin-role.md).

Role required: admin

## About this task

Use Now Assist to generate modules by providing prompts in natural language. The AI agent analyzes your prompt to identify the module type and key parameters, such as table names, views, roles, filters, and arguments. It then generates the requested modules.

## Procedure

1.  From the application navigator, select **All**, and then select **Create menu**.

    ![image.ui_gen_module_gen_create_menu]

    The module creation page opens.

2.  In the **Title** field, enter a name for the application menu.

3.  In the **Roles** field, enter a specific role to limit access to certain users.

4.  In the **Description** field, provide a description of the application menu to help clarify its purpose.

5.  Select **Create**.

    The Add modules to your application menu page opens.

6.  Select **Generate multiple modules at once using Now Assist**.

7.  In the **Tell Now Assist what you want** field, enter a prompt that describes the modules you want to create.

    For example:

    -   Create a list of active incidents assigned to me, and call it 'My Incidents'.
    -   Make a Workspace list page for all change requests scheduled this week.
    -   Create three record modules for the list, incident, and task tables.
    **Tip:** You can also select a module type from the available options.

8.  Select **Generate**.

    Now Assist generates the modules.

    An AI indicator appears next to the generated module, showing that it hasn’t been confirmed.

9.  Review the generated modules and do one of the following:

    -   To confirm the module and modify its fields, select **Accept and Edit**.
    -   To discard the generated module and try a different prompt, select **Reject**.
    After you select **Accept and Edit**, the AI indicator disappears.

10. After accepting the module, edit the configuration fields as needed.

    You can modify fields such as module type, table, role, and other properties specific to the module type.

11. Add or rearrange modules as needed to suit your specific needs.

12. Select **Done**.


## Result

The modules are added to your application menu and are ready for use.

Module generation issues

|Symptom|Cause|Resolution|
|-------|-----|----------|
|Module generation creates the wrong module type|The prompt did not clearly indicate the intended module type.|Specify the module type explicitly in the prompt \(for example, "Create a list module" or "Create a URL module"\). Alternatively, select a module type from the available options before entering the prompt.|

## Create five modules

1.  In the **Tell Now Assist what you want** field, enter the following prompt:

    ```
    Add:
    - a single record module called "Test Record",
    - an URL with arguments "url=https://example.com" and window name "External",
    - a list called "My Tasks", 
    - a script called "Data Cleanup Script" with arguments "var gr = new GlideRecord('task'); gr.query();" and window name "Cleanup"
    - a dashboard module
    ```

2.  Select **Generate**.

    The system creates five modules:

    |Module|Type|Description|
    |------|----|-----------|
    |Test Record|Record|A basic configuration without any additional parameters.|
    |URL|Direct|Contains parsed arguments: \`url=https://example.com\` and a window name: "External."|
    |My Tasks|List|A basic list configuration.|
    |Data Cleanup Script|Script|Includes parsed script arguments and a window name: "Cleanup."|
    |Dashboard|Dashboard|An empty dashboard module.|

3.  Select **Accept and edit**.
4.  \(Optional\) If needed, add, or rearrange modules.
5.  Select **Done** to finish.

**Parent Topic:**[Using UI generation](../concept/using-ui-generation.md)

