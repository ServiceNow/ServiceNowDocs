---
title: Configure data items in offline mode
description: Define a separate data item for offline mode, giving you the flexibility to define the amount of data to display when a user is offline.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Offline mode, Considerations before implementation, ServiceNow Mobile Platform configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Configure data items in offline mode

Define a separate data item for offline mode, giving you the flexibility to define the amount of data to display when a user is offline.

## Before you begin

Role required: admin

## About this task

Use the Mobile Offline properties area to specify the type and amount of information to display to a user when they are in offline mode. For example, you can display a month’s worth of tasks in online mode and only three days’ worth in offline mode. In both online and offline modes, the data item type is always the same and the information is extracted from the same table. For more information, see [Data items](../concept/sg-data-item.md).

**Note:** If a data item is not created for offline mode, then the standard data item is used for both offline and online modes.

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select **All mobile records** from the menu.

4.  From the **Record type** field, select **Data Item \[sys\_sg\_data\_item\]** and then either select **New** or an existing record.

5.  In the Offline Properties area, define offline mode query conditions for the data item to conform to.

    Create conditions using the [Condition builder](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

    **Note:** **Declarative** and **Scripts** are supported conditional types.

6.  Select **Save**.


**Parent Topic:**[Offline mode](../concept/mobile-offline-mode.md)

