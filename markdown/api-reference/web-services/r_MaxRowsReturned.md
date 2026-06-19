---
title: Specify the maximum number of rows returned
description: By default, ServiceNow only returns 100 rows of data with each iSQL query. If you need to return more rows of data, set the maxrows parameter for the iSQL session.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/api-reference/web-services/r\_MaxRowsReturned.html
release: zurich
product: Web Services
classification: web-services
topic_type: reference
last_updated: "2025-07-31"
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

\[Omitted image "isql\_shortcut\_maxrows.png"\] Alt text: iSQL shortcut properties

**Parent Topic:**[Use Interactive SQL with ODBC](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/web-services/t_UsingInteractiveSQLWithODBC.md)

