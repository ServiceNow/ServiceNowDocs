---
title: Choosing migration strategy
description: After you reviewed the current IT infrastructure and reviewed the IT needs of your organization, consider the migration method and target architecture.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Planning the migration process, Using Cloud Migration Assessment in Configurable Workspace, Cloud Migration Assessment, ITOM Cloud Accelerate, IT Operations Management]
---

# Choosing migration strategy

After you reviewed the current IT infrastructure and reviewed the IT needs of your organization, consider the migration method and target architecture.

-   Choose the type of migration for different resources:
    -   **Rehosting — "Lift-and-shift"**

        You rehost your application using a different hardware environment without changing the application architecture. Typically, this strategy suits large legacy applications, or scenarios where the migration must be done quickly and effectively.

    -   **Replatforming — “Lift-tinker-and-shift"**

        You keep the original architecture of the application, while making just a few optimizations to enjoy the benefits of the cloud infrastructure. Re-platforming may take longer than rehosting, but it is perfect for cases where you must have a degree of cost-effectiveness, functionality and time-savings without the significant resource requirements of refactoring.

    -   **Retiring**

        You stop using some appliances or products in your current infrastructure. For example, you may decide not to migrate aging servers or applications with few users.

    -   **Retaining — "Revisit"**

        Migration strategy decisions take a lot of consideration and research. In some cases, you may want to put it on hold and revisit the most crucial or problematic aspects of your infrastructure later.

    -   **Refactoring — "Rearchitecturing"**

        You review and redesign the architecture of the current infrastructure to leverage cloud features and flexibility. Refactor your infrastructure or its components to achieve scale, performance or agility that the application cannot meet with its existing architecture. This strategy may be the most expensive, but it may also be the perfect solution, especially if you are moving towards a service-oriented infrastructure.

    -   **Repurchasing — "Drop and shop"**

        You switch from your current application into a service or appliance that the cloud provider offers. In some cases, it is easier and more profitable to start using a new cloud product rather than investing into migrating an old one. If your organization has some home-grown products or an industry specific application not suitable for cloud infrastructures.

-   Depending on the needs of your organization, you may move all your IT resources onto the same cloud platform or use multiple platforms. Decide on the target architecture for different resources:
    -   **IaaS**

        Infrastructure-as-a-Service provides only a basic infrastructure containing virtual machines \(VMs\), software defined network \(SDN\), and network-attached storage \(NAS\).

    -   **SaaS**

        Software-as-a-Service, also referred to as on-demand software. Cloud providers manage applications and deliver applications to the customers using a web browser.

    -   **PaaS**

        Platform-as-a-Service provides a platform that customers use to deploy and run their applications without having to manage the infrastructure.

    -   **Hybrid**

        In a hybrid solution, the IT infrastructure is located on a public cloud, while still supporting and running some resources on-premise and private cloud workloads.

    -   **Container**

        Container as a Service is a container-based virtualization. Cloud providers use to this type to deliver container-related components to the customers: Container engines, orchestration and the underlying compute resources.

-   Establish your goals and decide on the time frame. Migration waves in Cloud Migration Assessment use fiscal quarters.
-   Identify groups of people and individuals who will be directly responsible for certain migration tasks and who will need to be notified inside your organization and on the side of the cloud provider.

**Parent Topic:**[Planning the migration process](cloud-migration-planning.md)

**Previous topic:**[Review detailed application information in Configurable Workspace](../task/migration-review-application-info.md)

**Next topic:**[Create assessment tasks for cloud migration in Configurable Workspace](../task/create-assessment-task.md)

