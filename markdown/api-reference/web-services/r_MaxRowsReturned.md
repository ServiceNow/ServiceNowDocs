---
title: Specify the maximum number of rows returned
description: By default, ServiceNow only returns 100 rows of data with each iSQL query. If you need to return more rows of data, set the maxrows parameter for the iSQL session.
locale: en-US
release: australia
product: Web Services
classification: web-services
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use Interactive SQL with ODBC, ODBC and client applications, Create data sources from other apps using ODBC driver, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Specify the maximum number of rows returned

By default, ServiceNow only returns 100 rows of data with each iSQL query. If you need to return more rows of data, set the maxrows parameter for the iSQL session.

To return all rows set `maxrows` to zero:

```
maxrows 0
```

To return more than 100 rows set `maxrows` to a higher value. For example, to return 500 rows:

```
maxrows 500
```

**Note:** If running the Interactive SQL console from a shortcut, you must modify the shortcut **Target** to include the **-maxrows** parameter with the desired value.

![iSQL shortcut properties](../image/isql_shortcut_maxrows.png)

**Parent Topic:**[Use Interactive SQL with ODBC](../task/t_UsingInteractiveSQLWithODBC.md)

