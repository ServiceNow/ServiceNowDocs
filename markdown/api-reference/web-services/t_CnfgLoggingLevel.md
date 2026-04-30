---
title: Configure the logging level of the ODBC driver
description: Change the logging level of the ODBC driver.
locale: en-US
release: yokohama
product: Web Services
classification: web-services
topic_type: task
last_updated: "2025-01-30"
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

    ![ODBC service JVM options](../image/ODBC_ServiceJVMOptions.png)

4.  Within the management console, navigate to **&lt;your\_installation\_directory&gt;** &gt; **Services** &gt; **ServiceNow\_ODBC** &gt; **Service Settings** &gt; **Logging**.

5.  Change the value of the **ServiceDebugLogLevel** by selecting all available check boxes.

    ![ODBC service debug log level](../image/ODBC_ServiceDebugLogLevel.png)

6.  In Windows, navigate to **Start** &gt; **Programs** &gt; **ServiceNow ODBC** &gt; **ODBC Administrator**.

7.  In the ODBC Administrator, select the **Tracing** tab.

8.  Navigate to the path in the **Log File Path** field and delete the old log file, if it exists.

9.  Click **Start Tracing Now**.

10. Enable SOAP debugging for your ServiceNow instance.


**Parent Topic:**[Configuring the ODBC driver](../concept/configuring-odbc.md)

**Related topics**  


[Generate logs for debugging](t_GenerateDebugLogs.md)

[Debug incoming SOAP envelope](../../inbound-soap/concept/c_DebuggingIncomingSOAPEnvelope.md)

