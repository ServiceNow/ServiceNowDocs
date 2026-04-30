---
title: CMDB classes targeted in Service Graph Connector for OpenTelemetry
description: When you complete setting up the connection, you can configure the integration to periodically pull data from ServiceNow Cloud Observability \(formerly Lightstep\). The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.
locale: en-US
release: xanadu
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2026-02-27"
reading_time_minutes: 4
breadcrumb: [OpenTelemetry, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB classes targeted in Service Graph Connector for OpenTelemetry

When you complete setting up the connection, you can configure the integration to periodically pull data from ServiceNow Cloud Observability \(formerly Lightstep\). The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.

**Important:** Starting with the Australia release, Service Graph Connector for OpenTelemetry is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

## Calculated Application Service \[cmdb\_ci\_service\_calculated\]

The following attributes in the Calculated Application Service \[cmdb\_ci\_service\_calculated\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Service Populator|service\_populator|
|Name|name|
|Hide from dashboard|hide\_from\_dashboard|
|Operational status|operational\_status|
|Service Populator Status|populator\_status|
|Service Type|type|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Calculated Application Service \[cmdb\_ci\_service\_calculated\]|Connects to::Connected by|Kubernetes Deployment \[cmdb\_ci\_kubernetes\_deployment\]|
|Calculated Application Service \[cmdb\_ci\_service\_calculated\]|Connects to::Connected by|Calculated Application Service \[cmdb\_ci\_service\_calculated\]|
|Calculated Application Service \[cmdb\_ci\_service\_calculated\]|Reference|Key Value \[cmdb\_key\_value\]|

## Docker Container \[cmdb\_ci\_docker\_container\]

The following attributes in the Docker Container \[cmdb\_ci\_docker\_container\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Container id|container\_id|
|Install Status|install\_status|
|Name|name|

## Docker Image \[cmdb\_ci\_docker\_image\]

The following attributes in the Docker Image \[cmdb\_ci\_docker\_image\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Image id|image\_id|
|Install Status|install\_status|
|Name|name|

## Key Value \[cmdb\_key\_value\]

The following attributes in the Key Value \[cmdb\_key\_value\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Key|key|
|Value|value|

## Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]

The following attributes in the Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Namespace|namespace|
|Install Status|install\_status|
|Kubernetes UID|k8s\_uid|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|Cluster of::Cluster|Kubernetes Node \[cmdb\_ci\_kubernetes\_node\]|
|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|Contains::Contained by|Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]|
|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|Contains::Contained by|Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\]|
|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|Contains::Contained by|Kubernetes Service \[cmdb\_ci\_kubernetes\_service\]|

## Kubernetes Cronjob \[cmdb\_ci\_kubernetes\_cronjob\]

The following attributes in the Kubernetes Cronjob \[cmdb\_ci\_kubernetes\_cronjob\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Kubernetes Cluster|cluster|
|Name|name|
|Namespace|namespace|
|Install Status|install\_status|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Kubernetes Cronjob \[cmdb\_ci\_kubernetes\_cronjob\]|Hosted on::Hosts|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|
|Kubernetes Cronjob \[cmdb\_ci\_kubernetes\_cronjob\]|Reference|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|

## Kubernetes DaemonSet \[cmdb\_ci\_kubernetes\_daemonset\]

The following attributes in the Kubernetes DaemonSet \[cmdb\_ci\_kubernetes\_daemonset\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Kubernetes Cluster|cluster|
|Name|name|
|Namespace|namespace|
|Install Status|install\_status|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Kubernetes DaemonSet \[cmdb\_ci\_kubernetes\_daemonset\]|Hosted on::Hosts|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|
|Kubernetes DaemonSet \[cmdb\_ci\_kubernetes\_daemonset\]|Reference|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|

## Kubernetes Deployment \[cmdb\_ci\_kubernetes\_deployment\]

The following attributes in the Kubernetes Deployment \[cmdb\_ci\_kubernetes\_deployment\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Kubernetes Cluster|cluster|
|Name|name|
|Namespace|namespace|
|Install Status|install\_status|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Kubernetes Deployment \[cmdb\_ci\_kubernetes\_deployment\]|Hosted on::Hosts|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|
|Kubernetes Deployment \[cmdb\_ci\_kubernetes\_deployment\]|Connects to::Connected by|Kubernetes Node \[cmdb\_ci\_kubernetes\_node\]|
|Kubernetes Deployment \[cmdb\_ci\_kubernetes\_deployment\]|Connects to::Connected by|Kubernetes ReplicaSet \[cmdb\_ci\_kubernetes\_replicaset\]|
|Kubernetes Deployment \[cmdb\_ci\_kubernetes\_deployment\]|Reference|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|

## Kubernetes Job \[cmdb\_ci\_kubernetes\_job\]

The following attributes in the Kubernetes Job \[cmdb\_ci\_kubernetes\_job\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Kubernetes Cluster|cluster|
|Kubernetes UID|k8s\_uid|
|Name|name|
|Namespace|namespace|
|Install Status|install\_status|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Kubernetes Job \[cmdb\_ci\_kubernetes\_job\]|Hosted on::Hosts|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|
|Kubernetes Job \[cmdb\_ci\_kubernetes\_job\]|Reference|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|

## Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\]

The following attributes in the Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Kubernetes Cluster|cluster|
|Name|name|
|Install Status|install\_status|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\]|Reference|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|

## Kubernetes Node \[cmdb\_ci\_kubernetes\_node\]

The following attributes in the Kubernetes Node \[cmdb\_ci\_kubernetes\_node\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Kubernetes UID|k8s\_uid|
|Name|name|
|Install Status|install\_status|
|Namespace|namespace|
|Kubernetes Cluster|cluster|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Kubernetes Node \[cmdb\_ci\_kubernetes\_node\]|Hosted on::Hosts|Server \[cmdb\_ci\_server\]|
|Kubernetes Node \[cmdb\_ci\_kubernetes\_node\]|Reference|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|

## Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]

The following attributes in the Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Install Status|install\_status|
|Kubernetes Cluster|cluster|
|Kubernetes UID|k8s\_uid|
|Namespace|namespace|
|IP Address|ip\_address|
|Start date|start\_date|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]|Contains::Contained by|Docker Image \[cmdb\_ci\_docker\_image\]|
|Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]|Contains::Contained by|Docker Container \[cmdb\_ci\_docker\_container\]|
|Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]|Reference|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|

## Kubernetes ReplicaSet \[cmdb\_ci\_kubernetes\_replicaset\]

The following attributes in the Kubernetes ReplicaSet \[cmdb\_ci\_kubernetes\_replicaset\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Kubernetes UID|k8s\_uid|
|Name|name|
|Namespace|namespace|
|Install Status|install\_status|
|Kubernetes Cluster|cluster|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Kubernetes ReplicaSet \[cmdb\_ci\_kubernetes\_replicaset\]|Hosted on::Hosts|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|
|Kubernetes ReplicaSet \[cmdb\_ci\_kubernetes\_replicaset\]|Connects to::Connected by|Kubernetes Node \[cmdb\_ci\_kubernetes\_node\]|
|Kubernetes ReplicaSet \[cmdb\_ci\_kubernetes\_replicaset\]|Reference|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|

## Kubernetes Service \[cmdb\_ci\_kubernetes\_service\]

The following attributes in the Kubernetes Service \[cmdb\_ci\_kubernetes\_service\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Namespace|namespace|
|Install Status|install\_status|

## Kubernetes StatefulSet \[cmdb\_ci\_kubernetes\_statefulset\]

The following attributes in the Kubernetes StatefulSet \[cmdb\_ci\_kubernetes\_statefulset\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Kubernetes Cluster|cluster|
|Namespace|namespace|
|Install Status|install\_status|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Kubernetes StatefulSet \[cmdb\_ci\_kubernetes\_statefulset\]|Hosted on::Hosts|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|
|Kubernetes StatefulSet \[cmdb\_ci\_kubernetes\_statefulset\]|Reference|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|

## Server \[cmdb\_ci\_server\]

The following attribute in the Server \[cmdb\_ci\_server\] table is populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|

**Related topics**  


[Kubernetes extension classes](../concept/cmdb-ci-class-models-kubernetes.md)

[CI relationships in the CMDB](../concept/c_CIRelationships.md)

