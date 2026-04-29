---
title: Disable auto-redirection for all agents to Service Operations Workspace
description: Verify that the agents aren't automatically redirected to Service Operations Workspace after logging in to the ServiceNow instance.
locale: en-US
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Landing page redirection in Service Operations Workspace for ITSM, Getting started with Service Operations Workspace for ITSM, Configuring Service Operations Workspace for ITSM, Service Operations Workspace for ITSM, IT Service Management]
---

# Disable auto-redirection for all agents to Service Operations Workspace

Verify that the agents aren't automatically redirected to Service Operations Workspace after logging in to the ServiceNow instance.

## Before you begin

Role required: admin

## Procedure

1.  From the **All** menu, navigate to sys\_homepage\_destination\_rule.list.

2.  Select the **SOW Landing Page** record.

3.  Clear the **Active** check box.

4.  Select **Update**.

5.  Clear the browser cache by using the following steps:

    1.  Enter `<instance-name>.service-now.com/cache.do` in the web browser.

    2.  Select **Clear Cache**.

        The browser page is refreshed.

    3.  Select **Clear All Browser Caches**.

        The browser page shows the `Unified Cache Cleared` message.

        **Note:**

        If the Homepage Destination Rules \[sys\_homepage\_destination\_rule\] table contains other records that redirect to SOW, use these steps to clear the **Active**  check box for each record.


**Parent Topic:**[Landing page redirection in Service Operations Workspace for ITSM](../concept/landing-page-redirection-sow-itsm.md)

