---
title: Enable asynchronous record addition for select modals
description: Use declarative actions to enable asynchronous record addition for select multi-record associator modals.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Enable asynchronous record addition for the multi-record associator, Administering Configurable Workspace, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Enable asynchronous record addition for select modals

Use declarative actions to enable asynchronous record addition for select multi-record associator modals.

## Before you begin

Role required: admin

## About this task

If asynchronous record addition isn’t required for all modals, use declarative actions to enable asynchronous record addition for select multi-record associator modals.

Configuration at the declarative action level takes higher precedence than system properties.

## Procedure

1.  Navigate to **All** &gt; **Declarative Actions** &gt; **Related List Actions**.

2.  Open a related list action.

3.  Open the record in the Specify client action field.

4.  In the Payload field, add the following code snippet before the closing bracket.

    ```
      "asyncProperties": { 
        "enableAsync": true, 
        "relatedListLabelName": "Affected CIs", 
         "asyncThreshold": 100
         } 
    
    ```

    -   `enableAsync`: Set to true to enable asynchronous record addition.
    -   `asyncThreshold`: The number of records needed to switch to asynchronous record addition. The value should equal to or greater than one. The default value is 100 records.
    -   `relatedListLabelName`: The display name for the notification related to the asynchronous record addition.
5.  Select **Update**.

6.  From the UX Add-on Event Mapping for the related list, select a record.

7.  Add the following snippet to the Target Payload Mapping field under your selected container.

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

