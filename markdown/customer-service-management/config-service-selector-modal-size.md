---
title: Configure the service selector modal size
description: The service selector modal displays a list of available services to an agent when they are creating a case. Users with the admin role can configure the size of the service selector modal.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring customer service case types, Customer service case types, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Configure the service selector modal size

The service selector modal displays a list of available services to an agent when they are creating a case. Users with the admin role can configure the size of the service selector modal.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to the **sys\_declarative\_action\_payload\_definition.list** in the application navigator to display the Action Payload Definitions list.

2.  Filter the **Label** field to display Case Type Selector.

3.  Select the desired record from the **Key** column.

4.  Edit the record and change the size of the modal in the **Payload** field.

    The following choices are available: small, medium, large, xl. For example, enter: `"size": "xl",`

5.  Select **Update**.


