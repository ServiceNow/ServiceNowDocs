---
title: Components installed with Service Mapping Plus
description: Several types of components are installed with activation of the Service Mapping Plus plugin, including tables and scheduled jobs.
locale: en-US
release: zurich
product: Service Mapping
classification: service-mapping
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Service Mapping reference, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Components installed with Service Mapping Plus

Several types of components are installed with activation of the Service Mapping Plus plugin, including tables and scheduled jobs.

**Note:** The Service Mapping Plus application is available in the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

## Scheduled jobs installed

|Scheduled job|Description|
|-------------|-----------|
|Update statistics for application service readiness dashboard|Refreshes the information displayed on the [Application service readiness dashboard](readiness-dashboard-ml.md). Runs hourly. In addition, runs when the **Check Readiness** button is selected on the **Application service readiness dashboard**. The system doesn't trigger this scheduled job sooner than five minutes since the last run.|

## Tables installed

|Table|Description|
|-----|-----------|
|ML-Related Service Status \[ml\_related\_service\_status\]|Contains the information about the ML-related issues in mapped application services.|
|Top ML Error Services \[top\_ml\_err\_services\_list\]|Contains the list of up to 10 application services containing the largest number of ML-related issues.|
|ML Dashboard Prerequisites \[ml\_dashboard\_prerequisites\]|Contains the links to forms and tables that require setting up for mapping based on ML and the status information for these configurations.|
|AFP Training Status \[afp\_training\_status\]|Contains the status of application fingerprint training.|
|Connection Suggestions Training Status \[connection\_suggestion\_training\_status\]|Contains the status of connection suggestions.|
|ML P2P ETA Calculation Constants \[sa\_ml\_p2p\_eta\_values\_list\]|Stores the information on how the system calculates the time remaining for connection suggestion training.|

## Properties Installed

<table id="table_xsw_zn3_3xb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sa.asc.logger\_level

</td><td>

Adds messages to the system log for the application service candidate.-   **Type:** string
-   **Default value:** error
-   **Other possible values:** debug

**Note:** Setting the property to debug displays both debug and error messages.

</td></tr><tr><td>

sa.topdown.enable\_cmdb\_based\_mapping

</td><td>

This property enables CMDB-based mapping using the CMDB instead of the MID Server.-   **Type:** boolean
-   **Default value:** false
-   **Other possible values:** true

</td></tr><tr><td>

sn\_sm\_scoped\_app\_app.sa.unified\_map.enabled

</td><td>

Enables access to the Unified Map through the Service Mapping workspace.-   **Type:** boolean
-   **Default value:** false
-   **Other possible values:** true

</td></tr><tr><td>

sn\_cmdb\_ws\_config\_property.unifiedmap.map\_search.max\_nodes

</td><td>

To ensure high performance, this property limits the number of nodes that can appear on a map.-   **Type:** integer
-   **Default value:** 250

Higher values might decrease performance because Unified Map loads all elements and related details when opened.

**Note:** The **unifiedmap.map\_search.max\_nodes** property in the workspace-specific \[sn\_cmdb\_ws\_config\_property\] table replaces the deprecated **sn\_cmdb\_ws.node.map.max.edge.count** property.

</td></tr><tr><td>

sn\_sm\_scoped\_app.svc\_by\_tags.max\_candidates\_per\_family

</td><td>

Limits the maximum number of tag-based service candidates created for a single family. If the family definition includes more candidates, the most recently updated CIs take precedence. This value applies to all tag-based service families.

-   **Type:** integer
-   **Default value:** 200

</td></tr><tr><td>

sn\_sm\_scoped\_app.max\_valid\_discovery\_period\_in\_days

</td><td>

Sets the maximum number of days a host is considered valid when generating application service candidates. Setting this value to any non-positive integer deactivates this feature.

 **Warning:** If this value is set lower than or too close to the discovery cycle, it might result in the removal of all hosts. Consequently, no new candidates are created and existing candidates are deleted.

 -   **Type:** integer
-   **Default value:** 0

</td></tr></tbody>
</table>**Parent Topic:**[Service Mapping reference](service-mapping-reference.md)

