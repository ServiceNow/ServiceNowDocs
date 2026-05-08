---
title: Docker virtualization
description: Discovery uses the Docker Pattern to collect data about specific objects in a Docker engine, running on a Linux host.
locale: en-US
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [OS-level virtualization discovery, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# Docker virtualization

Discovery uses the **Docker Pattern** to collect data about specific objects in a Docker engine, running on a Linux host.

The ServiceNow® platform supports the discovery of [Docker](https://www.docker.com/) release 1.11.0 or later.

Discovery runs the Docker Engine process classifier in the network. If the classifier identifies the **dockerd** or **docker daemon** process, the classifier triggers the Horizontal Pattern \(HorizontalDiscoveryProbe\) probe, which launches the Docker Pattern and begins collecting data from Docker components.

**Note:** For information on Probe to Pattern migration see the knowledge article [KB0694477](https://support.servicenow.com/kb_view.do?sysparm_article=KB0694477).

## Prerequisites

-   **User privileges**

    The user whose credentials are used to perform Docker Discovery must have privileges defined by one of these methods:

    -   Provide a user with elevated rights for running commands, since the Docker daemon runs as the root user. The Docker pattern supports the use of privileged commands, such as **sudo** or **pbrun**, to run as the root user.
    -   Assigned to a group named **docker**, which has special privileges for running Docker commands. For instructions on setting up a group, see documentation on [Docker](https://www.docker.com/).
-   **Latest patterns**

    Deploy the latest Discovery and Service Mapping Patterns application from ServiceNow Store.


## Docker restrictions and considerations

When using Docker virtualization, consider the following:

-   The initial Discovery process scan can identify an application in a container and classify it correctly. However, subsequent probes launched to explore that application cannot see inside the container and cannot return details about the application.
-   Discovery scans all containers it finds, including inactive containers, which can slow down Discovery. You should delete containers that are not running.
-   Before setting *sn\_itom\_pattern.manifest\_digest\_image\_id* property to **true** and running discovery: prevent duplicate Docker records from being created by deleting all Docker image records.
-   Only one Docker engine is permitted per computer \(on either a physical or virtual machine\).

## Data collected by Discovery during horizontal discovery

These attributes are discovered, in addition to the attributes derived from the parent OSLV tables.

<table id="table_okd_kb2_5w"><thead><tr><th>

Table and fields

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

Docker Engine \[cmdb\_ci\_docker\_engine\]

</td></tr><tr><td>

Name \[name\]

</td><td rowspan="11">

Stores information about instances of the Docker engine.

</td></tr><tr><td>

OS Arch \[os\_arch\]

</td></tr><tr><td>

GIT Commit \[git\_commit\]

</td></tr><tr><td>

Build Date \[build\_date\]

</td></tr><tr><td>

Version \[version\]

</td></tr><tr><td>

API Version \[api\_version\]

</td></tr><tr><td>

Go Version \[go\_version\]

</td></tr><tr><td>

Is Clustered \[is\_clustered\]

</td></tr><tr><td>

Running Process \[running\_process\]

</td></tr><tr><td>

Running Process Command \[running\_process\_command\]

</td></tr><tr><td>

Running Process Key Parameters \[running\_process\_key\_parameters\]

</td></tr><tr><td colspan="2">

Docker Image \[cmdb\_ci\_docker\_image\]

</td></tr><tr><td>

Name \[name\]

</td><td rowspan="5">

Stores information on the globally unique representation of Docker images.

</td></tr><tr><td>

Image id \[image\_id\]

</td></tr><tr><td>

Image digest \[image\_digest\]

</td></tr><tr><td>

Size \(byte\) \[size\_byte\]

</td></tr><tr><td>

Image created \[Image\_created\_at\]

</td></tr><tr><td colspan="2">

Docker Local Image \[cmdb\_ci\_docker\_local\_image\]

</td></tr><tr><td>

Name \[name\]

</td><td rowspan="2">

Stores local instances of Docker images.

</td></tr><tr><td>

Image id \[image\_id\]

</td></tr><tr><td colspan="2">

Docker Image Tag \[cmdb\_ci\_docker\_image\_tag\]

</td></tr><tr><td>

Name \[name\]

</td><td rowspan="4">

Stores tags from local Docker images.

</td></tr><tr><td>

Image id \[image\_id\]

</td></tr><tr><td>

Repository \[repository\]

</td></tr><tr><td>

Tag \[tag\]

</td></tr><tr><td colspan="2">

Docker Container \[cmdb\_ci\_docker\_container\]

</td></tr><tr><td>

Name \[name\]

</td><td rowspan="7">

Stores Docker containers found on the host.In cases where duplicate records are created, deduplication tasks appear once discovery runs. For information on how to resolve these tasks, see the [Making docker container identifier independent \[KB1443042\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1443042) article in the ServiceNow® Knowledge Base.

</td></tr><tr><td>

Image id \[image\_id\]

</td></tr><tr><td>

Container id \[container\_id\]

</td></tr><tr><td>

Size \(bytes\) \[size\_bytes\]

</td></tr><tr><td>

Command \[command\]

</td></tr><tr><td>

Container created \[container\_created\]

</td></tr><tr><td>

Status \[status\]

</td></tr></tbody>
</table>The **Collect Container Repository** extension section discovers this information.

|Table and field|Description|
|---------------|-----------|
|Container Repository \[cmdb\_ci\_container\_repository\]|
|Name \[name\]|The name of the container repository.|
|Container Repository Entry \[cmdb\_ci\_container\_repository\_entry\]|
|Name \[name\]|The name of the container repository entry.|
|Category \[category\]|The category of the container repository entry.|

## CI relationships

The Docker Pattern identifies the following relationships between discovered CIs.

<table id="table_dqz_s5y_lrb"><thead><tr><th>

CI

</th><th>

Relation

</th><th>

CI

</th></tr></thead><tbody><tr><td>

cmdb\_ci\_server

</td><td>

Runs::Runs On

</td><td>

cmdb\_ci\_docker\_engine

</td></tr><tr><td>

cmdb\_ci\_docker\_engine

</td><td>

Manages::Managed By

</td><td>

cmdb\_ci\_docker\_container

</td></tr><tr><td>

cmdb\_ci\_docker\_engine

</td><td>

Manages::Managed By

</td><td>

cmdb\_ci\_docker\_local\_image

</td></tr><tr><td>

cmdb\_ci\_docker\_image

</td><td>

Instantiates::Instantiated By

</td><td>

cmdb\_ci\_docker\_container

</td></tr><tr><td>

cmdb\_ci\_docker\_local\_image

 **Note:** The direction of this relation is the opposite for all store versions earlier than 1.0.99, February 2023.

</td><td>

Instantiates::Instantiated By

</td><td>

cmdb\_ci\_docker\_container

</td></tr><tr><td>

cmdb\_ci\_docker\_image\_tag

</td><td>

Registered On::Has Registered

</td><td>

cmdb\_ci\_docker\_local\_image

</td></tr><tr><td>

cmdb\_ci\_docker\_local\_image

</td><td>

Instantiates::Instantiated By

</td><td>

cmdb\_ci\_docker\_image

</td></tr></tbody>
</table>The **Collect Container Repository** extension section of the Docker Pattern identifies these relationships.

|CI|Relationship|CI|
|---|------------|---|
|Docker Image \[cmdb\_ci\_docker\_image\]|Provisioned From::Provisioned|Container Repository Entry \[cmdb\_ci\_container\_repository\_entry\]|
|Container Repository Entry \[cmdb\_ci\_container\_repository\_entry\]|Hosted on::Hosts|Container Repository \[cmdb\_ci\_container\_repository\]|

## Identification, containment, and hosting rules

Discovery uses an application rule identifier to find the Docker engine and then applies other rules to identify specific Docker objects.

-   **Application rule identifier**

    The system creates the cmdb\_ci\_docker\_engine configuration item \(CI\) during process classification. Based on this, Discovery uses the Application Rule identifier on the Application \[cmdb\_ci\_appl\] table to identify the particular Docker engine encountered. After establishing this identity, Discovery uses the relationships defined in the containment and hosting rules to accurately create and update the individual Docker component CIs related to that engine.

-   **Identifiers**

    |Name|Table|Attributes|
    |----|-----|----------|
    |Docker Container|Docker Container \[cmdb\_ci\_docker\_container\]|container\_id|
    |Docker Global Image|Docker Image \[cmdb\_ci\_docker\_image\]|image\_id|
    |Docker Local Image|Docker Local Image \[cmdb\_ci\_docker\_local\_image\]|image\_id|
    |Docker Image Tag|Docker Image Tag \[cmdb\_ci\_docker\_image\_tag\]|repository, tag|

-   **Containment and hosting rules**

    Docker Discovery uses these Create or edit a collection of containment rules and Create or edit a collection of hosting rules rules to create configuration items \(CI\) from the data returned by the Docker Pattern. After Discovery identifies the Docker engine by its relationship to the Application \[cmdb\_ci\_appl\] table, it uses these rules to identify the specific CIs connected to that engine from their relationships to one another. By connecting the components to one another in this fashion, from the application down, starting with the engine, Discovery avoids creating duplicate CIs for components from other Docker engines that use the same name or image\_id.

    |Parent|Child|Relationship|
    |------|-----|------------|
    |Docker Local Image|Docker Image Tag|Has registered|

    |Parent|Child|Relationship|
    |------|-----|------------|
    |Docker Container|Docker Engine|Managed by|
    |Docker Local Image|Docker Engine|Managed by|


**Parent Topic:**[Operating system-level virtualization discovery](c-oslv-discovery.md)

