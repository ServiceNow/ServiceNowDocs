---
title: Service instances \(Application services\)
description: Understand service instances \(application services\), learn about different application service types and how multiple ServiceNow business units and products use them.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 14
breadcrumb: [Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Service instances \(Application services\)

Understand service instances \(application services\), learn about different application service types and how multiple ServiceNow® business units and products use them.

**Note:** Application service is being renamed to service instance. Both terms are being used interchangeably in this section.

## What service instances \(application services\) are

A service instance is a set of interconnected applications and hosts that are configured to offer a service to the organization. Service instances can be internal, like an organization email system or customer-facing, like an organization website. For example, creating financial reports through a web-based application requires a computer, web server, application server, databases, middleware, and network infrastructure. These applications and hosts are all configured to offer the service of financial reporting. In development environments, an application service represents an instance of a business application or system.

ServiceNow applications refer to devices and applications that comprise an application service as configuration items \(CIs\). The various CIs and the relationships between them, that comprise an application service, are stored in the Configuration Management Database \(CMDB\).

Each application service contains an entry point as the top-level CI. An entry point is a point where clients access a service instance. Typically, it is a URL, or a combination of the IP address and port for application services in enterprise deployments. For cloud-based deployments, an entry point can be a URL to a cloud resource like an AWS gateway.

![Application service diagram.](../image/top-down-diagram.png "Application service")

The Common Service Data Model \(CSDM\) helps you streamline service types and service offerings. You can add relationships between application services and other service-related objects in the CSDM: Business Application, Technical Service Offerings, or Business Service Offerings.

There are the following types of application services:

-   **Discovered**

    Service Mapping discovers application services using patterns and by following traffic connections.

    Pattern-based discovery creates precise and complete application services that represent the service-centric view of the IT infrastructure. It creates a high-fidelity map that is well suited to managing mission-critical application services.

    In addition, it provides visibility of cloud-native services such as compute, load balancers, and API gateways. You can use service entry points such as AWS S3 buckets, AWS and Microsoft Azure API gateways, AWS Lambda functions, and Microsoft Azure functions to map services. It can also detect Lambda to Lambda calls and Lambda to RDS connections to build dynamic service maps.

    Top-down method maps VMs on-premises and in public clouds. However, it requires these VMs to be fully discovered for the top-down discovery to determine which applications are running in the VM. If a VM isn't fully discovered, use the tag-based method to bridge the gap \(see later in this document\). Tag-based mapping also maps containers, that you cannot map using the top-down discovery.

    Discovered application services have the service classification of application service. They are stored in the Mapped Application Service \[cmdb\_ci\_service\_discovered\] table.

-   **Dynamic CI Group**

    Dynamic CI groups which act as application services. The members of the [CMDB groups](cmdb-groups.md#) that is associated with the dynamic CI group, populates the application service. A dynamic CI group is a dynamic grouping of CIs, based on some common criteria such as the location of all web servers in Detroit or all Oracle databases in Boston. After creating a dynamic CI group, it can be used as a group offering in IT Service Management.

    If created from the Application Service wizard, the service classification is application service, and if created from the legacy Event Management UI or Service Mapping UI, the classification is technical service. Application services of the Dynamic CI Group type are stored in the Dynamic CI Group \[cmdb\_ci\_query\_based\_service\] table.

-   **Tag-based**

    A tag is a label that consists of a key-value pair. Your organization may use tags to categorize its assets, to enhance query and reporting capabilities. Discovery and Cloud Provisioning and Governance can discover tags used by all major cloud providers and container ecosystems. Once the tags are discovered, Service Mapping can create service instances based on these tags. For example, you can use tags to map all application services your organization uses in the production environment in the EMEA region.

    Tag-based application services have the service classification of application service. They are stored in the Tag-based Application Service \[cmdb\_ci\_service\_by\_tags\] table.

-   **Created Manually**

    With manual mapping, application owners manually document the applications, IT infrastructure, and relationships that support each application service. This methodology is the best fit for configuration items that are not fully discoverable due to security access issues. For example, IPS devices which support an intrusion prevention service for the security business unit.

    Try to avoid manual mapping wherever possible. It’s incredibly time consuming to map services manually, and often the information needed for mapping is not available due to evolving technology and a lack of processes that track and document the infrastructure dependencies needed for application context. And, whenever subsequent changes are made to the application service topology, the service map must be manually updated.

    Manually created application services have the service classification of application service. Application services of the created manually type are stored in the Mapped Application Service \[cmdb\_ci\_service\_discovered\] table.

-   **Dynamic**

    A dynamic application service includes only CIs that are part of CI relationships stored in the CMDB CI Relationship \[cmdb\_rel\_ci\] table.

    You can't edit a dynamic application service by directly adding or removing CIs from it. Dynamic application services are updated automatically to reflect any change to CI relationships in the CMDB CI Relationship \[cmdb\_rel\_ci\] table. When you add a relationship to a CI that is contained in a dynamic application service, then that service automatically updates to reflect the addition of the relationship and the associated new CI. In a similar manner, a dynamic application service automatically updates upon the removal of a relationship and its associated CI from a CI within the service.

    One way to create dynamic application services, is by converting legacy business services or legacy manual services \(created with Event Management, for example\) into application services of the dynamic type.

    Dynamic application services have the service classification of application service. Dynamic application services are stored in Calculated Application Services \[cmdb\_ci\_service\_calculated\] table.


## Who uses application services

Application services provide foundation for operation of the following business units and products of the ServiceNow AI Platform:

-   [ITOM Health](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-health-landing-page.md) gathers alerts from infrastructure events captured by third-party monitoring tools. It then uses IT-related information gathered by Discovery to map alerts to configuration items. Based on the collected information, then provides dashboards showing a consolidated view of all service-impact events.
-   [ITOM Optimization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-optimization-landing-page.md) gives you tools to provision private and public cloud infrastructure and services and to achieve consistent management and cost visibility. The [Cloud Cost Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/cloud-insights-landing-page.md) application, available in the ServiceNow Store, helps you to analyze the full range of costs associated with cloud assets so you can identify and take action on opportunities to save money and optimize operations.
-   [IT Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/r_ITServiceManagement.md) users rely on the application services reflecting the IT infrastructure to manage and deliver services to their customers.
-   Customer Service Management users efficiently diagnose and resolve issues related to the IT infrastructure in the context of application services.
-   [Software Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/c_SoftwareAssetMgmt.md) users understand the software running in your IT environment and track configurations that impact software license consumption across your IT environments and datacenters.
-   [Strategic Portfolio Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/r_ITBusinessManagement.md) users utilize data collected for application services to gain a comprehensive understanding of the applications used in your organization.

## How to create application services

Depending on the needs of your organization, you can deploy different methods of creating and populating application services.

**Important:** You can use the top-down and manual methods for the same application service. You cannot combine any other methods for creating or populating the same application service.

Analyze the IT infrastructure and service deployment in your organization to pick the optimal method of creating and populating application services.

<table id="table_ubz_lkj_mlb"><thead><tr><th>

Method

</th><th>

When to use

</th><th>

Additional considerations

</th></tr></thead><tbody><tr><td>

[Top-down discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/pattern-based-discovery.md) Service Mapping performs top-down discovery of application services. Service Mapping uses patterns to discover and map CIs. A pattern is a sequence of steps whose purpose is to detect attributes of a CI and its outbound connections. This method creates precise and complete application services that reliably represent the service-aware view of your organization's IT infrastructure

 [Tag-based discovery in Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/tag-based-mapping.md) is a complimentary method that enriches the results of top-down discovery.

</td><td>

Use this method to discover industry-recognized or customized second-tier and third-tier applications. Such applications may include load-balancing solutions, application or web servers with database connections.

</td><td>

Pattern-based mapping requires configuring credentials, users, and user permissions to let Service Mapping access applications inside your organization private network. This process may take time and effort.

</td></tr><tr><td>

[Tag-based](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/tag-based-mapping.md) If your organization uses tags for asset management, you can use these tags to map application services. Discovery and Cloud Provisioning and Governance discover tags assigned to CIs, and populate the CMDB with this data. Service Mapping uses the tag-related data from the CMDB to map services.

 Tag-based service mapping complements top-down service mapping. It provides visibility of containers and also maps VMs that aren’t fully discovered, which top-down service mapping is unable to do. However, while tag-based mapping associates tagged components with specific application services, it doesn’t map the connections between these components—This is another reason why tag-based mapping complements rather than replaces top-down service mapping.

</td><td>

Map resources on cloud workloads like IaaS/Paas/FaaS/CaaS as well as on container workloads using Kubernetes, OpenShift, or AWS ECS.Also, map resources in the Site Reliability Engineering \(SRE\) or Customer Reliability Engineering \(CRE\) deployments.

 Using tag-based method, you can map container resources in your deployments.

 Typically, you use this method to discover applications on cloud virtualizations or PaaS deployments.

</td><td>

Unlike other mapping methods, tag-based mapping doesn't require configuring credentials or providing users with elevated rights.Tag-based application services may not include relevant CIs, if these CIs don't have correct tags assigned to them.

</td></tr><tr><td>

Ingesting Application Performance Management \(APM\) maps from integrated Dynatrace or AppDynamics deploymentsCreate application services using the integration with [AppDynamics application model](https://store.servicenow.com/sn_appstore_store.do#!/store/application/3671b358db0d2200b141d6fdbf9619de/3.0.9?referer=%2Fstore%2Fsearch%3Fapptype%3Dintegrations%25253Bnonintegrations%26q%3DAppDynamics&sl=sh) and [Dynatrace monitoring](https://store.servicenow.com/sn_appstore_store.do#!/store/application/9f77f7a94f9f1200dbec7bb28110c7c2/2.6.0?referer=%2Fstore%2Fsearch%3Fapptype%3Dintegrations%25253Bnonintegrations%26q%3Ddynatrace&sl=sh) platform available on ServiceNow Store.

</td><td>

Use this integration to create application services based on APM maps from Dynatrace or AppDynamics. You are able to use application services created by this method for monitoring Health.

</td><td>

Analyze discovered resources in the CMDB before ingesting from 3rd party to avoid creating duplicate CIs.

</td></tr><tr><td>

[Populate an application service using the Dynamic CI Group method](../task/populate-app-service-dynamic-group.md) Based on CMDB groups, whose members populate the application service.

</td><td>

Use this method as a simple and fast way to create dynamic CI groups for deployments including Microsoft Active Directory, Microsoft Exchange or other DNS-related services. Dynamic CI Groups are especially useful if only a list of resource is available, without configuration details or credentials.Using a CMDB group lets you use CMDB Health to monitor health, and use a CMDB Query Builder saved query to filter for the CIs included in the application service.

</td><td>

There is no map view for application services created using this method. You can only view CIs belonging to such an application service as a list.

Need to ensure that the CMDB group accurately filters for the CIs that should be included in the application service.

</td></tr><tr><td>

[Application service API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/rest-apis/application-service-api.md) Create an automation for creating application services in bulk. Use this method, if your organization has performed cross-organization mapping and analysis and collected some information about services.

Application services created using APIs belong to the manual type are stored in the Mapped Application Service \[cmdb\_ci\_service\_discovered\] table.

</td><td>

Use this method for environments that require tracing of DevOps Continuous Integration/Continuous Deployment \(CI/CD\) process. You can import third-party service maps into manual application services individually or in bulk. For example, see the [Digital Guidebook: Importing 3rd-party service maps into ServiceNow Service Mapping](https://developer.servicenow.com/connect.do#!/event/knowledge19/LAB0577/knowledge19_LAB0577_bind_imported_cis_to_an_application_service).

</td><td>

Be familiar with the exact service structure: sys\_id of each CI comprising the service and the hierarchy that the CIs form. This method requires knowledge of the scripting infrastructure that your organization uses.

</td></tr><tr><td>

[Populate an application service using the Manual method](../task/populate-app-service-manual.md) Create a manual application service with one CI only: the entry point. To populate a manually created application service, add other CIs manually as described in [Manually add CIs to an application service](../../service-mapping/task/manually-add-ci-to-business-service.md).

 Alternatively, create and populate manual application services by [converting business services](../../service-mapping/concept/convert-bus-to-app-svc-intro.md#) created in the CMDB and stored in \[cmdb\_ci\_service\].

</td><td>

Use the manual method if you can't use other methods of creating or populating application services.

 Create application services manually for intrusion prevention.

</td><td>

This method doesn't require any preexisting setup or object configuration.You can include CIs of any class in manually created application services.

 Manually created application services reflect some changes to CIs, like CI attributes. However, they do not automatically reflect changes to CI relationships.

</td></tr><tr><td>

[Populate an application service using the Dynamic Service method](../task/populate-app-service-dynamic-service.md) Application services that automatically update to reflect any change to CI relationships in the CMDB CI Relationship \[cmdb\_rel\_ci\] table.

 To conform with Common Service Data Model, you can also convert legacy services to dynamic application services. Those legacy services are stored in the \[cmdb\_ci\_service\] or \[cmdb\_ci\_service\_manual\] CMDB tables:

-   [Convert business services to application services](../../service-mapping/concept/convert-bus-to-app-svc-intro.md#)
-   [Convert legacy manual services into dynamic application services](../task/convert-manual-app-ser-to-dynamic.md)

</td><td>

Use this method to transform legacy business services into application services that other ServiceNow products can utilize. For example, dynamic application services can be used for service monitoring and change management.

</td><td>

You can't edit a dynamic application service by adding or removing CIs from it. The system automatically modifies an application service of the dynamic type when you modify relevant relationships for CIs that are part of that application service.

</td></tr><tr><td>

[From CSV file](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/import-business-services-csv.md) Service Mapping extracts information from this file and creates potential application services referred to as service candidates. Use this method, if your organization has performed cross-organization mapping and analysis and collected some information about services.

</td><td>

If necessary, you can import service candidates from multiple CSV files.

</td><td>

Organize all the collected information in a specific order in a CSV file, precisely as described in the documentation.

</td></tr></tbody>
</table>To comply with CSDM, convert manual services created using IT Operations Management Event Management and stored in \[cmdb\_ci\_service\_manual\] as covered in [Convert manual services to application services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/migrate-manual-2-application-service.md) or [Convert manual services to application services using API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/convert-manual-to-application-service.md). Converted services become application services of the manual type stored in the Mapped Application Service \[cmdb\_ci\_service\_discovered\] table.

## Domain separation

Domain separation, if deployed, impacts an service instance as follows:

-   When creating an service instance, the service instance is assigned to the user's domain.
-   When manually adding a CI to an service instance, you can choose only CIs that belong to the service domain.
-   When using the [createOrUpdateService - POST](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/rest-apis/application-service-api.md) REST API for creating or updating an application service, the process stops if one of the CIs referenced in the API belongs to a different domain than the application service itself.
-   When converting business services into application services, the newly created application service belongs to the same domain as the original business service. The application service comprises only CIs belonging to the same domain as the application service itself.

