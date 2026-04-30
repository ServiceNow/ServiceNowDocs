---
title: GCP discovery solutions comparison
description: ITOM Visibility applications discover a variety of Google Cloud Platform \(GCP\) resources and populate the relevant configuration item \(CI\) classes in the Configuration Management Database \(CMDB\) with their attributes.
locale: en-US
release: xanadu
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
keywords: [Patterns, Azure, Cloud, Discovery, Visibility, CMDB]
breadcrumb: [Reference, GCP, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# GCP discovery solutions comparison

ITOM Visibility applications discover a variety of Google Cloud Platform \(GCP\) resources and populate the relevant configuration item \(CI\) classes in the Configuration Management Database \(CMDB\) with their attributes.

## ITOM Visibility solutions

ITOM Visibility can offer you comprehensive visibility into your organization's cloud infrastructure. Each application offers unique strengths and capabilities, and by comparing them you can gain holistic insights on their capabilities and benefits.

<table id="table_sld_tvh_hfc"><thead><tr><th>

ITOM Visibility solution

</th><th>

Overview

</th><th>

Configuration

</th></tr></thead><tbody><tr><td>

Discovery and Service Mapping Patterns and Visibility Content

</td><td>

[Discovery patterns used by ITOM Visibility](https://www.servicenow.com/docs/access?context=c_MappingPatternsCustomization&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)

</td><td>

-   You must update your store apps to the latest release version.
-   You must provide ITOM Visibility with access permissions. For more information, see [Set up Google Cloud Platform service accounts](https://www.servicenow.com/docs/access?context=set-up-gcp-service-accounts&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)

</td></tr><tr><td>

Service Graph Connector for GCP

</td><td>

[Service Graph Connector for GCP](../../configuration-management/concept/sgc-cmdb-integration-gcp.md)

</td><td>

[Configure Service Graph Connector for GCP using the guided setup](../../configuration-management/task/sgc-config-gcp-integration.md)

</td></tr></tbody>
</table>**Note:**

The CI class, in most cases, is applicable to both solutions. If it's not applicable to one of the solutions, the solution is marked "N/A".

If an entry is marked with one asterisk, the resource type is supported by Patterns only by utilizing the **Google Asset inventory** pattern's inclusion list. For more information, see [Google Cloud Platform \(GCP\) resource inventory discovery](https://www.servicenow.com/docs/access?context=gcp-resource-inventory-discovery&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US).

If an entry is marked with two asterisks, the resource type is supported by Service Graph Connecters only by utilizing the \[sn\_cmdb\_int\_util\_service\_graph\_resource\_inclusion\_whitelist\] table.

|Resource type|Supported by Cloud Discovery and Service Mapping Patterns|Supported by Cloud Service Graph Connectors|CI Class|
|-------------|---------------------------------------------------------|-------------------------------------------|--------|
|admissionregistration.k8s.io/mutatingwebhookconfiguration|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|
|admissionregistration.k8s.io/validatingwebhookconfiguration|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|
|alloydb.googleapis.com/Cluster|Yes|No|cmdb\_ci\_cloud\_db\_cluster|
|apigateway.googleapis.com/api|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|
|apigateway.googleapis.com/apiconfig|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|
|apigee.googleapis.com/instance|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|
|apigee.googleapis.com/organization|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|
|apikeys.googleapis.com/key|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|
|appengine.googleapis.com/application|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|
|apps.k8s.io/daemonset|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|
|apps.k8s.io/Deployment|Yes\*|Yes|cmdb\_ci\_kubernetes\_deployment|
|apps.k8s.io/ReplicaSet|Yes\*|Yes|cmdb\_ci\_kubernetes\_replicaset|
|apps.k8s.io/statefulset|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|
|artifactregistry.googleapis.com/dockerimage|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|
|artifactregistry.googleapis.com/repository|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|
|bigquery.googleapis.com/bigquery-public-data/datasets|Yes|No|cmdb\_ci\_cloud\_public\_database|
|bigquery.googleapis.com/bigquery-public-data/datasets/tables|Yes|No|cmdb\_ci\_database|
|bigquery.googleapis.com/Dataset|Yes|N/A|cmdb\_ci\_cloud\_database|
|bigquery.googleapis.com/Dataset|N/A|Yes\*\*|cmdb\_ci\_cmp\_resource|
|bigquery.googleapis.com/Table|Yes|No|cmdb\_ci\_database|
|bigtableadmin.googleapis.com/Instance|Yes|Yes|cmdb\_ci\_cloud\_database|
|bigtableadmin.googleapis.com/Table|Yes|No|cmdb\_ci\_database|
|cloudasset.googleapis.com/feed|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|
|cloudbilling.googleapis.com/billingaccount|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|
|cloudbilling.googleapis.com/projectbillinginfo|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|
|cloudfunctions.googleapis.com/CloudFunction|Yes\*|Yes|cmdb\_ci\_cloud\_function|
|cloudresourcemanager.googleapis.com/Folder|Yes|Yes|cmdb\_ci\_gcp\_folder|
|cloudresourcemanager.googleapis.com/Organization|Yes|Yes|cmdb\_ci\_cloud\_org|
|cloudresourcemanager.googleapis.com/Project|Yes|Yes|cmdb\_ci\_gcp\_project|
|cloudresourcemanager.googleapis.com/tagkey|Yes\*|Yes|cmdb\_ci\_cmp\_resource|
|cloudresourcemanager.googleapis.com/tagvalue|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|
|compute.googleapis.com/Address|Yes|No|cmdb\_ci\_cloud\_public\_ipaddress|
|compute.googleapis.com/autoscaler|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|
|compute.googleapis.com/BackendService|N/A|Yes|cmdb\_ci\_cloud\_load\_balancer|
|compute.googleapis.com/BackendService|Yes|N/A|cmdb\_ci\_lb\_service|
|compute.googleapis.com/Disk|Yes|Yes|cmdb\_ci\_storage\_volume|
|compute.googleapis.com/DiskTypes|Yes|No|cmdb\_ci\_disk\_type|
|compute.googleapis.com/Firewall|N/A|Yes|cmdb\_ci\_compute\_security\_group|
|compute.googleapis.com/Firewall|Yes|Yes|cmdb\_ci\_network\_acl\_rule|
|compute.googleapis.com/ForwardingRule|Yes|Yes|cmdb\_ci\_lb\_service|
|compute.googleapis.com/HttpHealthCheck|Yes|Yes|cmdb\_ci\_lb\_health\_service|
|compute.googleapis.com/Image|Yes|No|cmdb\_ci\_os\_template|
|compute.googleapis.com/Instance|Yes|N,A|cmdb\_ci\_lb\_pool\_member|
|compute.googleapis.com/Instance|N/A|Yes|cmdb\_ci\_server|
|compute.googleapis.com/Instance|Yes|Yes|cmdb\_ci\_vm\_instance|
|compute.googleapis.com/Instance/networkInterfaces|Yes|No|cmdb\_ci\_endpoint\_vnic|
|compute.googleapis.com/Instance/networkInterfaces|Yes|Yes|cmdb\_ci\_nic|
|compute.googleapis.com/InstanceGroup|Yes|N/A|cmdb\_ci\_lb\_pool|
|compute.googleapis.com/InstanceGroup|N/A|Yes\*\*|cmdb\_ci\_cmp\_resource|
|compute.googleapis.com/Instancegroupmanager|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|
|compute.googleapis.com/Instancesettings|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|
|compute.googleapis.com/InstanceTemplate|Yes|No|cmdb\_ci\_instance\_template|
|compute.googleapis.com/Instancetemplate|No|Yes\*\*|cmdb\_ci\_cmp\_resource|
|compute.googleapis.com/MachineImage|No|Yes|cmdb\_ci\_os\_template|
|compute.googleapis.com/MachineTypes|Yes|No|cmdb\_ci\_cloud\_hardware\_type|
|compute.googleapis.com/MachineTypes|Yes|No|cmdb\_ci\_compute\_template|
|compute.googleapis.com/Network|Yes|Yes|cmdb\_ci\_network|
|compute.googleapis.com/Networkendpointgroup|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|
|compute.googleapis.com/Regions|Yes|No|cmdb\_ci\_google\_datacenter|
|compute.googleapis.com/resourcepolicy|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|
|compute.googleapis.com/router|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|
|compute.googleapis.com/Snapshot|Yes|Yes|cmdb\_ci\_storage\_vol\_snapshot|
|compute.googleapis.com/ssh|Yes|No|cmdb\_ci\_cloud\_key\_pair|
|compute.googleapis.com/sslcertificate|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|
|compute.googleapis.com/Subnetwork|Yes|Yes|cmdb\_ci\_cloud\_subnet|
|compute.googleapis.com/targetHttpProxy|Yes|N/A|cmdb\_ci\_lb\_service|
|compute.googleapis.com/targetHttpProxy|Yes|Yes\*\*|cmdb\_ci\_cmp\_resource|
|compute.googleapis.com/TargetPool|Yes|N/A|cmdb\_ci\_cloud\_load\_balancer|
|compute.googleapis.com/TargetPool|N/A|Yes|cmdb\_ci\_lb\_pool|
|compute.googleapis.com/targetSslProxy|Yes|No|cmdb\_ci\_lb\_service|
|compute.googleapis.com/targetTcpProxy|Yes|No|cmdb\_ci\_lb\_service|
|compute.googleapis.com/UrlMap|Yes|N/A|cmdb\_ci\_cloud\_load\_balancer|
|compute.googleapis.com/UrlMap|N/A|Yes\*\*|cmdb\_ci\_cmp\_resource|
|compute.googleapis.com/zones|Yes|No|cmdb\_ci\_availability\_zone|
|container.googleapis.com/Cluster|Yes|Yes|cmdb\_ci\_kubernetes\_cluster|
|container.googleapis.com/NodePool|No|Yes|cmdb\_ci\_kubernetes\_node\_pool|
|containerregistry.googleapis.com/image|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|
|dataplex.googleapis.com/entrygroup|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|
|firebase.googleapis.com/firebaseproject|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|
|firebasedatabase.googleapis.com/instances|Yes|No|cmdb\_ci\_cloud\_database|
|firebaserules.googleapis.com/release|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|
|firebaserules.googleapis.com/ruleset|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|
|firestore.googleapis.com/Database|Yes|Yes|cmdb\_ci\_cloud\_database|
|iam.googleapis.com/role|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|
|iam.googleapis.com/serviceaccount|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|
|iam.googleapis.com/serviceaccountkey|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|
|integrations.googleapis.com/integration|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|
|integrations.googleapis.com/integrationversion|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|
|K8s.io/endpoints|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|
|K8s.io/Namespace|Yes\*|Yes|cmdb\_ci\_kubernetes\_namespace|
|k8s.io/Node|Yes\*|Yes|cmdb\_ci\_kubernetes\_node|
|K8s.io/persistentvolume|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|
|k8s.io/persistentvolumeclaim|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|
|K8s.io/Pod|Yes\*|Yes|cmdb\_ci\_docker\_container|
|K8s.io/Pod|N/A|Yes|cmdb\_ci\_docker\_image|
|K8s.io/Pod|N/A|Yes|cmdb\_ci\_kubernetes\_pod|
|K8s.io/Pod|N/A|Yes|cmdb\_ci\_kubernetes\_volume|
|K8s.io/resourcequota|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|
|k8s.io/Service|Yes\*|Yes|cmdb\_ci\_kubernetes\_service|
|K8s.io/serviceaccount|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|
|labels|Yes|No|cmdb\_key\_value|
|logging.googleapis.com/logbucket|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|
|logging.googleapis.com/logmetric|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|
|logging.googleapis.com/logsink|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|
|logging.googleapis.com/recentquery|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|
|memcache.googleapis.com/Instance|Yes\*|Yes|cmdb\_ci\_cloud\_database|
|monitoring.googleapis.com/alertpolicy|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|
|monitoring.googleapis.com/dashboard|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|
|monitoring.googleapis.com/notificationchannel|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|
|networkmanagement.googleapis.com/connectivitytest|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|
|orgpolicy.googleapis.com/policy|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|
|policy.k8s.io/poddisruptionbudget|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|
|pubsub.googleapis.com/subscription|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|
|pubsub.googleapis.com/topic|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|
|rbac.authorization.k8s.io/ClusterRole|No|Yes|cmdb\_ci\_kubernetes\_cluster\_role|
|rbac.authorization.k8s.io/ClusterRoleBinding|No|Yes|cmdb\_ci\_kubernetes\_cluster\_role\_binding|
|rbac.authorization.k8s.io/role|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|
|rbac.authorization.k8s.io/rolebinding|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|
|redis.googleapis.com/clusters|Yes|No|cmdb\_ci\_cloud\_db\_cluster|
|redis.googleapis.com/Instance|No|Yes|cmdb\_ci\_cloud\_database|
|run.googleapis.com/revision|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|
|run.googleapis.com/service|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|
|servicedirectory.googleapis.com/endpoint|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|
|servicedirectory.googleapis.com/namespace|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|
|servicedirectory.googleapis.com/service|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|
|servicemanagement.googleapis.com/managedservice|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|
|servicenetworking.googleapis.com/connection|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|
|serviceusage.googleapis.com/service|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|
|spanner.googleapis.com/Database|Yes|No|cmdb\_ci\_database|
|spanner.googleapis.com/Instance|Yes|Yes|cmdb\_ci\_cloud\_database|
|sqladmin.googleapis.com/backup|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|
|sqladmin.googleapis.com/backuprun|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|
|sqladmin.googleapis.com/Instance|Yes\*|Yes|cmdb\_ci\_cloud\_database|
|sqladmin.googleapis.com/Instances/databases|Yes\*|No|cmdb\_ci\_database|
|storage.googleapis.com/Bucket|N/A|Yes|cmdb\_ci\_cloud\_object\_storage|
|storage.googleapis.com/Bucket|Yes|N/A|cmdb\_ci\_cmp\_resource|
|storage.k8s.io/storageclass|Yes\*|Yes\*\*|cmdb\_ci\_cmp\_resource|

\* These resource types are supported in Patterns only by utilizing the **Google Asset inventory** pattern's inclusion list. For more information, see [Google Cloud Platform \(GCP\) resource inventory discovery](https://www.servicenow.com/docs/access?context=gcp-resource-inventory-discovery&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US).

\*\* These resource types are supported in Service Graph Connecters only by utilizing the \[sn\_cmdb\_int\_util\_service\_graph\_resource\_inclusion\_whitelist\] table.

**Parent Topic:**[Service Graph Connector for GCP reference](../../configuration-management/concept/sgc-cmdb-gcp-reference.md)

