---
title: Getting started with ODBC
description: Before installing the ODBC driver, create an ODBC user account, assign the odbc role, and define an ACL rule for the odbc role.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/web-services/c\_GettingStartedWithODBC.html
release: australia
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create data sources from other apps using ODBC driver, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Getting started with ODBC

Before installing the ODBC driver, create an ODBC user account, assign the odbc role, and define an ACL rule for the odbc role.



**Note:** Before downloading and installing the ODBC driver, [review the requirements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/r_ODBCDriverInstallationReqs.md) to ensure that your configuration is compatible.

1.  [Create an ODBC user account and assign the odbc role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/t_CreateAnODBCUser.md)  
The ODBC driver communicates with your ServiceNow instance as a specific user. Create an ODBC user account and assign the odbc role to enable the user to communicate via ODBC.
2.  [Define an ACL rule for the odbc role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/t_DefineAnACLRuleForTheODBCRole.md)  
Define an ACL rule for the odbc role to provide read access to the incident table. You can create other ACL rules for the odbc role to provide read access to other tables.

**Parent Topic:**[Create data sources from other apps using ODBC driver](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/c_ODBCDriver.md)

