---
title: Configure ribbon settings for case types
description: Create a new ribbon configuration for a case type or enable ribbon configurations to be inherited by the case type.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring customer service case types, Customer service case types, Case management, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Configure ribbon settings for case types

Create a new ribbon configuration for a case type or enable ribbon configurations to be inherited by the case type.

## Before you begin

Role required: admin

## About this task

In the Customer Service Management application, a case type represents the data and processes that are needed to resolve a specific type of customer issue. The system administrator can create a table for a new case type that extends the Case table \(sn\_customerservice\_case\). The extended table for the case type inherits most of the functionality of the Case table.

As part of configuring forms, you can configure ribbon settings for case types. The ribbon appears at the top of the form and includes components that display customer and case information, such as Customer 360, Timeline, and Active SLA. Each component has a ribbon setting that stores configuration information about that component.

Case types that are extended from the Case table can display these components in the ribbon on the Case form. For case types, you can do the following:

-   Create new ribbon settings for case extensions, or
-   Modify existing ribbon settings so that the case extensions inherit the ribbon component behavior.

To create new ribbon settings, see Set up ribbons in workspace.

To modify ribbon component behavior, use the procedure below.

## Procedure

1.  Navigate to **All** &gt; **Workspace Experience** &gt; **Forms** &gt; **Ribbon Settings**.

2.  Select the component name in the Ribbon Settings list.

    For example, you can select Customer 360.

3.  On the Ribbon Setting form for the selected component, enable the **Inherit** check box.

4.  Select **Update**.

5.  Repeat steps 2 to 4 for each component to be displayed in the ribbon.


