---
title: Invoke Embedded Task Automation via API in RPA Hub
description: Invoke an attended bot process \(attended automation\) from the UI experiences by creating an action.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Embedded Task Automation \(ETA\), Use, RPA Hub, Workflow Data Fabric]
---

# Invoke Embedded Task Automation via API in RPA Hub

Invoke an attended bot process \(attended automation\) from the UI experiences by creating an action.

The limitation to trigger the attended bot process \(attended automation\) from other UI experiences such as playbook can be resolved by performing the following customisation. By default, the UI action is created for classic or workspace experience to trigger the attended bot process \(attended automation\) when attended configuration is activated.

To create a UI action or edit an existing one, see [Create a UI action](https://www.servicenow.com/docs/access?context=t_EditingAUIAction&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

In the corresponding action, verify that the action visibility is `new sn_rpa_fdn.RPAInstanceFormHooks().canTriggerAutomation(current,’<attended_config_sys_id>`.

Populate the &lt;`attended_config_sys_id`&gt; with the associated Attended Configuration Sys ID.​

The following code must be added to the **Script** section of the corresponding Action form:

```
var rpaFormHooks = new GlideAjax('sn_rpa_fdn.RPAInstanceFormHooks');​

rpaFormHooks.addParam('sysparm_name', 'generateRuntimeLaunchUrl');​

rpaFormHooks.addParam('attendedConfigId’, ‘<attended_config_sys_id>’);​

rpaFormHooks.addParam('recordId', g_form.getUniqueValue());​

rpaFormHooks.getXMLAnswer(function(response) {​

var result = JSON.parse(response);​

if (!result.error) ​

top.window.open(result.url);​

});​
```

**Parent Topic:**[Embedded Task Automation \(ETA\) in RPA Hub](embedded-task-auto-rpa.md)

**Related topics**  


[Embedded Task Automation \(ETA\) in RPA Hub](embedded-task-auto-rpa.md)

[Conditions for the visibility of UI action \(button\)](../reference/visibility-cond-button-rpa.md)

