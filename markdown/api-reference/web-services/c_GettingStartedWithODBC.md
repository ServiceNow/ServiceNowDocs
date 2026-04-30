---
title: Getting started with ODBC
description: Before installing the ODBC driver, create an ODBC user account, assign the odbc role, and define an ACL rule for the odbc role.
locale: en-US
release: zurich
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create data sources from other apps using ODBC driver, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Getting started with ODBC

Before installing the ODBC driver, create an ODBC user account, assign the odbc role, and define an ACL rule for the odbc role.



**Note:** Before downloading and installing the ODBC driver, [review the requirements](../reference/r_ODBCDriverInstallationReqs.md) to ensure that your configuration is compatible.

1.  [Create an ODBC user account and assign the odbc role](../task/t_CreateAnODBCUser.md)  
The ODBC driver communicates with your ServiceNow instance as a specific user. Create an ODBC user account and assign the odbc role to enable the user to communicate via ODBC.
2.  [Define an ACL rule for the odbc role](../task/t_DefineAnACLRuleForTheODBCRole.md)  
Define an ACL rule for the odbc role to provide read access to the incident table. You can create other ACL rules for the odbc role to provide read access to other tables.

**Parent Topic:**[Create data sources from other apps using ODBC driver](c_ODBCDriver.md)

