---
title: Prepare a CSV file for mapping your candidates
description: Organize information about potential application services \(candidates\) in your organization and save it in a CSV file.
locale: en-US
release: yokohama
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Map multiple application services from a CSV file using classic Service Mapping, Application service mapping using classic Service Mapping, Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Prepare a CSV file for mapping your candidates

Organize information about potential application services \(candidates\) in your organization and save it in a CSV file.

## Before you begin

Role required: service\_mapping\_admin

## About this task

## Procedure

1.  Create an .xlsx file.

2.  Define entry point attributes for service candidates in the .xlsx file.

    Customers use these entry points to access services. For example, they use http://www.google.com:8080 to access the Google page.

    **Warning:** Do not confuse column order in the .xlsx file. Entering attributes in wrong columns causes mapping errors.

<table id="table_spv_tbv_tw"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

A

</td><td>

Enter a unique name of the planned service instance. For example, NY Public Library or Google.**Warning:** Service Mapping imports only application services with unique names.

 If there is more than one entry with the same name in CSV files you use, the latest imported record overwrites the previous ones.

</td></tr><tr><td>

B

</td><td>

\(Optional\) If you know the URL that serves as the entry point to your service instance, enter it in this column. For example, enter https://www.nypl.org/ or www.google.com:8080. **Warning:** If you define the URL, you do not have to define the IP address, port, FQDN, and protocol. Service Mapping parses the URL to extract the IP address, port, and FQDN.

 If there is no URL that serves as the entry point, define other parameters in columns C, and E.

</td></tr><tr><td>

C

</td><td>

\(Optional\) The IP address of the entry point in the IPv4 format. Enter this parameter only if you did not enter the URL in column B.

</td></tr><tr><td>

D

</td><td>

\(Optional\) The port of the entry point. For example, 8080 for the Google page. Enter this parameter only if you did not enter URL in column B.If you did not enter either URL or the port, Service Mapping uses port 80 for the http protocol and port 443 for the https protocol.

</td></tr><tr><td>

E

</td><td>

\(Optional\) The FQDN of the service entry point, for example,www.google.com for Google. Enter this parameter only if you did not enter the URL in column B.

</td></tr></tbody>
</table>3.  Save the file in a drive that you can access during the import with the **.csv** extension.


## What to do next

[Map multiple application services from a CSV file using classic Service Mapping](import-business-services-csv.md)

**Parent Topic:**[Map multiple application services from a CSV file using classic Service Mapping](import-business-services-csv.md)

