---
title: View components installed with Security Support Common
description: Several types of components are installed when you activate the Security Support Common plugin including but not limited to tables, user roles, and modules.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Components installed with Security Support Common, Security Operations common functionality, Security Operations]
---

# View components installed with Security Support Common

Several types of components are installed when you activate the Security Support Common plugin including but not limited to tables, user roles, and modules.

## Locating components

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

If you want to limit the list of installed components to roles, scheduled jobs, and tables for the Security Support Common application, follow these steps:

## View filtered lists for components installed with an application

Filter the Applications Files table so that only the roles, scheduled jobs, and tables that are installed with an application are displayed. The application you want to view these components for should be installed so that its files are loaded onto the instance and into the metadata table. Follow these steps to view filtered lists from the Applications Files table.

1.  In the filter navigator, enter **sys\_metadata.list** to navigate to the metadata table.
2.  Select the condition builder \(filter icon\), and select, **Application** &gt; **is** followed by the name of your application.
3.  In the condition builder, to add a second filter, click **AND**, then select, **Class** &gt; **is a** and choose one of the following classes from the list: **Role**, **Scheduled job**, or **Table**.
4.  Select **Run**.

The results for the class you selected are displayed in a filtered list.

**Parent Topic:**[Components installed with Security Support Common](install-with-sec-sup-common.md)

