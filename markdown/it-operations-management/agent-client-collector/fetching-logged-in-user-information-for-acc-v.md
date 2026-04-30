---
title: Populating Assigned To attribute in Computer CI for ACC-V
description: To update the Assigned To attribute of the Computer CI, you need to collect information from the logged in user.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Using Agent Client Collector for Visibility, Agent Client Collector for Visibility, Agent Client Collector, IT Operations Management]
---

# Populating Assigned To attribute in Computer CI for ACC-V

To update the Assigned To attribute of the Computer CI, you need to collect information from the logged in user.

## Before you begin

Role required: admin

You can automatically populate Assigned to for Windows endpoint devices and macOS devices, like workstations or employee laptops, as part of agent-based Discovery using ACC-VC with the following system properties. See [Available system properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US) for more information.

-   **sn\_acc\_vis\_content.set\_assigned\_to**
-   **sn\_acc\_vis\_content.assigned\_to\_user\_order**

## Procedure

1.  Create higher user privileges to fetch the logged in user details.

    Use Log on As Local System User instead of the default ServiceNow user for running the Agent Client Collector.

    These commands are executed on the Windows machine:

    -   wmic COMPUTERSYSTEM GET USERNAME
    -   From osquery: SELECT l.user FROM logged\_in\_users l JOIN users u ON l.sid = u.uuid WHERE u.type != 'special'
    This command is executed on the macOS machine: SELECT distinct\(l.user\) FROM logged\_in\_users l JOIN users u ON l.user = u.username

2.  User names match is performed on the user records in the sys\_user table.

    The Assigned To attribute is populated and then it creates a reference to the user. Systems logs shows a warning if no user can be found in sys\_user. The user names sourced for Assigned To attribute is based on the system property: **sn\_acc\_vis\_content.assigned\_to\_user\_order**.

3.  Assigned\_to attribute is set based on priorities.

    If assigned\_to is already there, keep it as is by default. However, you can update the **sn\_acc\_vis\_content.set\_assigned\_to** system property to override it. If there are any Reconciliation Rules defined, then the IRE populates the field accordingly.


## Result

No new user account is created in the sys\_user table. Instead, the existing user is queryied and the same is referenced as Assigned To user for a CI.

**Parent Topic:**[Using Agent Client Collector for Visibility](../concept/acc-v-using-agent-client-collector-for-visibility.md)

