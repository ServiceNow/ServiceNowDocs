---
title: Resize a modal
description: Use declarative actions to resize a modal in your workspace.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure action buttons, Declarative actions, Administer, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Resize a modal

Use declarative actions to resize a modal in your workspace.

## Before you begin

Role required: admin

## About this task

If resizing isn’t required for all record page modals, use declarative actions to resize individual modals.

Declarative actions take higher precedence than system properties.

## Procedure

1.  Navigate to **All** &gt; **Declarative Actions** &gt; **Related List Actions**.

2.  From the Action Assignments list, select a related list action.

    An Action Assignment record opens.

3.  From UX Add-on Event Mappings related list, select the event mapping for opening a modal.

    A UX Add-on Event Mapping record opens.

4.  In the Target Payload Mapping field, enter the following snippet under `“container”: {`.

    ```
                                    "resizableConfig": { 
     "enableResizable": true 
    }, 
    
    ```

5.  Specify the modal’s default size by appending the following snippet.

    ```
    "customSize": { 
                "height": "590px", 
                "width": "1500px" 
            }, 
     
    "size": { 
                "type": "JSON_LITERAL", 
                "value": "custom" 
    }
    
    ```

6.  Select **Update**.


