---
title: Set up browser policies
description: Set up the browser policies to enable access to the Browser Extension for Employee Center within the supported browsers.
locale: en-US
release: xanadu
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-07-02"
reading_time_minutes: 1
breadcrumb: [Browser Extension for Employee Center, Setup task management and integration features, Configure, Employee Center, Employee Service Management]
---

# Set up browser policies

Set up the browser policies to enable access to the Browser Extension for Employee Center within the supported browsers.

## Before you begin

Role required: none

**Note:** The enterprise administrator must set up the browser policies.

## About this task

The Browser Extension for Employee Center can be accessed through Google Chrome and Microsoft Edge browsers.

**Note:** The administrator is responsible for setting up the browser policies depending on the supported browser in use.

The browser settings and policy page might look different for different browsers.

## Procedure

1.  Configure the Browser Extension for Employee Center in either of the supported web browsers.

    -   For more information on setting up the Browser Extension for Employee Center in Google Chrome, see [https://support.google.com/chrome/a/answer/14749672?hl=e](https://support.google.com/chrome/a/answer/14749672?hl=e).
    -   For more information on setting the Browser Extension for Employee Center in Microsoft Edge, see [https://learn.microsoft.com/en-us/deployedge/configure-microsoft-edge](https://learn.microsoft.com/en-us/deployedge/configure-microsoft-edge).

        The following is a sample of the JSON file that you must fill to see the policies on the browser.

        ```json
        {
           "Instance": {
             "Value": ""
           },
           "Browser extension portal": {
             "Value": ""
           },
           "Employee portal": {
             "Value": ""
           },
           "Extension title": {
             "Value": ""
           },
           "Extension icon path": {
             "Value": ""
           },
           "Enable notifications": {
             "Value": false
           },
           "Enable context menu": {
             "Value": false
           },
           "Open search in browser extension": {
             "Value": false
           },
           "Allowed sites": {
             "Value": []
           },
           "Context menu title for search": {
             "Value": ""
           },
           "Context menu title for search in portal": {
             "Value": ""
           },
           "Empty state title": {
             "Value": ""
           },
           "Empty state message": {
             "Value": ""
           },
           "Empty state action label": {
             "Value": ""
           },
           "Empty state header logo": {
             "Value": ""
           }
         }
        ```

2.  In the **ServiceNow Employee Center Browser Extension** policy, fill in the fields.

    For a description of the field values, see [Browser Extension policy form](../reference/ecbe-policy-form.md).


