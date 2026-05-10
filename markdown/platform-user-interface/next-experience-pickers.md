---
title: Exploring Next Experience pickers
description: Next Experience scope pickers provide easy consistent scope selection across your instance.Add keyboard shortcuts for scope selector menus to be able to navigate scope selectors using your keyboard.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Exploring Next Experience pickers

Next Experience scope pickers provide easy consistent scope selection across your instance.

The scope selection menu icon \(![Scope selector icon.](../image/polaris-scope-selector-icon.png)\) displays in the Unified Navigation for users with roles that provide access to the application, domain, and update set scope pickers.

Any non-Global application scope displays a red circle on the scope selector menu icon \(![Scope selector icon.](../image/icon-scope-changed.png)\).

The instance tools icon \( ![Instance tools icon.](../image/icon-instance-tools.png)\) displays the application scope and current update set in a horizontal row beneath the other tool icons in the Unified Navigation. To enable this feature, you must create a system property called **glide.ui.next\_experience.instance\_tools\_disabled** and set it to **False**. When this feature is enabled, the scope selector icon is hidden.

-   **Application scope**: Enables application developers to view and select the application where their changes apply. For more information, see [Application scope](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/c_ApplicationScope.md).
-   **Domain scope**: Defines what users can access. Only users with access to domain separation see the domain scope picker. For more information, see [Domain scope](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/c_DomainScope.md).
-   **Update set**: Enables admin users to choose an update set for making and tracking customizations. For more information, see [Exploring System Update Sets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/system-update-sets/exploring-system-update-sets.md).

-   **Crypto module selector**: Enables users with more than one cryptographic module to select a module when entering data. This picker displays instead of the encryption context selector when the Key Management Framework is enabled through the **com.glide.kmf.global** system property and the system property **glide\_encryption.cle\_replatforming\_with\_kmf sys\_prop** is set to **opt\_in**. For more information, see [Create a cryptographic module](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/platform-encryption/create-cryptographic-module.md).


**Parent Topic:**[Configuring the Next Experience UI](next-experience-ui-admin.md)

## Keyboard shortcuts for the scope selector menu

Add keyboard shortcuts for scope selector menus to be able to navigate scope selectors using your keyboard.

Keyboard shortcuts for scope selector menus must be configured. They aren't available by default.

**Note:** Each of the pickers below includes two system properties that the admin must create. The **Value** field of the first one must be set to true. The **Value** field of the second one must be set to the keyboard combo for the picker.

<table id="table_l5g_k4h_mrb"><thead><tr><th>

Picker

</th><th>

Properties

</th><th>

Default key shortcut

</th></tr></thead><tbody><tr><td>

Application

</td><td>

-   glide.ui.keyboard.shortcuts.polaris.application\_picker.enabled
-   glide.ui.keyboard.shortcuts.polaris.application\_picker.key\_combo

</td><td>

ctrl+alt+a

</td></tr><tr><td>

Domain

</td><td>

-   glide.ui.keyboard.shortcuts.polaris.domain\_separation\_picker.enabled
-   glide.ui.keyboard.shortcuts.polaris.domain\_separation\_picker.key\_combo

</td><td>

ctrl+alt+d

</td></tr><tr><td>

Update set

</td><td>

-   glide.ui.keyboard.shortcuts.polaris.update\_set\_picker.enabled
-   glide.ui.keyboard.shortcuts.polaris.update\_set\_picker.key\_combo

</td><td>

ctrl+alt+u

</td></tr></tbody>
</table>