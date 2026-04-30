---
title: Populating users based on type for ACC-V
description: You can persist the type of users that populate the CMDB depending on your particular interests. Currently, local and system are supported for Windows, Linux, and macOS.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Using Agent Client Collector for Visibility, Agent Client Collector for Visibility, Agent Client Collector, IT Operations Management]
---

# Populating users based on type for ACC-V

You can persist the type of users that populate the CMDB depending on your particular interests. Currently, local and system are supported for Windows, Linux, and macOS.

You can filter the types of users by using the system property: **sn\_acc\_visibility.persist\_os\_user\_type**. See [Available system properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US) for more information.

-   **For Windows**

    You need to identify if a server is domain controller or not. Since domain controller machines don’t have local accounts, local user information does not persist for such machines and is not populated.

    For non-domain controller Windows machines, use OSquery commands to get user information through ACC-V: select `uid`, `username`, `directory`, `type` from users where **type=local** or **type=special**.

-   **For Linux**

    The userID defines if a user is a local account or system account. This is defined by **UID\_MIN** and **UID\_MAX**.

    Use this command to get user information through ACC-V to get **UID\_MIN** and **UID\_MAX** value: `grep -E '^UID_MIN|^UID_MAX' /etc/login.defs`.

    Use this command to get user names: `cat /etc/passwd | awk -F':' '{print $1,$3,$6`.

-   **For macOS**

    Use OSquery commands to get user information through ACC-V: select `uid`, `username`, `directory` from users. User names that are preceded by ‘\_’ are treated as system accounts. Others are local accounts.


**Parent Topic:**[Using Agent Client Collector for Visibility](../concept/acc-v-using-agent-client-collector-for-visibility.md)

