---
title: ITOM Content Service
description: ServiceNow ITOM Content Service offers extensive visibility of products in your infrastructure. The classification of processes identified by Predictive Intelligence enables wider discovery and weekly updates of new configuration items in the CMDB. Use the Discovery Admin Workspace to review and manage ITOM Content Service suggestions.
locale: en-US
release: xanadu
product: ITOM Visibility
classification: itom-visibility
topic_type: concept
last_updated: "2025-11-09"
reading_time_minutes: 5
breadcrumb: [ITOM Visibility, IT Operations Management]
---

# ITOM Content Service

ServiceNow® ITOM Content Service offers extensive visibility of products in your infrastructure. The classification of processes identified by Predictive Intelligence enables wider discovery and weekly updates of new configuration items in the CMDB. Use the Discovery Admin Workspace to review and manage ITOM Content Service suggestions.

![Discovery admins upload their fingerprints to Data Services, AI librarians tag and classify them and then deliver classifiers back to the admins.](../image/ics-mm-diagram.png "ITOM Content Service Model")

## About ITOM Content Service

ITOM Visibility offers multiple methods of discovering products in your infrastructure. When running discovery with Discovery and Service Mapping Patterns for example, each pattern searches for one version of a product and can offer in-depth visibility of the product's information.

While your infrastructure is growing at scale, and new IT products are rapidly released to the market, you must have wider, rapidly updating visibility. Every week, ITOM Content Service identifies products that you’re currently using and delivers new Configuration Items \(CI\) for your usage. The latest version of Discovery Admin Workspace enables you to refresh the content service suggestions manually before reviewing them.

ITOM Content Service provides the following benefits:

-   Reviews the products that you’re currently using every week and delivers new configuration items \(CIs\).
-   Based on AI, it helps you identify running processes fingerprints and SNMP System OIDs and create the CIs you need for monitoring your infrastructure.
-   Identifies irrelevant processes that aren’t suitable candidates for CIs.
-   Discovers a higher number of products by using AI capabilities that cluster and classify running application processes.

## Benefits of Software Asset Management integration with ITOM Content Service

ITAM Software Asset Management \(SAM\) users benefit from the integration with ITOM Content Service in multiple ways.

-   Gain visibility on the processes currently running on the installed software. This also enables you to find out which installed software doesn't have running processes and might be redundant.
-   ITOM Content Service compliments Software Asset Management in cases of services that don't require installation, for example, an Oracle database that runs as a service and isn’t installed. In cases like this, ITOM Content Service creates the installed software record based on combining the process fingerprint data with the data discovered by SAM. Without ITOM Content Service, you can’t gain this kind of visibility.
-   Using file-based discovery capabilities, ITOM Content Service can discover a running system file that is identified with an app. For example, ITOM Content Service can match an installed software record to an Apache Kafka running an `exe` file. For more information, see [File-based Discovery](file-based-discovery.md).

For more information on Software Asset Management, see [Software Asset Management Content Service](https://www.servicenow.com/docs/access?context=c_SAMContentService&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US).

## Benefits of using Service Mapping with ITOM Content Service

With the latest version of ITOM Content Service, Service Mapping users can leverage Service Fingerprints suggestions to identify and select application services based on classified components. By viewing component details such as product, product category, publisher, and description, you can make informed decisions about which candidates to convert into application services. You can also see which additional processes can be integrated into the service, as certain processes collectively build a comprehensive service when combined.

Both ITOM Content Service suggestions and Service Fingerprints offer automated, weekly suggestions for candidates, but they differ in a few ways.

<table id="table_gcc_3xc_bdc"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Identifies

</th><th>

Focus

</th><th>

Details on publisher

</th><th>

Location

</th></tr></thead><tbody><tr><td>

ITOM Content Service suggestions

</td><td>

Process fingerprints

</td><td>

Individual processes, which could be components of a service or standalone.

</td><td>

Specific actions of a process, offering higher granularity.

</td><td>

Process's publisher.

 If a process is part of a service but has a different publisher, the process provides details only about its own publisher.

</td><td>

**Content service suggestions** tab in Discovery Admin Workspace Content 360

</td></tr><tr><td>

Service Fingerprints

</td><td>

Service fingerprints

</td><td>

Services based on classified components.

</td><td>

The service as a whole, providing a broader perspective.

</td><td>

Service's publisher.

 If a process is part of a service but has a different publisher, the service fingerprint provides details only about the service’s publisher.

</td><td>

**Service Fingerprints** tab in Service Mapping workspace

</td></tr></tbody>
</table>For more information about using Service Fingerprints in Service Mapping, see [Map application services based on Automated Service Suggestions](../../service-mapping/task/map-application-suggestion.md).

For more information about Service Fingerprints candidates, see [KB1706310](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1706310).

## Managing ITOM Content Service with the Discovery Admin Workspace

Review recommended actions and application suggestions and configure discovery through Discovery Admin Workspace.

Note that the Discovery Admin Workspace is supported starting with the Vancouver release.

For more information, see [Discovery Admin Workspace Content 360](discovery-workspace-content-360.md).

## Sharing data on the CDS

The Continuance Delivery System \(CDS\) is a ServiceNow® technology that synchronizes data between the Data Services instance that stores and distributes data and the customer instances.

Opting in to sharing application fingerprint process data with ITOM Content Service through the CDS enables them to be tagged and classified by AI librarians. ITOM Content Service then delivers new CIs every week. Your data is shared with your ServiceNow® instance in a safe environment. You can control access to your data by setting permissions in the Discovery Admin Workspace.

The three options for sharing your data are:

-   Sharing the running processes fingerprint data, which enables access to the Process Groups \[cmdb\_process\_groups\] table.
-   Sharing the SNMP System OIDs data, which enables access to the SNMP OID \[discovery\_snmp\_oid\] table.
-   Sharing the Service Info data of mapped candidates, which enables access to the Application Service Candidate \[application\_service\_candidate\] table \(starting with ITOM Content Service version 1.6.2 and Discovery Admin Workspace version 1.11.0\).

For more information on setting the permissions, see [Share data on ITOM Content Service](../task/share-data-itom-content-service.md)

