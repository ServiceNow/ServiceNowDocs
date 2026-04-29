---
title: Use a local data store to pull data from
description: If a large amount of data needs to be queried often, and the data does not need to be real-time, perform a sync of the ServiceNow table that you're interested in with your integrating application's data store.
locale: en-US
release: australia
product: Web Services
classification: web-services
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Strategies, Record retrieval limitations, SOAP web service, Inbound, Web services, API implementation, API implementation and reference]
---

# Use a local data store to pull data from

If a large amount of data needs to be queried often, and the data does not need to be real-time, perform a sync of the ServiceNow table that you're interested in with your integrating application's data store.

## Data push

-   Using a scheduled job, ServiceNow can generate a csv/xml from a report and have it emailed to a specific location. The receiver might have a trigger to take the email attachment, parse it, and populate an internal table from which the application can communicate when the data is needed.
-   Using a schedule job, ServiceNow can generate a csv/xml from a report and FTP it to an public FTP/FTPS location. The integrating product would consume this csv file on a regular basis and populate an internal table from which the application can communicate when the data is needed.

**Note:** Currently, the platform does not provide a method for extracting very large amounts of data and sending the output to an FTP server. However, a customization to perform that function is described at [here](http://www.servicenowguru.com/integration/exporting-report-ftp/). The customization was developed for use in specific ServiceNow instances, and is not supported by ServiceNow Customer support. The method is provided as-is and should be tested thoroughly before implementation. Post all questions and comments regarding this customization to our community [forum](http://community.service-now.com/forum).

## Data pull

Using a cron job, a machine internal to your network can make a wget call to pull csv/xml data from any table within ServiceNow. The integrating product would consume this csv/xml file on a regular basis and populate an internal table from which the application can communicate when the data is needed. Examples of the wget command that would be used:

-   wget --user=itil --password=itil --no-check-certificate https://&lt;instance name&gt;.service-now.com/incident\_list.do?CSV
-   wget --user=itil --password=itil --no-check-certificate https://&lt;instance name&gt;.service-now.com/incident\_list.do?XML

**Parent Topic:**[SOAP strategies](../concept/c_SOAPStrategies.md)

