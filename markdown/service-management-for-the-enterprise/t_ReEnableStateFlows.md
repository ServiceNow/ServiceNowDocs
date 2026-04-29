---
title: Re-enable state flows
description: When service management state flows have been disabled, they cannot be re-enabled from the user interface.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Implications of disabling SM state flows, Service management states, Service Management]
---

# Re-enable state flows

When service management state flows have been disabled, they cannot be re-enabled from the user interface.

## About this task

State flows can, however, be re-enabled by running a script for each service management application.

## Procedure

1.  For each service management application, run the following script:

    ```
    var now_GR = new GlideRecord(‘sm_config’);
     gr.get(‘name’, ‘{YOUR_APP_NAME}’); //this can be looked up by navigating to 
     the sm_config list
     gr.use_sf = true;
     gr.update();
    ```


**Parent Topic:**[Implications of disabling SM state flows](../concept/c_ImpDsblStFl.md)

