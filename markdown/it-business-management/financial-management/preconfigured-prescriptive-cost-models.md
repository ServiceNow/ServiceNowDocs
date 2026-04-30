---
title: Prescriptive cost models for shared services and business applications - Legacy
description: L1 Costing – Shared Services provides a complete visibility of fully loaded IT infrastructure cost, infrastructure shared services showback, and lays foundation for future growth. L2 Costing – Business Applications provides cost of applications and end user, aligns applications to business units, furnishes cost information to support each business unit in business terms.
locale: en-US
release: zurich
product: Financial Management
classification: financial-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 10
breadcrumb: [The Cost Models tab - Legacy, Financial Management workbench - Legacy, Financial Modeling - Legacy, Financial Management - Legacy, Project Portfolio Management, Strategic Portfolio Management]
---

# Prescriptive cost models for shared services and business applications - Legacy

L1 Costing – Shared Services provides a complete visibility of fully loaded IT infrastructure cost, infrastructure shared services showback, and lays foundation for future growth. L2 Costing – Business Applications provides cost of applications and end user, aligns applications to business units, furnishes cost information to support each business unit in business terms.

**Important:**

This feature is available only when you own an ITBM Analyst license.

## L1 Costing – Shared Services

The specifications of the L1 Costing – Shared Services are:

![L1 Costing – Shared Services](../image/L1-CostModel.png "L1 Costing – Shared Services")

-   The cost bucket layer is tied to the ITFM bucket table \[itfm\_bucket\] and the cost buckets are specific to a model.
-   IT shared service segment accounts \(the middle layer in this model\) are sourced from the IT shared service table \[itfm\_shared\_service\].
-   The business unit layer is tied to the platform business unit table \[business\_unit\].

## L2 Costing – Business Applications

![L2 Costing – Business Applications](../image/L2-CostModel.png "L2 Costing – Business Applications")

The specifications of the L2 Costing – Business Applications are almost the same as L1 Costing – Shared Services. However, there is an additional layer for applications. Enterprise Architecture \(formerly APM\) Business Application \[cmdb\_ci\_business\_app\] table is the source of accounts to the applications segment. Or, it can be Application \[cmdb\_ci\_appl\] table or other custom tables.

## Seeded IT Shared Services

-   **IT Shared Service: Equip End Users**

    IT Shared Service: Equip End Users is a cost collection container that holds any money spent on providing the end users with personal \(not shared\) devices, the software that runs on these devices, and the support associated with making and keeping those devices functioning. This container excludes major device upgrades, lease cycle turnover, and other replenishment-related costs, which are captured within the Facilitate Ongoing Change container.

-   **IT Shared Service: Facilitate Configuration Change**

    IT Shared Service: Facilitate Configuration Change is a cost collection container that holds money spent on supporting the ITSM Change, Release and Configuration Management processes. That is, any dollars spent on managing ongoing, daily, common, and ad-doc configuration changes. This includes activities like patching \(non-security related\), firmware updates, hardware/software configuration setting changes, installation, de-installation, and upgrade of hardware components, and general add, move, or change requests across the IT landscape. This container excludes major upgrades and changes across a large portion of the environment for which a project plan and/or funding would need to be secured.

-   **IT Shared Service: Facilitate Connectivity**

    IT Shared Service: Facilitate Connectivity is a cost collection container that holds any money spent on providing all device network connectivity to the company, its computing and/or knowledge assets, the hardware and software to do it, and the support associated with making \(and keeping\) the access up. This includes all personal and enterprise devices. This container excludes monitoring hardware, software, and personnel costs, which are captured in the Monitor the Environment container.

-   **IT Shared Service: Management and Overhead**

    IT Shared Service: Management and Overhead is a cost collection container that holds any money spent on IT executive compensation, as well as one-time charge items that apply to the existence of IT operations, compliance or audit costs, and otherwise uncategorised costs. This container excludes any costs captured or accounted for in any of the other IT process definitions.

-   **IT Shared Service: Monitor the Environment**

    IT Shared Service: Monitor the Environment is a cost collection container that holds the money spent on supporting the ITOM Event Management process; that is, any dollars spent on monitoring the entire IT landscape. This includes endpoint connectivity speeds, endpoint application performance testing, hardware/software/network/storage threshold checking, and fault and event correlation management tools used by operations management personnel. This container excludes security specific and/or cloud monitoring services mentioned in other process areas.

-   **IT Shared Service: Perform Upgrades/Maintenance**

    IT Shared Service: Perform Upgrades/Maintenance is a cost collection container that holds money spent supporting the ITSM Change, Release and Configuration Management processes. That is, all dollars spent on managing major upgrades, either project planned and/or specifically funded. This includes activities such as widespread OS upgrades; hardware replacement cycle activities; and internal or third-party business or IT management software package release updates across the IT landscape. This container excludes ongoing, daily, common, and ad-doc configuration changes that only require a change ticket to be executed.

-   **IT Shared Service: Provide Tech Support**

    IT Shared Service: Provide Tech Support is a cost collection container that holds money spent supporting the ITSM Incident, Problem and Knowledge Management processes. That is, any dollars spent on providing technical support services to end users across the organization. This includes tier 1, 2, and 3 personnel, incident or problem management software, root cause analysis time, routine or ad-doc assistance \(password resets, how to Q&amp;A\), and/or standard operating procedure guidance. This container excludes actual configuration changes to end user and/or corporate assets performed by way of documented change tickets.

-   **IT Shared Service: Run Business Applications**

    IT Shared Service: Run Business Applications is a cost collection container that holds any dollars spent on ongoing personnel time to keep business applications operating. This includes resources dedicated to applications and excludes IT or infrastructure operation costs.

-   **IT Shared Service: Secure the Environment**

    IT Shared Service: Secure the Environment is a cost collection container that holds money spent on supporting the Security Operations. That is, any dollars spent on providing information security across the corporate IT landscape. This includes individual user endpoint devices, cloud applications, cloud computing, and/or on-premise computing resource of all types in addition to all desktops, laptops, smart phones, network gear, servers, databases, and applications. This excludes the physical security costs associated with datacenters, and office space card readers.

-   **IT Shared Service: Store and Manage Data**

    IT Shared Service: Store and Manage Data is a cost collection container that holds any dollars spent on the underlying tools and foundational activities related to the management of structured and unstructured data \(for example, encryption, backups, purging, archiving, migrations, and DR replication\) and/or storage capacity \(for example, reorganizations and excess capacity acquisition\). It includes these types of activities and all the people power used to ensure the health of the data and storage landscape. This container excludes elements related to local storage on end user devices utilized by single individuals and specific activities, and allocated storage that can be related to specific applications or systems.

-   **IT Shared Service: Supply Computing Power**

    IT Shared Service: Supply Computing Power is a cost collection container that holds any dollars spent on providing foundational elements that exist, cost money to maintain, but may never actually be used such as disaster recovery facilities or contracts, hardware spares inventory, on-premises UPS systems, and generators. It also includes daily active data center costs related to things such as space, power, and cooling.


## ITFM prescribed metrics

-   **Allocate to Business Unit based on Change Request volume based on CIs**

    The metric allocates shared service cost to business unit based on the following weighting table:

    ![Allocate to Business Unit based on Change Request volume based on CIs](../image/PrescribedMetric1.png "Allocate to Business Unit based on Change Request volume based on CIs")

    -   The Change Request \[change\_request\] table provides a list of all change requests and their related configuration item.
    -   The CMDB \[CMDB\_ci\] provides a list of all configuration items and their related department.
    -   The Department \[cmn\_department\] table provides a list of all departments and their business unit.
    -   The prescribed metric performs a count of change requests \(for CIs\) per business unit and weights the costs accordingly. Count number of CRs related to things requested by BUs \(does not align with the allocations matrix\) for the relevant fiscal period.

        The weight table enforces lifespan on this metric.

        -   Duration start: Actual start.
        -   Duration end: Actual end.
-   **Allocate to Business Unit based on CI Count**

    The metric allocates shared service cost to business unit based on the following weighting table:

    ![Allocate to Business Unit based on CI Count](../image/PrescribedMetric2.png "Allocate to Business Unit based on CI Count")

    -   The CMDB \[CMDB\_ci\] provides a list of all configuration items and their related department.
    -   The Department \[cmn\_department\] table provides a list of all departments and their related business unit.
    -   The prescribed metric performs a count of configuration items per business unit and weights the costs accordingly.
-   **Allocate to Business Unit on Headcount**

    The metric allocates shared service cost to business unit based on the following weighting table:

    ![Allocate to Business Unit on Headcount](../image/PrescribedMetric3.png "Allocate to Business Unit on Headcount")

    -   The User \[sys\_user\] table provides a list of all system users and their related department.
    -   The Department \[cmn\_department\] table provides a list of all departments and their related business unit.
    -   The prescribed metric performs a count on the number of users per business unit and weights the costs accordingly.

        Filter criteria: Only count active users.

-   **Allocate to Business Unit on Computer count**

    The metric allocates shared service cost to business unit based on the following weighting table:

    ![Allocate to Business Units on Computer count](../image/PrescribedMetric4.png "Allocate to Business Units on Computer count")

    -   The Computer \[cmdb\_ci\_computer\] table provides a list of all computer names and their related department.
    -   The Department \[cmn\_department\] table provides a list of all departments and their related business unit.
    -   The prescribed metric performs a count on the number of computers per business unit and weights the costs accordingly.
-   **Allocate to Business Unit on Change Request volume**

    The metric allocates shared service cost to business unit based on the following weighting table:

    ![Allocate to Business Unit on Change Request volume](../image/PrescribedMetric5.png "Allocate to Business Unit on Change Request volume")

    -   The Change Request \[change\_request\] table provides a list of all change requests and who requested it.
    -   The Department \[cmn\_department\] table provides a list of all departments and their related business unit.
    -   The prescribed metric performs a count of change requests per business unit and weights the costs accordingly.
        -   The weight table enforces lifespan on this metric.
        -   Duration start: Actual start.
        -   Duration end: Actual end.
-   **Allocate to Business Unit based on Incident volume**

    The metric allocates shared service cost to business unit based on the following weighting table:

    ![Allocate to Business Unit based on Incident volume](../image/PrescribedMetric6.png "Allocate to Business Unit based on Incident volume")

    -   The Incident \[incident.list\] table provides a list of all incidents and their related callers.
    -   The Caller \[users \[ITIL view\]\] table provides a list of all departments and their related business unit.
    -   The prescribed metric performs a count of incidents per business unit \(opened and closed within the period\) and weights the costs accordingly.
-   **Allocate to Business Application based on Compute Power**

    The metric allocates shared service cost to applications based on the following weighting table:

    ![Allocate to Application based on Compute Power](../image/PrescribedMetric7.png "Allocate to Application based on Compute Power")

    -   The CI Relationship \[cmdb\_rel\_ci\] table provides a list of all relationships between configuration items.
    -   The prescribed metric performs a count of configuration items where the Child.Class = Server and weights the costs accordingly to the receiving applications.

**Parent Topic:**[The Cost Models tab - Legacy](c_TheCostModelsTab.md)

**Related topics**  


[Prescriptive cost models for business services and business capabilities - Legacy](preconfigured-prescriptive-cost-models-two.md)

[View settings for each cost model - Legacy](../task/t_ViewSettingsForEachCostModel.md)

[Delete a cost model - Legacy](../task/t_DeleteACostModel.md)

[Compare cost models - Legacy](../task/t_CompareCostModels.md)

[Clone a cost model - Legacy](../task/t_CloneACostModel.md)

[Create breakdown relationship - Legacy](../task/t_CreateBreakdownRelationship.md)

