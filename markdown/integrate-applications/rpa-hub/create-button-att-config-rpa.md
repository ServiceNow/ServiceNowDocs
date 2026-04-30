---
title: Invoke Embedded Task Automation via API
description: Invoke an attended bot process \(attended automation\) from the UI experiences by creating an action.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Managing RPA Hub, RPA Hub, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Invoke Embedded Task Automation via API

Invoke an attended bot process \(attended automation\) from the UI experiences by creating an action.

The limitation to trigger the attended bot process \(attended automation\) from other UI experiences such as playbook can be resolved by performing the following customisation. By default, the UI action is created for classic or workspace experience to trigger the attended bot process \(attended automation\) when attended configuration is activated.

To create a UI action or edit an existing one, see [Create a UI action](https://www.servicenow.com/docs/access?context=t_EditingAUIAction&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

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

**Parent Topic:**[Managing RPA Hub](managing-rpa-hub.md)

**Related topics**  


[Embedded Task Automation in RPA Hub](embedded-task-auto-rpa.md)

[Visibility conditions of the UI action \(button\)](../reference/visibility-cond-button-rpa.md)

