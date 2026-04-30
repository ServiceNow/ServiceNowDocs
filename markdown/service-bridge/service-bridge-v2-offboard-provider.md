---
title: Off-board a Service Exchange provider
description: Off-board a provider connection and delete all related records.
locale: en-US
release: yokohama
product: Service Bridge
classification: service-bridge
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Registering with a provider, Installing and configuring Service Exchange for Consumers, Service Exchange for Consumers, Service Exchange]
---

# Off-board a Service Exchange provider

Off-board a provider connection and delete all related records.

## Before you begin

Role required: admin, sn\_sb.admin

## Procedure

1.  Navigate to **All** &gt; **Service Exchange Consumer** &gt; **Provider Connections**.

2.  Click on the **Number** column to open the provider connection record.

3.  Click **Off-Board Provider**.

    You will see a confirmation message indicating that this action will off-board this connection and delete all related connection records.

4.  Click **OK** to off-board the provider connection.

5.  If you want to delete all related tasks, select the **Delete all existing tasks for this connection** check box in the confirmation message, and enter **Delete** in the dialog box that appears and click **OK**.

    The consumer will be off-boarded and all related data will be deleted.


## Result

Records related to the specific provider connection gets deleted from the following tables:

**Note:** For each table listed, only the records related to the specific provider connection being off-boarded are deleted.

-   Connection tables:
    -   ih\_sync\_capture\_definition
    -   ih\_sync\_outbound\_definition
    -   ih\_sync\_inbound\_definition
    -   ih\_sync\_process\_event
    -   ih\_sync\_remote\_system
    -   http\_connection
    -   sys\_user
    -   sys\_user\_has\_role
    -   sys\_alias
    -   oauth\_2\_0\_credentials
    -   oauth\_credential
    -   oauth\_requestor\_profile
    -   oauth\_entity\_profile
    -   oauth\_entity
    -   sn\_sb\_rps\_connection
    -   sn\_transport\_queue
    -   sn\_transport\_profile
    -   sn\_sb\_con\_service\_bridge\_settings
    -   sn\_sb\_con\_authorized\_user
    -   sn\_sb\_con\_persona
    -   sn\_sb\_con\_provider\_connection
    -   sn\_sb\_con\_entitlement
-   Records related to the specific provider connection are deleted from the following tables only if you select the **Delete all existing tasks for this connection** check box in the confirmation dialog:
    -   Tasks
        -   sn\_sb\_con\_provider\_task
        -   sn\_sb\_con\_remote\_task
    -   Entitlements
        -   sn\_sb\_con\_remote\_record\_producer
            -   item\_option\_new
            -   item\_option\_new\_set
        -   sn\_sb\_con\_remote\_task\_def
            -   sn\_sb\_con\_remote\_task\_variable
            -   sn\_sb\_con\_inbound\_field
            -   sn\_sb\_con\_outbound\_field

