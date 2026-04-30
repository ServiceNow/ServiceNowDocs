---
title: Application service readiness dashboard in configurable workspace
description: Review the information on the dashboard to ensure that you are ready to discover and map application services based on machine learning \(ML\). Service Mapping uses data processed by Predictive Intelligence to generate suggestions for traffic-based connections.
locale: en-US
release: xanadu
product: Service Mapping
classification: service-mapping
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Service Mapping reference, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Application service readiness dashboard in configurable workspace

Review the information on the dashboard to ensure that you are ready to discover and map application services based on machine learning \(ML\). Service Mapping uses data processed by Predictive Intelligence to generate suggestions for traffic-based connections.

The Application service readiness dashboard is part of Service Mapping Plus, available on the ServiceNow Store.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

Predictive Intelligence evaluates connections between application fingerprints, CIs, and processes, and ranks their relevancy. Service Mapping uses this information to create connections based on connection rules. It also generates connection suggestions for servers and load balancers for you to decide which connections to add or remove from the application services.

Widgets on the ML Dashboard page show the information about prerequisites and issues related to service discovery based on Predictive Intelligence. Select links inside the widgets and reports to navigate to the related list or form.

## Required ServiceNow AI Platform roles

service\_mapping\_admin

## Access the Application service readiness dashboard

To open the dashboard, navigate to **Workspaces** &gt; **Service Mapping**. Then select the Application service readiness icon![application service readiness icon](../image/readiness-dashboard-navigation.png). ![Assessment dashboard](../image/readiness-dashboard.png)

**Note:** Starting with Service Mapping Plus version 1.15.2, the Application service readiness dashboard is updated and includes new information.

## Reports

The dashboard includes the following reports.

<table id="table_qln_b5v_dsb"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Source table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Mapping status of application service

</td><td>

A bar report![Bar report icon](../../../use/reporting/image/icon-bar-report-p.png)

</td><td>

ML-Related Service Status \[ml\_related\_service\_status\]

</td><td>

A bar report that provides the summary of ML-related issues in mapped application services. For detailed information, see [Mapping status of application services](readiness-dashboard-ml.md#section_kpj_npq_xrb).

</td></tr><tr><td>

Application fingerprints training status

</td><td>

A donut report![Donut report icon](../../../use/reporting/image/icon-donut-report-p.png)

</td><td>

AFP Training Status \[afp\_training\_status\]

</td><td>

A donut report that shows the status of application fingerprint training. Predictive Intelligence trains predictive models and machine-learning solutions. View the training status for application fingerprints to understand if your deployment is ready for mapping using Predictive Intelligence.

</td></tr><tr><td>

Discovered connection suggestion status

</td><td>

A donut report![Donut report icon](../../../use/reporting/image/icon-donut-report-p.png)

</td><td>

Connection Suggestions Training Status \[connection\_suggestion\_training\_status\]

</td><td>

A donut report that shows the status of connection suggestions. For details, see [Status of discovered connection suggestions](readiness-dashboard-ml.md#section_nwc_vtr_xrb).

</td></tr></tbody>
</table>## Mapping status of application services

Review the summary of ML-related issues in mapped application services.

|Category|Description|
|--------|-----------|
|Mapped without issues|The number of application services discovered without ML-related issues.|
|Missing source-target AFP|The number of application services missing some application fingerprints for a source or target process. To solve issues, calibrate the fingerprint-based discovery.|
|Missing source-target process|The number of application services missing some source-target process information. To solve these issues, rediscover the target hosts and ensure that the relevant processes are discovered.|
|Confidence level unavailable|The confidence level indicates the likelihood of this connection being part of the service instances. If the confidence level appears as **N/A**, wait until the application fingerprints training is complete.|
|Missing target host|The number of application services with some CI connections not fully discovered, because the horizontal discovery didn't discover host CIs. To solve these issues, rediscover the target hosts and ensure that the relevant processes are discovered.|

## Prerequisites status

Application service mapping requires the integration of several modules and applications: credentials, Predictive Intelligence, enhanced Application Dependency Mapping \(ADME\) discovery, and scheduled jobs. Review the list of prerequisites and ensure that the state of all prerequisites is **Ready**.

<table id="id_jdp_1ps_1sb"><thead><tr><th>

Prerequisite

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Install and enable Predictive Intelligence \(PI\) plugin

</td><td>

Service Mapping uses Predictive Intelligence to generate connection suggestions. 1.  Ensure that the Predictive Intelligence plugin appears **Installed**.
2.  Click the Predictive Intelligence tile and verify that the **Status** is **Active**. If the status is **Inactive**, select the **Activate/Repair** link under **Related Links**.

</td></tr><tr><td>

Enable ADME property

</td><td>

Service Mapping uses ADME probes. Ensure that the **glide.discovery.enable\_adme** property is set to **True**.

</td></tr><tr><td>

Enable all relevant ADME - data collector probes

</td><td>

There are multiple ADME probes for different types of operating systems. Enable all probes necessary to discover configuration items \(CIs\) in your environment.

</td></tr><tr><td>

Assure minimum number of running processes

</td><td>

Check that the clustering solution created enough process groups, which become suggestions. If there are fewer processes than necessary, calibrate fingerprint-based discovery.

</td></tr><tr><td>

Enable application fingerprint \(AFP\) scheduled job

</td><td>

Ensure that the **Applications suggestion - ITOM Autodisco** scheduled job that controls the fingerprint-based discovery is set to **Active**.

</td></tr><tr><td>

Enable Connection Suggestion property

</td><td>

Confirm that discovery based on Predictive Intelligence is enabled. Navigate to the System Property \[sys\_properties\] table and verify that the **sa\_ml.connection\_suggestions.active** property is set to **True**.

</td></tr><tr><td>

Enable connection suggestion scheduled job

</td><td>

Ensure that the **Status** of the **Service Mapping - Traffic Process to Process** scheduled job is **Active**. This schedule job triggers generation of connection suggestions.

</td></tr></tbody>
</table>## Status of discovered connection suggestions

Predictive Intelligence evaluates connections between application fingerprints, CIs, and processes, and ranks their relevancy. Service Mapping uses this information to create connections based on connection rules. It also generates connection suggestions for servers and load balancers for you to decide which connections to add or remove from the application services.

The confidence level indicates the likelihood of this connection being part of the service instances.

-   **High** - This connection is likely to an internal component that is only used by this specific component or application.
-   **Medium** - This connection is likely to a middleware component used by multiple services, such as IBM MQ or Oracle WebLogic Server.
-   **Low** - This connection is likely to an application deployed on numerous servers in the organization, typically for monitoring purposes, such as Tivoli Enterprise Monitoring Agents or MID Server.
-   **Very low** - This connection is likely to a central application used by the entire organization, for example, Microsoft Active Directory or Okta.

You can use connection suggestions without the confidence level for mapping application services.

## Service issues

Review the list of application services most affected by ML-related issues. The list of most affected services is available if the connection suggestions feature is enabled in your deployment. The list shows service names and the number of ML-related issues for each of them. It also indicates if the traffic-based feature is enabled for the services.

**Parent Topic:**[Service Mapping reference](service-mapping-reference.md)

**Related topics**  


[Learn about ADME probes](../../discovery/reference/r_DataCollDiscoTCPConnections.md)

[Enable and configure discovery using ADME probes](../../discovery/reference/r_DiscoveryProperties.md)

[Calibrate fingerprint-based discovery](../../discovery/concept/calibrate-process-based-discovery.md#)

[Ensure that the fingerprint-based discovery generates suggestions](../../discovery/concept/calibrate-process-based-discovery.md#)

[Troubleshooting guide for Service Mapping ML Connection Suggestions \[KB0963421\]](https://support.servicenow.com/nav_to.do?uri=%2Fkb%3Fid%3Dkb_article_view%26sysparm_article%3DKB0963421)

