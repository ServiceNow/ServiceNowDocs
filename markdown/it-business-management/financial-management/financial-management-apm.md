---
title: Financial Management for licensed APM users - Legacy
description: If you are an Enterprise Architecture \(formerly Application Portfolio Management\) licensed user and using Financial Management, then the base system provides you with a Business Application Costing cost model that you can use to evaluate the cost of your business applications along with its prescribed metrics.
locale: en-US
release: australia
product: Financial Management
classification: financial-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Financial Management - Legacy, Project Portfolio Management, Strategic Portfolio Management]
---

# Financial Management for licensed APM users - Legacy

If you are an Enterprise Architecture \(formerly Application Portfolio Management\) licensed user and using Financial Management, then the base system provides you with a Business Application Costing cost model that you can use to evaluate the cost of your business applications along with its prescribed metrics.

## Business Application Costing cost model

![Business application costing cost model](../image/BusinessAppCostingCostModel.png "Business application costing cost model")

The specifications of the Business Application Costing cost model are:

-   The cost bucket layer is tied to the ITFM bucket table \[itfm\_bucket\] and the cost buckets are specific to the model.
-   IT shared service segment accounts are sourced from the IT shared service table \[itfm\_shared\_service\].
-   Business application segment accounts \(the middle layer in this model\) are sourced from the Business Application \[cmdb\_ci\_business\_app\] table. This table is the source of accounts to the applications segment. Or, it can be Application \[cmdb\_ci\_appl\] table or other custom tables.
-   The business unit layer is tied to the platform business unit table \[business\_unit\].
-   There is no data source to this cost model, which means that you should enter the spend information directly into the model and not come from the general ledger. Using the general ledger as a source of spend information is an optional feature that you can configure. See [Prerequisites to modify data source of a cost model](../reference/transition-data-source-cost-model.md) for more information.

## Seeded IT Shared Services

-   **IT Shared Service: End User Compute**

    IT Shared Service: Equip End Users is a cost collection container that holds any money spent on providing the end users with personal \(not shared\) devices, the software that runs on these devices, and the support associated with making and keeping those devices functioning. This container excludes major device upgrades, lease cycle turnover, and other replenishment-related costs, which are captured within the Facilitate Ongoing Change container.

-   **IT Shared Service: Database**

    IT Shared Service: Facilitate Configuration Change is a cost collection container that holds money spent on supporting the ITSM Change, Release and Configuration Management processes. That is, any dollars spent on managing ongoing, daily, common, and ad-doc configuration changes. This includes activities like patching \(non-security related\), firmware updates, hardware/software configuration setting changes, installation, de-installation, and upgrade of hardware components, and general add, move, or change requests across the IT landscape. This container excludes major upgrades and changes across a large portion of the environment for which a project plan and/or funding would need to be secured.

-   **IT Shared Service: Network**

    IT Shared Service: Facilitate Connectivity is a cost collection container that holds any money spent on providing all device network connectivity to the company, its computing and/or knowledge assets, the hardware and software to do it, and the support associated with making \(and keeping\) the access up. This includes all personal and enterprise devices. This container excludes monitoring hardware, software, and personnel costs, which are captured in the Monitor the Environment container.

-   **IT Shared Service: IT Management**

    IT Shared Service: Management and Overhead is a cost collection container that holds any money spent on IT executive compensation, as well as one-time charge items that apply to the existence of IT operations, compliance or audit costs, and otherwise uncategorised costs. This container excludes any costs captured or accounted for in any of the other IT process definitions.

-   **IT Shared Service: Data Center**

    IT Shared Service: Monitor the Environment is a cost collection container that holds the money spent on supporting the ITOM Event Management process; that is, any dollars spent on monitoring the entire IT landscape. This includes endpoint connectivity speeds, endpoint application performance testing, hardware/software/network/storage threshold checking, and fault and event correlation management tools used by operations management personnel. This container excludes security specific and/or cloud monitoring services mentioned in other process areas.

-   **IT Shared Service: IT Operations**

    IT Shared Service: Perform Upgrades/Maintenance is a cost collection container that holds money spent supporting the ITSM Change, Release and Configuration Management processes. That is, all dollars spent on managing major upgrades, either project planned and/or specifically funded. This includes activities such as widespread OS upgrades; hardware replacement cycle activities; and internal or third-party business or IT management software package release updates across the IT landscape. This container excludes ongoing, daily, common, and ad-doc configuration changes that only require a change ticket to be executed.

-   **IT Shared Service: Service Desk**

    IT Shared Service: Provide Tech Support is a cost collection container that holds money spent supporting the ITSM Incident, Problem and Knowledge Management processes. That is, any dollars spent on providing technical support services to end users across the organization. This includes tier 1, 2, and 3 personnel, incident or problem management software, root cause analysis time, routine or ad-doc assistance \(password resets, how to Q&amp;A\), and/or standard operating procedure guidance. This container excludes actual configuration changes to end user and/or corporate assets performed by way of documented change tickets.

-   **IT Shared Service: Application**

    IT Shared Service: Run Business Applications is a cost collection container that holds any dollars spent on ongoing personnel time to keep business applications operating. This includes resources dedicated to applications and excludes IT or infrastructure operation costs.

-   **IT Shared Service: Security &amp; Compliance**

    IT Shared Service: Secure the Environment is a cost collection container that holds money spent on supporting the Security Operations. That is, any dollars spent on providing information security across the corporate IT landscape. This includes individual user endpoint devices, cloud applications, cloud computing, and/or on-premise computing resource of all types in addition to all desktops, laptops, smart phones, network gear, servers, databases, and applications. This excludes the physical security costs associated with datacenters, and office space card readers.

-   **IT Shared Service: Storage**

    IT Shared Service: Store and Manage Data is a cost collection container that holds any dollars spent on the underlying tools and foundational activities related to the management of structured and unstructured data \(for example, encryption, backups, purging, archiving, migrations, and DR replication\) and/or storage capacity \(for example, reorganizations and excess capacity acquisition\). It includes these types of activities and all the people power used to ensure the health of the data and storage landscape. This container excludes elements related to local storage on end user devices utilized by single individuals and specific activities, and allocated storage that can be related to specific applications or systems.

-   **IT Shared Service: Compute**

    IT Shared Service: Supply Computing Power is a cost collection container that holds any dollars spent on providing foundational elements that exist, cost money to maintain, but may never actually be used such as disaster recovery facilities or contracts, hardware spares inventory, on-premises UPS systems, and generators. It also includes daily active data center costs related to things such as space, power, and cooling.


## ITFM prescribed metrics

-   **Allocate to Application based on Active User Count**

    The metric allocates shared service cost to applications based on the following weighted metric:

    ![Allocate to Applications using active user count.](../image/PrescribedMetricSStoBAonUC.png "Allocate to Applications using active user count")

    -   The Business Application \[cmdb\_ci\_business\_app\] table provides a list of all business applications.
    -   The prescribed metric performs a sum of active users and weights the costs accordingly to the receiving applications by **Sys ID**.
-   **Allocate to Application based on Compute Power**

    The metric allocates shared service cost to applications based on the following weighting table:

    ![Allocate to Application based on Compute Power](../image/PrescribedMetric7.png "Allocate to Application based on Compute Power")

    -   The CI Relationship \[cmdb\_rel\_ci\] table provides a list of all relationships between configuration items.
    -   The prescribed metric performs a count of configuration items where the Child.Class = Server and weights the costs accordingly to the receiving applications.
-   **Allocate to Business Unit on Headcount**

    The metric allocates shared service cost to business unit based on the following weighting table:

    ![Allocate to Business Unit on Headcount](../image/PrescribedMetric3.png "Allocate to Business Unit on Headcount")

    -   The User \[sys\_user\] table provides a list of all system users and their related department.
    -   The Department \[cmn\_department\] table provides a list of all departments and their related business unit.
    -   The prescribed metric performs a count on the number of users per business unit and weights the costs accordingly.

        Filter criteria: Only count active users.


## Dashboards for Business Application Costing cost model

There are three performance analytic dashboards that you can access with Business Application Costing cost model. They are:

-   [Application TCO dashboard](../../../use/dashboards/application-content-packs/financial-mgmt-application-TCO-dashboard.md).
-   [Business Application Costing dashboard](../../../use/dashboards/application-content-packs/financial-mgmt-level2-costing-business-applications.md).
-   [CIO Dashboard for Business Applications.](../../../use/dashboards/application-content-packs/cio-dashboard-business-application.md) [CIO Dashboard for Business Applications](../../../use/dashboards/application-content-packs/cio-dashboard-business-application.md).

-   **[Configure business application costing cost model - Legacy](../task/modify-bus-app-costing-cost-model.md)**  
Configure the business application costing cost model to allocate expenses and generate bucket cost lines for the fiscal periods to suit your requirements.

**Parent Topic:**[Financial Management - Legacy](c_ITFinance.md)

