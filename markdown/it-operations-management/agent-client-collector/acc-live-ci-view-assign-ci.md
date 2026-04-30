---
title: Assign a problematic CI to its incident to view live CI data
description: Retrieve live CI data to help troubleshoot the issues that caused an incident by assigning the problematic CI to its incident. An incident typically is associated with the CI that caused the incident, but if this was omitted during the incident creation, you can assign the CI manually.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [View live CI data with ACC, Agent Client Collector, IT Operations Management]
---

# Assign a problematic CI to its incident to view live CI data

Retrieve live CI data to help troubleshoot the issues that caused an incident by assigning the problematic CI to its incident. An incident typically is associated with the CI that caused the incident, but if this was omitted during the incident creation, you can assign the CI manually.

## Before you begin

Ensure that you have installed Agent Client Collector Framework and Service Operations Workspace on your instance.

Role required: itil

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  Select the Lists icon \(![Lists icon](../image/lists-icon.png)\) icon.

3.  Select **Incidents** &gt; **All**.

4.  Select an incident with a value of **Configuration item = \(empty\)**.

5.  Select the **Live CI Data** tab.

6.  Enter the first several characters of the CI that caused the incident in the **Primary configuration item** field.

    A list of CIs matching the string appears.

7.  Select the relevant CI from the list.

    The name of the CI appears in the **Primary configuration item** field, and the CI's live data appears on the **Live CI Data** tab.


