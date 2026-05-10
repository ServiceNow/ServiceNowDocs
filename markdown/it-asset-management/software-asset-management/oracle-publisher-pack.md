---
title: Software Asset Management publisher pack for Oracle
description: Use the Software Asset Management publisher pack for Oracle to track and optimize licensing for your Oracle products.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 10
breadcrumb: [Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Software Asset Management publisher pack for Oracle

Use the Software Asset Management publisher pack for Oracle to track and optimize licensing for your Oracle products.

The Oracle publisher pack supports the following Oracle products:

-   Oracle Database
-   Oracle Database options
-   Oracle management packs
-   Oracle WebLogic Server
-   Oracle Java

To use the publisher pack, activate the Software Asset Management Professional for Oracle plugin \(com.snc.samp.oracle\).

## Oracle licensing

The Oracle publisher pack adds Oracle specific licensing options for software entitlements.

<table id="table_fxl_ggn_4lb"><thead><tr><th>

Field

</th><th>

Options

</th></tr></thead><tbody><tr><td>

Agreement Type

</td><td>

-   Generic
-   Unlimited License Agreement \(ULA\)

</td></tr><tr><td>

License metric

</td><td>

-   Named User Plus
-   Per Processor
-   Employee

</td></tr><tr><td>

Metric group

</td><td>

Oracle

</td></tr></tbody>
</table>**Important:** The Software Asset Management application supports Bring Your Own License \(BYOL\) for Oracle Database and WebLogic Server across hybrid infrastructures. With BYOL support, you can track licenses for your Oracle Database and WebLogic Server in both on-premise and public cloud environments. For more information about Oracle BYOL support, see [Bring your own license or subscription to the public cloud](byol-concepts.md).

Additionally, you can use the Oracle Global License Advisory Services \(GLAS\) to manage licensing of your deployed Oracle software products. For more information, see [Oracle GLAS data collection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/oracle-glas-discovery.md).

## Oracle license metrics

The Software Asset Management application supports the following license metrics for Oracle:

-   **Named User Plus**

    The Named User Plus \(NUP\) license metric licenses all users and physical devices that access the following Oracle products:

    -   Oracle Database
    -   Oracle Database options
    -   Oracle management packs
    -   Oracle WebLogic Server
    If a user operates a device that accesses any of these Oracle products, the NUP license metric licenses both the user and the device. Use this license metric in environments where users and devices are easily identifiable and countable.

    **Important:** To use this license metric, you must create a corresponding client access record. Client access records enable you to track and manage the users or devices that are accessing a particular version of your software. The Software Asset Management application can then use the information in these client access records to reconcile your software. For more information on client access records, see [Create a software client access record in workspace](../task/create-clientaccess-workspace.md) or [Add a software client access record in Software Asset Management classic](../task/t_AddAClientAccessRec.md).

    The NUP license metric implements different licensing minimums based on the Oracle Database or Oracle WebLogic Server edition that your users and devices are accessing.

    |Oracle product edition|Licensing requirement|
    |----------------------|---------------------|
    |Oracle Database Standard Edition \(SE\) or Standard Edition One \(SE1\)|Minimum five NUP licenses required.|
    |Oracle Database Standard Edition 2 \(SE2\)|Minimum 10 NUP licenses required per database server. Additionally, each SE2 database can use a maximum of 16 CPU threads at any given time.|
    |Oracle Database Enterprise Edition|Minimum of either 25 NUP licenses per processor or the total number of users and devices that are accessing this database edition. The license metric sets this licensing minimum to the larger of the two values.|
    |Oracle WebLogic Server Standard Edition|Minimum 10 NUP licenses per processor.|
    |Oracle WebLogic Server Enterprise Edition|Minimum 10 NUP licenses per processor core.|
    |Oracle WebLogic Suite Edition|Minimum 10 NUP licenses per processor core.|

    Licensing minimums are automatically applied to the software models for your Oracle products using the following metric attributes:

    -   **Minimum users per processor** \(Oracle Database products\)
    -   **Minimum NUPs for WebLogic on-premise deployments** \(Oracle WebLogic Server products in on-premise environments\)
    -   **Minimum NUPs for WebLogic cloud deployments** \(Oracle WebLogic Server products in cloud environments\)
    The Software Asset Management application can then use the metric attribute values to determine the number of rights that are required for each Oracle product. To determine this number, the Software Asset Management application multiplies the appropriate metric attribute value by the number of processors or processor cores on the underlying physical server that the Oracle product is installed or running on. The resulting value is compared against the total number of users and devices that are accessing the Oracle product. The number of required rights is set to the larger of the two values.

    For example, 20 users are accessing an Enterprise Edition database that is running on a physical server with eight processor cores. The NUP license metric consumes 200 rights because the number of rights that is based on the metric attribute value \(25 minimum licenses x 8 CPU cores = 200 rights\) is greater than the number of users that are accessing the database \(20 users\).

-   **Per Processor**

    The Per Processor license metric licenses the server processors on which you install or run the following Oracle products:

    -   Oracle Database
    -   Oracle Database options
    -   Oracle management packs
    -   Oracle WebLogic Server
    -   Oracle Java
    Although you can install and run Oracle products on physical servers, virtual servers, partitioned servers, and the cloud, the Per Processor license metric licenses processors only on the underlying physical server or cloud server.

    The Per Processor license metric calculates the number of rights that are required for your Oracle products by multiplying the total number of processor cores by a core processor licensing factor, as specified on the [Oracle Processor Core Factor Table](http://www.oracle.com/us/corporate/contracts/processor-core-factor-table-070634.pdf). Use this license metric in environments where large numbers of users and devices are accessing the same environment or where users aren’t easily identifiable and countable, such as the internet.

    For example, a physical server that is running an Enterprise Edition database has two processors with four cores each. If your core processor licensing factor is 0.5, the Per Processor license metric consumes four rights for the physical server.

    2 CPUs x 4 CPU cores x 0.5 licensing factor = 4 rights.

    When you allocate rights for a database using the NUP or Per Processor license metric, Software Asset Management automatically allocates rights for the associated Database options and management packs using the same license metric.

    If you create a [Client Access License](../task/t_AddAClientAccessRec.md) \(CAL\) record to specify the number of users or devices that can access an Oracle Database or WebLogic Server, the Software Asset Management application licenses users and devices using only the NUP license metric. Software Asset Management doesn’t use the Per Processor license metric even if Per Processor licenses are available.

-   **Employee**

    The Employee license metric licenses the total number of full-time, part-time, and temporary employees, including those employed directly and indirectly through agents, contractors, and consultants, according to Oracle's definition of internal business operations.

    The Employee license metric calculates the number of licenses that are required by the total number of employees and not the number of employees that use the Oracle Java SE Universal. The licensing cost is calculated using a tier-based pricing model defined by Oracle. The pricing model is stored in the Price tier \[samp\_price\_tier\] table. For more details, see [Pricing model for Oracle Java SE Universal](../reference/oracle-price-tiers.md).

    Additionally, for the Employee license metric, the true-up cost is shown for a subscription period of one year.

    When you run reconciliation for a software model that has one or more entitlements with the Employee license metric, a right is consumed for each employee recorded in the resource value records. You can create a resource value record for the Java SE software model keeping the value of units consumed the same as the number of employees consuming the licenses. For details, see [Create a resource value record](../task/create-resource-value-record.md).

    When you're using a custom tier table, you can update the override license cost records associated with the Java SE software model. For details, see [Create or update an override license cost record](../task/create-edit-override-license-cost.md).


## Oracle verified third-party vendor tool

To collect installation and usage data for the Oracle products that are deployed in your environment, you must use a discovery process. With the verification and enrollment of ServiceNow in the Oracle Third-Party Tool Vendor \(3PTV\) Program, the ServiceNow Discovery application and Software Asset Management application are both verified by Oracle to collect and report on this data without requiring any Oracle measurement tools. You can collect and report on data for Oracle Database, Oracle WebLogic Server, Oracle Fusion Middleware, and the underlying hardware that supports these products.

During contract renewals and audits, Oracle requires you to provide specific usage data for your Oracle products.​ You can collect this data by running scripts that are provided by Oracle. These scripts collect data about the Oracle products that are deployed in your environment, as well as the physical and virtual hardware that supports those products.​ However, the process of collecting and reviewing this data can be very time consuming.

The ServiceNow Discovery application uses Oracle-verified Discovery patterns and reporting to collect the same data that is provided in the script output. You can collect this data regularly to track your compliance and minimize unexpected audit results.

For more information on Oracle discovery, see [Oracle Global License Advisory Services \(GLAS\) data collection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/oracle-glas-discovery.md).

**Note:** To access all the benefits of ServiceNow Discovery, request and install the CMDB CI Class Models application from the ServiceNow Store. See [CMDB CI Class Models store app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/cmdb-ci-class-models/cmdb-ci-class-models.md) for more information on this application.

-   **[Oracle Database and WebLogic Server licensing in partitioned environments](oracle-licensing-partitioned-environments.md)**  
The Software Asset Management application supports Oracle licensing rules for Oracle Database and WebLogic Server in both soft- and hard-partitioned environments. You can use partitioning to help reduce the number of licenses that are required for your installations.
-   **[Oracle licensing in cloud environments](oracle-licensing-cloud-environments.md)**  
The Software Asset Management application supports licensing rules for Oracle Database and WebLogic Server \(Standard, Enterprise, and Suite Editions\) in cloud environments.
-   **[Oracle Database licensing in multitenant architectures](oracle-licensing-multitenant-architectures.md)**  
The Software Asset Management application supports licensing rules for Oracle databases in multitenant architectures.
-   **[Oracle Database licensing for Standard Editions](oracle-db-licensing-std-edition.md)**  
Oracle Database Standard Editions are licensed on servers having a value less than the maximum capacity of sockets to help ensure risk-free license compliance.
-   **[Oracle Database options and management packs](../reference/oracle-options.md)**  
You can use the Software Asset Management publisher pack for Oracle to track licensing positions for your Oracle Database options and management packs. The Licensable Oracle Options \[samp\_oracle\_option\_set\] table provides the complete list of database options and management packs that you can create software models for.
-   **[Oracle reconciliation](oracle-recon.md)**  
Oracle reconciliation keeps your Oracle license positions accurate and up-to-date without requiring manual calculations. Reconciliation runs weekly or on-demand.
-   **[Oracle Infrastructure report](../reference/oracle-infrastructure-report.md)**  
You can use the Oracle Infrastructure report to gain visibility into your Oracle infrastructure. This report includes information about the Oracle databases and WebLogic Server editions that you’re running and the configuration items that are supporting them.
-   **[Oracle DB Server Deployments per Agreement report](../reference/oracle-server-agreement.md)**  
You can use the Oracle DB Server Deployments per Agreement report to gain visibility into your Oracle Database server deployments across hybrid infrastructures, based on the agreement type.
-   **[Software Publisher Analytics dashboard for Oracle in Software Asset Management classic](../reference/dashboard-oracle.md)**  
View compliance analysis results related to Oracle on the Software Publisher Analytics dashboard in the Software Asset Management classic application.
-   **[Publisher overview for Oracle in the Software Asset Workspace](../reference/publisher-overview-oracle.md)**  
View license usage information related to Oracle in the publisher overview for Oracle in the Software Asset Workspace.

**Parent Topic:**[Supported software publisher licenses](sam-publisher-packs.md)

