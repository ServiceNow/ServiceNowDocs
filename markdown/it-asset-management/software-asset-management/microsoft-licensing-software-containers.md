---
title: Microsoft SQL Server licensing in container deployments
description: The Software Asset Management publisher pack for Microsoft supports licensing rules for Microsoft SQL Server products that are deployed across both on-premise and cloud environments using Docker containers.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Software Asset Management publisher pack for Microsoft, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Microsoft SQL Server licensing in container deployments

The Software Asset Management publisher pack for Microsoft supports licensing rules for Microsoft SQL Server products that are deployed across both on-premise and cloud environments using Docker containers.

Containers are executable software packages that bundle all the code and dependencies that are required for deploying and running a specific application. With a container, you can deploy and run the same application uniformly across any computing environment, such as a desktop computer or the cloud, without having to reconfigure the application. Each container also virtualizes an operating system \(OS\) so that you can quickly and easily deploy multiple isolated applications within the same computing environment.

The Software Asset Management application works in conjunction with the ServiceNow® Discovery application to identify the following information in both on-premise and cloud environments:

-   The Docker containers through which your Microsoft SQL Server products are deployed.
-   The corresponding Kubernetes clusters that enable each container to run.
-   The OS of the underlying physical server that the container is running on.
-   The Microsoft SQL Server version and edition that is deployed through each container.
-   The number of virtual processor cores that are assigned to each container.

The Software Asset Management application uses the resulting data to create corresponding software installation records for each of your discovered containers. You can then reconcile these container-based software installations to track and optimize the license compliance of the Microsoft SQL Server products that are deployed through each container.

For more visibility into the Microsoft SQL Server products that are deployed through your Docker containers, view the [Licensable Software Products Deployed on Containers report](../reference/microsoft-licensable-software-products-deployed-containers-report.md).

For more information on Docker discovery, see Docker virtualization. For more information on Kubernetes discovery, see Kubernetes discovery.

## Supported licensing models

The Microsoft publisher pack supports the following licensing models for Microsoft SQL Server products that are deployed through containers:

**Note:** For more information on each licensing model, refer to [Supported Microsoft license types](../reference/supported-microsoft-license-types.md).

<table id="table_pmq_j3c_tvb"><thead><tr><th>

Licensing Model

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Per core

</td><td>

You must license each container as a standalone device. Licensing is based on the number of virtual CPUs \(vCPUs\) that are discovered on each container, with a minimum of four per core licenses per container.

</td></tr><tr><td>

Server/CAL

</td><td>

You must license each container using a server \(per instance or per server\) license. You must also license each user or device that is accessing the underlying physical server running these containers using a user or device CAL license.

 Server licenses enable you to license container-based software installations on your physical servers. To license only a certain number of installations on a physical server, use a server \(per instance\) license. To license all installations on a physical server, use a server \(per server\) license.

 CAL licenses are client access licenses that grant a set number of users or devices access to the underlying physical server on which your containers are running.

-   To grant a set number of users access to a physical server, regardless of how many devices those users are accessing the server through, use a user CAL license.
-   To grant a set number of devices access to a physical server, regardless of how many users are accessing the server through those devices, use a device CAL license.

</td></tr></tbody>
</table>-   **[Licensable Software Products Deployed on Containers report](../reference/microsoft-licensable-software-products-deployed-containers-report.md)**  
You can use the Licensable Software Products Deployed on Containers report to gain visibility into the software products that are deployed across both on-premise and cloud environments using Docker containers.

**Parent Topic:**[Software Asset Management publisher pack for Microsoft](microsoft-publisher-pack.md)

