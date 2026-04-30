---
title: Enable Computer Telephony Integration providers to interact with the Service Operations Workspace
description: Enable an agent \(with the sn\_openframe\_user role\) to receive inbound calls and place outbound calls using the Computer Telephony Integration \(CTI\) interface.
locale: en-US
release: zurich
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring Service Operations Workspace for ITSM to improve your experience, Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Enable Computer Telephony Integration providers to interact with the Service Operations Workspace

Enable an agent \(with the sn\_openframe\_user role\) to receive inbound calls and place outbound calls using the Computer Telephony Integration \(CTI\) interface.

## Before you begin

Enable the following plugins.

-   com.snc.notify
-   com.snc.cti
-   com.sn\_openframe

For more information about installing and enabling a plugin, see [Activate a plugin](https://www.servicenow.com/docs/access?context=t_ActivateAPlugin&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

Role required: admin

## About this task

The CTI integration helps an agent call a user using the phone number in the user profile and contact cards. The ServiceNow application uses the OpenFrame API when an agent initiates a call. The OpenFrame API helps the ServiceNow AI Platform® communicate with the connectors, such as an Amazon connector, already configured in the application.

For more information about CTI integration, see [Integrating with Computer Telephony Integration \(CTI\)](https://www.servicenow.com/docs/access?context=cti-csm-integration&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).

For more information on the various OpenFrame APIs, see [openFrameAPI - Client](https://www.servicenow.com/docs/access?context=c_openFrameAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US).

## Procedure

1.  From the **All** &gt; **sys\_properties.list**.

2.  Open the **sn\_sow.default\_call\_from\_contact\_page** property.

3.  In the **Value** field, specify `CTI`.

4.  Select **Update**.


**Parent Topic:**[Configuring Service Operations Workspace for ITSM to improve your experience](../concept/configuring-sow-to-improve-experience.md)

