---
title: Configure the logging level of the ODBC driver
description: Change the logging level of the ODBC driver.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/web-services/t\_CnfgLoggingLevel.html
release: australia
product: Web Services
classification: web-services
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring the ODBC driver, Create data sources from other apps using ODBC driver, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Configure the logging level of the ODBC driver

Change the logging level of the ODBC driver.

## Before you begin

You must have administrator-level access for the Windows computer on which you want to configure the logging level.

Role required: none

## Procedure

1.  In Windows, navigate to **Start** &gt; **Programs** &gt; **ServiceNow ODBC** &gt; **Management Console**.

2.  \[ODBC version 1.0.8\] Within the management console, navigate to **&lt;your\_installation\_directory&gt;** &gt; **Services** &gt; **ServiceNow\_ODBC** &gt; **Service Settings** &gt; **IP Parameters**.

3.  \[ODBC version 1.0.8\] Change the value of the **ServiceJVMOptions** attribute to the desired logging level.

    \[Omitted image "ODBC\_ServiceJVMOptions.png"\] Alt text: ODBC service JVM options

4.  Within the management console, navigate to **&lt;your\_installation\_directory&gt;** &gt; **Services** &gt; **ServiceNow\_ODBC** &gt; **Service Settings** &gt; **Logging**.

5.  Change the value of the **ServiceDebugLogLevel** by selecting all available check boxes.

    \[Omitted image "ODBC\_ServiceDebugLogLevel.png"\] Alt text: ODBC service debug log level

6.  In Windows, navigate to **Start** &gt; **Programs** &gt; **ServiceNow ODBC** &gt; **ODBC Administrator**.

7.  In the ODBC Administrator, select the **Tracing** tab.

8.  Navigate to the path in the **Log File Path** field and delete the old log file, if it exists.

9.  Click **Start Tracing Now**.

10. Enable SOAP debugging for your ServiceNow instance.


**Parent Topic:**[Configuring the ODBC driver](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/configuring-odbc.md)

**Related topics**  


[Generate logs for debugging](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/t_GenerateDebugLogs.md)

[Debug incoming SOAP envelope](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/c_DebuggingIncomingSOAPEnvelope.md)

