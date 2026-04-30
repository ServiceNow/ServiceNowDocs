---
title: Resize select modals in Configurable Workspace
description: Use declarative actions to enable resizing for select modals in your Configurable Workspace.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Resize all record page modals in Configurable Workspace, Administering Configurable Workspace, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Resize select modals in Configurable Workspace

Use declarative actions to enable resizing for select modals in your Configurable Workspace.

## Before you begin

Role required: admin

## About this task

If resizing isn’t required for all record page modals, use declarative actions to enable resizing for select modals.

Configuration at the declarative action level takes higher precedence than system properties.

## Procedure

1.  Navigate to **All** &gt; **Declarative Actions** &gt; **Related List Actions**.

2.  Open a related list action.

3.  From the UX Add-on Event Mapping, select the event mapping for opening a modal.

4.  Add the following snippet to the Target Payload Mapping field under `“container”: {`.

    ```
                                    "resizableConfig": { 
     "enableResizable": true 
    }, 
    
    ```

5.  Specify the modal’s default size by adding the following snippet under your previous addition.

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


