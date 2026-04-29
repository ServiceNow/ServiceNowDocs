---
title: Off-board a Service Exchange consumer
description: Off-board an onboarded consumer and remove all related records.
locale: en-US
release: australia
product: Service Bridge
classification: service-bridge
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Register a consumer, Use for providers, Service Exchange for Providers, Service Exchange]
---

# Off-board a Service Exchange consumer

Off-board an onboarded consumer and remove all related records.

## Before you begin

Role required: admin, sn\_sb.admin

## Procedure

1.  Navigate to **All** &gt; **Service Exchange Provider** &gt; **Consumers**.

2.  Select the **Number** column to open the consumer connection record.

3.  Select the **Off-Board Consumer** related link on the form.

    You see a confirmation message indicating that this action will off-board this connection and delete all related connection records.

4.  Select **OK** to off-board the consumer connection.

5.  If you want to delete all related tasks, select the **Delete all existing tasks for this connection** check box in the confirmation message, and enter **Delete** in the dialog box that appears and select **OK**.

    The consumer is off-boarded and all related data is deleted.


## Result

The following tables are deleted:

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
-   Tasks \(records from the following tables are deleted only if you choose to delete all existing tasks\)
    -   sn\_sb\_pro\_provider\_task
    -   sn\_sb\_pro\_remote\_task

**Parent Topic:**[Register a Service Exchange consumer](service-bridge-v2-onboarding.md)

