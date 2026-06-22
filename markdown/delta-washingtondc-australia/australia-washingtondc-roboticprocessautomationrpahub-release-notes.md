---
title: Combined Robotic Process Automation \(RPA\) Hub release notes for upgrades from Washington DC to Australia
description: Consolidated page of all release notes for Robotic Process Automation \(RPA\) Hub from Washington DC to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-washingtondc-australia/australia-washingtondc-roboticprocessautomationrpahub-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 14
breadcrumb: [Products combined by family]
---

# Combined Robotic Process Automation \(RPA\) Hub release notes for upgrades from Washington DC to Australia

Consolidated page of all release notes for Robotic Process Automation \(RPA\) Hub from Washington DC to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Robotic Process Automation \(RPA\) Hub release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Washington DC to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Robotic Process Automation \(RPA\) Hub to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

Ensure that you upgrade any of the following currently installed Microsoft Software Installers \(MSIs\) by downloading the RPA applications:

-   RPA Desktop Design Studio
-   Attended Robot
-   Unattended Robot
-   Unattended Robot Login Agent

For more information, see [Download the RPA applications from RPA Hub](https://www.servicenow.com/docs/access?context=download-installer-rpa&family=washingtondc&ft:locale=en-US).

 The following upgrade steps are applicable only when you’re upgrading from San Diego or Tokyo to Washington DC.

 Based on the number of records in the application file table, you could experience a potential delay while upgrading the RPA Hub applications from Tokyo or before to Washington DC.

 Before upgrading RPA Hub to Washington DC, you must set the value of the **glide.rollback.blacklist.TableParentChange.change** system property to **false**. If this property doesn't exist in the System Property \[sys\_properties\] table, add the property and set its value to false. For more information on how to add a property, see [Add a system property](https://www.servicenow.com/docs/access?context=t_AddAPropertyUsingSysPropsList&family=washingtondc&ft:locale=en-US).

 After you upgrade to the Washington DC, the bot process definitions change to the new structure, which is the bot process configuration.

 Although the bot process configuration doesn't replace the bot process completely, most fields are moved from bot process to bot process configuration. If you upgrade to the Utah version without updating the system property value, the tables don’t extend the Application File table. To update the table changes manually, see the [Restructuring RPA Hub tables to sys\_metadata in Utah](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1223629) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Robotic Process Automation \(RPA\) Hub.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **[Embedded Task Automation in RPA Hub](https://www.servicenow.com/docs/access?context=embedded-task-auto-rpa&family=washingtondc&ft:locale=en-US)**

Trigger attended bot processes, also known as attended automations, from the ServiceNow forms, playbooks, workspaces, and so on.

To trigger this bot process from the ServiceNow form, select the **Enable Embedded Task Automation** check box in the Attended Bot Process form. After enabling this check box, two additional tabs, Process Field Parameters and Attended Configuration, are available on the Bot Process form. For more information about the Bot Process form, see [Bot Process form](https://www.servicenow.com/docs/access?context=bot-process-form&family=washingtondc&ft:locale=en-US).

On the Process Field Parameters tab, create dynamic parameters that are used in the bot process. Process field parameters are used for setting a value or getting the value of a field on a particular form. For more information about creating process field parameters, see [Create a process field parameter in RPA Hub](https://www.servicenow.com/docs/access?context=create-process-field-param-rpa&family=washingtondc&ft:locale=en-US). You can also create a parameter from the Field Parameter Mappings tab by selecting the **Create parameter** button from the Attended Configurations menu. For more information, see [Map a table field to a bot process field parameter in RPA Hub](https://www.servicenow.com/docs/access?context=create-field-param-mapping-rpa&family=washingtondc&ft:locale=en-US).

In the RPA Hub workspace, create an attended configuration record. For more information about creating an attended configuration record, see [Create an attended configuration record in RPA Hub](https://www.servicenow.com/docs/access?context=create-attended-config-rpa&family=washingtondc&ft:locale=en-US).

On the Field Parameter Mappings tab, map the form fields to the process field parameters that are used in the automations. This process enables an easy data flow during the execution of a bot process. For more information about mapping field parameters, see [Map a table field to a bot process field parameter in RPA Hub](https://www.servicenow.com/docs/access?context=create-field-param-mapping-rpa&family=washingtondc&ft:locale=en-US).

Activate the attended configuration record to trigger the attended bot process. For more information, see [Activate an attended configuration record in RPA Hub](https://www.servicenow.com/docs/access?context=activate-attend-config-rpa&family=washingtondc&ft:locale=en-US).

-   **[New components for Embedded Task Automation](https://www.servicenow.com/docs/access?context=forms_sn_rpa_studio&family=washingtondc&ft:locale=en-US)**

The following four new components are added to the new **Forms** section in RPA Desktop Design Studio. These components are available under the new ServiceNow category in the Toolbox pane.

    -   **AttendedConfigurations** component: Segregate the execution of the automations in a single automation project and call the respective logic according to the action invoked. For more information, see [Use the AttendedConfigurations component](https://www.servicenow.com/docs/access?context=use-attended-configurations-forms&family=washingtondc&ft:locale=en-US).
    -   **GetProcessFieldParameters** component: Fetch the values of the ServiceNow form fields associated in the Field Parameter Mapping of the corresponding attended configuration record in RPA Hub. For more information, see [Use the GetProcessFieldParameters component](https://www.servicenow.com/docs/access?context=use-get-process-field-param-forms&family=washingtondc&ft:locale=en-US).
    -   **GetRecordContextID** component: Fetch the current record sys\_id of the ServiceNow form, from where the automation is triggered. For more information, see [Use the GetRecordContextID component](https://www.servicenow.com/docs/access?context=use-get-record-context-id-forms&family=washingtondc&ft:locale=en-US).
    -   **SetProcessFieldParameters** component: Update the values of the ServiceNow form fields associated in the Field Parameter Mapping of the corresponding attended configuration record in RPA Hub. For more information, see [Use the SetProcessFieldParameters component](https://www.servicenow.com/docs/access?context=use-set-process-field-param-forms&family=washingtondc&ft:locale=en-US).
-   **[External credential vault in RPA Hub](https://www.servicenow.com/docs/access?context=external-credentials-rpa&family=washingtondc&ft:locale=en-US)**

In RPA Hub, you can retrieve robot credentials, application credentials, or Time-based One-time Password \(TOTP\) seeds from the external credential vault.

Create an external credential vault record in RPA Hub to register your external credential vault for further usage by the robot. For more information, see [Create an external credential vault record in RPA Hub](https://www.servicenow.com/docs/access?context=create-ext-cred-rpa&family=washingtondc&ft:locale=en-US).

A new **External Credential** check box is available in the credential set form, an application credential form, and a TOTP authenticator form. If this check box is selected, the credentials or TOTP seed is fetched from a configured external credential vault. If the check box is selected in the TOTP authenticator form, the seed is fetched from a configured external credential vault. For more information about these forms, see [Create a credential set within a bot process](https://www.servicenow.com/docs/access?context=create-credential-set-botprocess&family=washingtondc&ft:locale=en-US), [Create an application credential set in RPA Hub](https://www.servicenow.com/docs/access?context=create-application-credential&family=washingtondc&ft:locale=en-US), and [Create a TOTP authenticator in RPA Hub](https://www.servicenow.com/docs/access?context=map-totp-credential-set-rpa&family=washingtondc&ft:locale=en-US).

If the application credential record has the **External Credential** check box enabled, then the **SetApplicationCredential** component in RPA Desktop Design Studio doesn’t set the credentials and displays an error. For more information about the **SetApplicationCredential** component, see [Use the SetApplicationCredential component](https://www.servicenow.com/docs/access?context=use-credentials-setappcredential&family=washingtondc&ft:locale=en-US).

Use the steps listed in the [Steps to configure an external credential vault in RPA Hub](https://www.servicenow.com/docs/access?context=config-ext-cred-rpa&family=washingtondc&ft:locale=en-US) topic to guide you through all the tasks of configuring an external credential vault in RPA Hub.

-   **[Storage of process execution data in flat files](https://www.servicenow.com/docs/access?context=bot-process-form&family=washingtondc&ft:locale=en-US)**

In RPA Hub, you can configure the output type as flat files for the execution logs that are generated on the robot machine.

On the Bot Process form, select an output type of the execution log file from the **Output Type** field from the Log Settings section. This field appears when the **Track Execution Logs** option is selected and when the **Robot Machine** is selected from the **Storage** field.

The location of the flat files is `Users\<Userprofile>\ServiceNow RPA Logs\.executionlogs\{InstanceName}\.archive\{ProcessJob number}` in the machine on which you have installed the attended or unattended robot.

If the size of the flat file exceeds 10 MB, it splits into multiple flat files with the log sequence appended to the file names until it executes the automation. A flat file doesn't log the data of input or output ports in a component or method that you have selected as **Mark Data as Sensitive** in the RPA Desktop Design Studio.

-   **[New Workflow Studio Actions and Subflow](https://www.servicenow.com/docs/access?context=rpa-hub-actions&family=washingtondc&ft:locale=en-US)**

Invoke the following new actions and subflow in Workflow Studio:

    -   **Change Life Cycle Stage Status of a Bot Process** Action to modify the life cycle stage status of a bot process that is not retired.
    -   **Stop Process** Action and **Stop Process** subflow to stop a bot process. If the robot pool option is enabled for the bot process, it stops all the robots assigned to the pool. If Graceful Stop is enabled, it provides a capability for robots to exit the automation smoothly. Graceful Stop is not applicable for bot processes with the robot pool option enabled.
-   **[Wait for any screen method at the Universal App Connector level](https://www.servicenow.com/docs/access?context=use-the-wait-for-any-screen-method&family=washingtondc&ft:locale=en-US)**

In RPA Desktop Design Studio, the **WaitForAnyScreen** method appears in the **Object Explorer** pane when you double-click the **Universal App connector** object under the **Global Objects** pane.

The **WaitForAnyScreen** method finds an application screen within a specified duration, and then you can enable it to pass the control to another method. You can set up multiple application screens that appear in an order on the method, and the **WaitForAnyScreen** method tries to find a screen starting from the first application screen by matching the screen match rules. If the method doesn't find a screen, it tries to find the next screen in the order. However, if the method finds a screen, it completes execution and doesn't proceed to the screens next in the order. If the method doesn't find any screen within the specified duration, you may optionally enable it to pass the control to another component through the **ELSE** port.

-   **[SetPassword Method](https://www.servicenow.com/docs/access?context=connectors-chrome-methods&family=washingtondc&ft:locale=en-US)**

In RPA Desktop Design Studio, the **SetPassword** method automates securely entering a password in the password field of a web-based, Java, or Windows application. It accepts the password as a **SECURE STRING** type and then enters it in the password field.

-   **[SimulateMouseEvent Method](https://www.servicenow.com/docs/access?context=connectors-chrome-methods&family=washingtondc&ft:locale=en-US)**

In the RPA Desktop Design Studio, the **SimulateMouseEvent** method automates simulating a mouse event on an element on a web-based application. For example, automate the right-click mouse event on a button to open a context menu. The screen element on which the mouse event occurs must priorly have the mouse event defined in the HTML. The method supports a list of mouse events and mouse button types.

-   **[IEnumerable data type port in connectors](https://www.servicenow.com/docs/access?context=table-connector&family=washingtondc&ft:locale=en-US)**

The **IEnumerable** input data type enables methods to accept arrays, array lists, and lists. This input data type port is available in multiple connectors.

-   **[Universal App connector supports Shadow DOM elements](https://www.servicenow.com/docs/access?context=configure-uac&family=washingtondc&ft:locale=en-US)**

The **XPath** and the **CssSelector** locators in the Universal App connector shows the full XPath and CSS path with the Shadow DOM elements, if a web application uses Shadow DOM.


</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Robotic Process Automation \(RPA\) Hub features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **[Manage plugins from a single location](https://www.servicenow.com/docs/access?context=install-plugins-rpa-studio&family=washingtondc&ft:locale=en-US)**

In the RPA Desktop Design Studio, install, view, update, or remove plugins from the **Plugin Manager** window or the **Plugins** node in the **Project Explorer** pane.

-   **[New location for the Attachments and Workflow Studio components in the Toolbox pane](https://www.servicenow.com/docs/access?context=servicenow&family=washingtondc&ft:locale=en-US)**

In RPA Desktop Design Studio, the Attachments and Workflow Studio components are available under the new ServiceNow category in the Toolbox pane.


</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Robotic Process Automation \(RPA\) Hub features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Robotic Process Automation \(RPA\) Hub features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Robotic Process Automation \(RPA\) Hub.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

Install RPA Hub by requesting it from the ServiceNow Store.

 For cumulative release notes information on RPA Hub, see [RPA Hub release notes](https://servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/platform-app-engine/store-rn-plat-app-engine-rpa-hub.html).

 For cumulative release notes information on RPA Desktop Design Studio, see [RPA Plugin Bundle release notes](https://servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/platform-app-engine/store-rn-plat-app-rpa-plugin-bundle.html).

 For cumulative release notes information on RPA sample templates, see [RPA sample template release notes](https://servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/platform-app-engine/store-rn-plat-app-engine-rpa-sample-template.html).

 If you have previously downloaded the application from the ServiceNow Store and a new version is available, you can update it in your ServiceNow AI Platform instance at **All** &gt; **System Applications** &gt; **All Available Applications**.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Robotic Process Automation \(RPA\) Hub we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

To use the Unattended Robot application, the minimum requirements are as follows:

-   Intel Processor \(1vCPU\).
-   4-GB RAM.
-   Minimum 20-GB free disk space after installing the OS, patches, and base software.
-   Microsoft Windows 10 or Windows Server 2016 or Windows Server 2019.
-   .NET Framework 4.7.1 or later.
-   DPI scaling setting must be deactivated.

 To use the Unattended Robot application, the recommended requirements are:

-   Intel Processor \(4vCPU\).
-   8-GB RAM.
-   Minimum 50-GB free disk space after installing the OS, patches, and base software.
-   Microsoft Windows 10 or Windows Server 2016 or Windows Server 2019.
-   .NET Framework 4.7.1 or later.
-   DPI scaling setting must be deactivated.

 An unattended robot is mapped to only one machine.

 Virtual Machines \(VMs\) that are used for the Unattended Robot application must be persistent and constantly on.

 To use the Attended Robot application, the minimum requirements are as follows:

-   Intel Processor \(1vCPU\).
-   4-GB RAM.
-   Minimum 20-GB free disk space after installing OS, patches, and base software.
-   Microsoft Windows 10 or Windows Server 2016 or Windows Server 2019.
-   .NET Framework 4.7.1 or later.
-   DPI scaling setting must be deactivated.

 To use the Attended Robot application, the recommended requirements are as follows:

-   Intel Processor \(4vCPU\).
-   8-GB RAM.
-   Minimum 50-GB free disk space after installing the OS, patches, and base software.
-   Microsoft Windows 10 or Windows Server 2016 or Windows Server 2019.
-   .NET Framework 4.7.1 or later.
-   DPI scaling setting must be deactivated.

 An attended robot is mapped to only one user.

 To use the RPA Desktop Design Studio application, the minimum requirements are as follows:

-   Intel Processor \(Core i5 or later\)
-   4-GB RAM.
-   20-GB free disk space.
-   Microsoft Windows 10 or Windows Server 2016 or Windows Server 2019.
-   .NET Framework 4.7.1 or later.
-   Monitor with 1920x1080p resolution.
-   DPI scaling setting must be deactivated.

 To use the RPA Desktop Design Studio application, the recommended requirements are as follows:

-   Intel Processor \(Core i7\).
-   8-GB RAM.
-   50-GB free disk space.
-   Microsoft Windows 10 or Windows Server 2016 or Windows Server 2019.
-   .NET Framework 4.7.1 or later.
-   Monitor with 1920x1080p resolution.
-   DPI scaling setting must be deactivated.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Robotic Process Automation \(RPA\) Hub we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

ServiceNow workspaces don’t support mobile devices. For more information about the list of supported browsers, see [Browser support](https://www.servicenow.com/docs/access?context=browser-support&family=washingtondc&ft:locale=en-US).

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Robotic Process Automation \(RPA\) Hub, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Robotic Process Automation \(RPA\) Hub we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

RPA Hub supports international languages. For more information, see [Internationalization support for RPA Hub](https://www.servicenow.com/docs/access?context=rpa-hub-international-language-support&family=washingtondc&ft:locale=en-US).

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Robotic Process Automation \(RPA\) Hub we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   Use the Embedded Task Automation feature to trigger attended bot processes, also known as attended automations, from ServiceNow forms, playbooks, workspaces, and so on.
-   Retrieve sensitive information, such as usernames and passwords, securely from various external vaults by enabling the external credential vault feature in RPA Hub.
-   Store the logs of a process execution in a readable format through flat files.
-   New actions and subflow such as **Change Life Cycle Stage Status of a Bot Process** Action, **Stop Process** Action, and **Stop Process** Subflow are available in the Workflow Studio that further refine RPA integration via flows, subflows, and APIs.
-   Enhanced Universal App Connector.

 See [Robotic Process Automation \(RPA\) Hub](https://www.servicenow.com/docs/access?context=rpa-main-landing-page&family=washingtondc&ft:locale=en-US) for more information.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-washingtondc-australia/rn-combined-intro.md)

