---
title: Off-board a Service Exchange consumer
description: Off-board an on-boarded consumer and remove all related records.
locale: en-US
release: yokohama
product: Service Bridge
classification: service-bridge
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Register a Service Exchange consumer, Use Service Exchange for providers, Service Exchange for Providers, Service Exchange]
---

# Off-board a Service Exchange consumer

Off-board an on-boarded consumer and remove all related records.

## Before you begin

Role required: admin, sn\_sb.admin

## Procedure

1.  Navigate to **All** &gt; **Service Exchange Provider** &gt; **Consumers**.

2.  Select the **Number** column to open the consumer connection record.

3.  Select the **Off-Board Consumer** related link on the form.

    You see a confirmation message indicating that this action off-boards this connection and deletes all related connection records.

4.  Select **OK** to off-board the consumer connection.

5.  If you want to delete all related tasks, select the **Delete all existing tasks for this connection** check box in the confirmation message, and enter **Delete** in the dialog box that appears and select **OK**.

    The consumer is off-boarded and all related data is deleted.


## Result

Records related to the specific consumer connection gets deleted from the following tables:

**Note:** For each table listed, only the records related to the specific consumer connection being off-boarded are deleted.

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
    -   sn\_sb\_pro\_registration
    -   sn\_sb\_pro\_service\_bridge\_settings
    -   sn\_sb\_pro\_authorized\_user
    -   sn\_sb\_pro\_consumer\_connection
    -   sn\_sb\_pro\_entitlement
-   Tasks \(records related to the specific consumer connection are deleted only if you choose to delete all existing tasks\)
    -   sn\_sb\_pro\_provider\_task
    -   sn\_sb\_pro\_remote\_task

