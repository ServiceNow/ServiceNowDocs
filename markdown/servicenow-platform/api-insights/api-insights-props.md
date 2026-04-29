---
title: API Insights properties
description: API Insights properties control the behavior of the application.
locale: en-US
release: australia
product: API Insights
classification: api-insights
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reference, API Insights, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# API Insights properties

API Insights properties control the behavior of the application.

## System properties

These system properties are available for API Insights.

**Note:** To open the System Properties \[sys\_properties\] table, enter `sys_properties.list` in the navigation filter.

<table id="table_w4t_nrm_jzb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_api\_insights\_ws.import\_outbound\_rest\_api

</td><td>

Set the property to enable or disable the import of outbound REpresentational State Transfer \(REST\) APIs from your ServiceNow instance to the API Insights workspace.-   Type: string
-   Default value: `{"custom_api":false,"servicenow_api":false}`
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_api\_insights\_ws.import\_outbound\_soap\_api

</td><td>

Set the property to enable or disable the import of outbound Simple Object Access Protocol Application Programming Interface \(SOAP\) APIs from your ServiceNow instance to the API Insights workspace.-   Type: string
-   Default value: `{"custom_api":false,"servicenow_api":false}`
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_api\_insights\_ws.import\_scripted\_rest\_api

</td><td>

Set the property to enable or disable the import of scripted REST APIs from your ServiceNow instance to the API Insights workspace, and set the timeframe for recent activity.-   Type: string
-   Default value: `{"custom_api":false,"servicenow_api":true,"active_in_last":false,"active_in_last_number_of_days":90}`
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_api\_insights\_ws.import\_scripted\_soap\_api

</td><td>

Set the property to enable or disable the import of scripted SOAP APIs from your ServiceNow instance to the API Insights workspace, and set the timeframe for recent activity.-   Type: string
-   Default value: `{"custom_api":false,"servicenow_api":false,"active_in_last":false,"active_in_last_number_of_days":90}`
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_api\_insights\_ws.ml\_min\_cluster\_quality

</td><td>

Enter the minimum cluster quality to display in machine learning recommendations, ranging from `0` to `100`.-   Type: integer
-   Default value: `80`
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_api\_insights\_ws.search\_api\_limit

</td><td>

Enter the desired limit on results for API and API component searches.-   Type: integer
-   Default value: `1000`
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_api\_insights\_ws.settings\_api\_to\_business\_app\_service

</td><td>

Set the property to the relationship model between APIs and business context.-   Type: choice list
-   Default value: `CSDM`
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_api\_insights\_ws.settings\_grant\_access\_workflow

</td><td>

Set the property to the sys ID of the workflow to be executed when an access request is submitted in API Insights.-   Type: string
-   Default value: `API Grant/Reject Access Template`
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_api\_insights\_ws.settings\_preferred\_tool

</td><td>

Set the preferred tool for the creation of new APIs in API Insights.-   Type: choice list
-   Default value: `Authoring tool`
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_api\_insights\_ws.settings\_preferred\_tool\_url

</td><td>

Set the URL for the preferred API authoring tool inAPI Insights. This property value is used when the **settings\_preferred\_tool** property is set to `API Authoring Tool`.-   Type: string
-   Default value: `http://www.postman.com`
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_api\_insights\_ws.settings\_support\_group\_column

</td><td>

Set the column on the Configuration item \[cmdb\_ci\] table that will represent the support group in the API Insights dashboards.-   Type: choice list
-   Default value: `managed_by_group`
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_api\_insights\_ws.show\_ml\_clustering\_recs

</td><td>

Set the property to `false` to disable the clustering recommendations for orphan API components.-   Type: true \| false
-   Default value: `true`
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_api\_insights\_ws.show\_overview\_metrics\_widgets

</td><td>

Set the property to `true` to enable showing the Metric Base widgets on the API and API Component Overview pages.-   Type: true \| false
-   Default value: `false`
-   Location: System Property \[sys\_properties\] table

</td></tr></tbody>
</table>**Parent Topic:**[API Insights reference](../concept/api-insights-reference.md)

