---
title: Configure modal background loading
description: Configure a modal to load large selections of records added to a related list in the background.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure action buttons, Declarative actions, Administer, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Configure modal background loading

Configure a modal to load large selections of records added to a related list in the background.

## Before you begin

Role required: admin

## About this task

If background loading isn’t required for all modals, configure individual modals to load related list records in the background using declarative actions.

Declarative actions take higher precedence than system properties.

## Procedure

1.  Navigate to **All** &gt; **Declarative Actions** &gt; **Related List Actions**.

2.  From the Action Assignments list, select a related list action.

    An Action Assignment record opens.

3.  From the Specify client action field, select **Open Record**.

    An Action Payload Definition record opens.

4.  In the Payload field, add the following snippet before the closing bracket.

    ```
      "asyncProperties": { 
        "enableAsync": true, 
        "relatedListLabelName": "Affected CIs", 
         "asyncThreshold": 100
         } 
    
    ```

    -   `enableAsync`: Set to true to enable background loading.
    -   `asyncThreshold`: The number of records needed to switch to background loading. The value should equal to or greater than one. The default value is 100 records.
    -   `relatedListLabelName`: The display name for the background loading notification.
5.  Select **Update**.

    The Action Assignment record for the related list action opens.

6.  From the UX Add-on Event Mappings related list, select an event mapping.

    A UX Add-on Event Mapping record opens.

7.  In the Target Payload Mapping field, enter the following snippet under `“container”: {`.

    ```
                         "asyncProperties": { 
                           "binding": { 
                                                    "address": [ 
                                                "asyncProperties" 
                                             ] 
                                }, 
                    "type": "EVENT_PAYLOAD_BINDING" 
                            } 
    
    ```

8.  Select **Update**.


## Result

When you select any number of records beyond the threshold, a notification informs you that the records will load in the background.

![MRA notification 1](../image/y-mra-notification-1.png)

When you add the selected records, the modal closes, and a notification confirms that the records are loading in the background.

![MRA notification 2](../image/y-mra-notification-2.png)

After the records are added, a notification informs you that the records were added successfully.

![MRA notification 3](../image/y-mra-notification-3.png)

