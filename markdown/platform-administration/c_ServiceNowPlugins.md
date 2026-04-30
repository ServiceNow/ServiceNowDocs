---
title: ServiceNow plugins
description: Plugins are software components that provide features and functionalities within a ServiceNow instance.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Basic system configuration, Get started, Administer]
---

# ServiceNow plugins

Plugins are software components that provide features and functionalities within a ServiceNow instance.

Plugins and applications video, approximately two minutes long.

## Differences between plugins and applications

Plugins and applications are separate components on the ServiceNow AI Platform.

-   A plugin adds features to installed applications and extends functionality on the ServiceNow AI Platform. For additional details about plugins, see [KB0716626](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0716626).
-   An application is a standalone piece of code that implements a collection of features on the ServiceNow AI Platform. You can install applications from the ServiceNow Store or create your own applications.

## Activating plugins

All plugins are provided by ServiceNow, but some plugins are activated differently.

-   A set of plugins are activated on your instance by default. You can activate additional plugins on your instance depending on your business needs. For details, see [Activate a plugin](../task/t_ActivateAPlugin.md).
-   Other plugins require activation by ServiceNow personnel. To request activation, follow the steps in [Request a plugin](../task/t_RequestAPlugin.md).

There are some plugins that you can't activate or upgrade on your instance and the button is greyed out. This situation can happen in the following cases:

-   The plugin requires a subscription that you haven't purchased. To purchase a subscription, contact your ServiceNow account manager.
    -   Some features are not included in the ServiceNow AI Platform and require a separate subscription. To purchase a subscription or to find plugin costs, contact the [account manager](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0547253) in your company.
    -   When you purchase a subscription, certain plugins are activated automatically. If a paid plugin isn't activated automatically, you can manually activate it from the All Applications list in your instance. If the plugin doesn't appear in the instance, submit a request via the Now Support Service Catalog.
    -   You can't activate a plugin in your production instance. However, you can test a plugin by activating it in a non-production instance. This includes plugins that are associated with a for-fee subscription. When you’re ready to activate the plugin in your production instance, request the plugin from Now Support.
-   The plugin depends on other plugins being activated.
    -   When you activate a plugin with dependent plugins, the system notifies you of the dependencies before it completes the activation. If you opt to continue with activation, the system automatically activates all the plugins required.
    -   In some cases, the plugin works, but certain features that don't apply to your system aren't installed. When you ask to activate a plugin in this category, the system notifies you of the dependencies before it completes the activation. If you opt to continue, the system activates the requested plugin but doesn't include the features that depend on other plugins.
-   The plugin is already activated on your instance.
    -   To determine if a plugin is already activated, see [Plugin Activation Status \[KB0678767\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0678767).
    -   After a plugin is activated, you can't disable or deactivate it. If needed, you can hide the functionality. You should thoroughly test, in a non-production instance, the features that are installed when you activate the plugin before using them in a production instance.

After a plugin is activated, you cannot disable or deactivate it. You should thoroughly test, in a non-production instance, the specific features and functionalities that are installed when you activate the plugin before using them in a production instance. See [Uninstall a ServiceNow plugin \[KB0716414\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0716414).

-   If necessary, you can hide or disable the functionality by restricting access through the use of roles and ACLs.
-   Some plugins support rollback contexts. For details on using rollback contexts, see [Roll back and delete recovery](../../table-administration/concept/rollback-delete-recovery.md).

A warning message appears if the alter table or create table operation fails when you activate or upgrade a plugin. Contact Customer Service and Support for help with processing any skipped tables.

## Personal developer instances

You can test a plugin on your personal developer instance \(PDI\) before launching it in a production instance. If a plugin isn't active by default on a PDI, you can activate the plugin without requesting or purchasing it.

To activate a plugin on a PDI, use the All Applications page on your instance. If the plugin isn't available on the All Applications page, activate it from the [ServiceNow® Developer Site](https://developer.servicenow.com/). For more information, see [Activate a plugin on a personal developer instance](../task/activate-plugin-pdi.md).

**Note:** Some plugins aren't available for activation on PDIs.

-   **[Activate a plugin](../task/t_ActivateAPlugin.md)**  
You can activate most plugins to expand features and functionalities in the ServiceNow AI Platform.
-   **[Request a plugin](../task/t_RequestAPlugin.md)**  
If a plugin does not appear in the Application Manager, you cannot activate it yourself. Request activation of the plugin by ServiceNow personnel.
-   **[List of plugins \(Zurich\)](../reference/list-of-plugins.md#)**  
List of all plugins that you can activate if you have the admin role.

**Parent Topic:**[Basic system configuration](../../core-configuration/concept/p_CoreConfigurationOverview.md)

**Related topics**  


[List of plugins \(Zurich\)](../reference/list-of-plugins.md#)

