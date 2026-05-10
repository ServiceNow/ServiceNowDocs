---
title: Tag-based discovery in Service Mapping
description: If your organization uses tags, or establishes them in a local ServiceNow instance, you can use these tags to map application services.
locale: en-US
release: australia
product: Service Mapping
classification: service-mapping
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Choose method for discovering and mapping services, Exploring Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Tag-based discovery in Service Mapping

If your organization uses tags, or establishes them in a local ServiceNow instance, you can use these tags to map application services.

A tag is a label that consists of a key-value pair. Your organization might use tags to categorize its assets and to enhance query and reporting capabilities. Discovery and Cloud Provisioning and Governance can discover tags used by all major cloud providers and container ecosystems. Once the tags are discovered, Service Mapping can create application services based on these tags. Typically organizations use tagging in virtualized, hyper-converged, or multi-cloud infrastructures.

|Segment|Technology providers|What is tagged|
|-------|--------------------|--------------|
|Cloud|Amazon Web Services \(AWS\), Azure, Google Cloud Platform \(GCP\), IBM Cloud Platform|IaaS, PaaS, FaaS, CaaS resources|
|Hyper-converged|Nutanix|Virtual machines|
|Containers|Kubernetes, OpenShift Container Platform, AWS ECS|Containers|
|Virtualization|VMware vCenter|Virtual machines|

Unlike other mapping methods, tag-based mapping does not require configuring credentials or providing users with elevated rights. You can effectively use tags to map multiple service instances.

## Tag-based discovery stages

The tag-based discovery and mapping process consists of the following stages:

1.  Discovery and Cloud Provisioning and Governance discover tags for cloud and resource configuration items \(CIs\) and then populate data for discovered tags into the Key Value \[cmdb\_key\_value\] table.
2.  The administrator creates CI tag categories and defines tag keys that the categories contain. Tag categories contain tags with similar use. For example, if your organization has production and staging environments, you could create "production" and "staging" tag values.
3.  The administrator creates a tag-based service family and selects tag categories to use for its mapping. CIs that have more than one tags assigned to them, can be part of multiple services.

    -   Only CIs with discovered tag keys for the selected tag categories become part of application services.
    -   The administrator can narrow the criteria by defining specific tag values in addition to tag categories.
    -   Service Mapping uses only CIs that have the matching values to create application services.
    -   CIs that have more than one tag assigned to them can be a part of multiple services.
    **Note:** When creating a service family for mapping services based on tags in domain-separated environment, you must pick the relevant leaf domain.

4.  Service Mapping queries the CMDB for CIs with tag values that match the tag definitions for this tag-based service family.
5.  Service Mapping creates service candidates based on the defined tags.

    Service Mapping populates tag-based services based on this service family only with CIs belonging to the leaf domain to which the service family belongs.

6.  The administrator selects the service candidates to map and starts the mapping process.
7.  Service Mapping adds new application services to the Tag-Based Application Service \[cmdb\_ci\_service\_by\_tags\] table.

    **Important:** Service instances mapped using tags might not include relevant CIs if those CIs do not have the correct tags.

8.  Service Mapping maps application services by creating connections between tagged CIs based on CI relationships. The Traversal Rules for Application Services \[svc\_traversal\_rules\] table contains information used for creating tag-based application services.

    **Note:** Service Mapping includes CIs that are part of these relationships even if these CIs do not have tags assigned to them.


## Creating tag-based services

You can create single tag-based application services using the Common Service Data Model \(CSDM\) flow as described in [populate application services using tags](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/populate-app-service-tags.md).

For information about how to create multiple tag-based services, see [Map application services using tags with classic Service Mapping](../task/map-service-tag.md).

**Related topics**  


[Tag-based discovery configuration](tag_discovery_configuration.md)

[Tag Governance](../../it-operations-management/reference/landing-page-tag-governance.md)

