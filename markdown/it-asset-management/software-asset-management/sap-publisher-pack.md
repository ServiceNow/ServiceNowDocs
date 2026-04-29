---
title: Software Asset Management publisher pack for SAP
description: Use the Software Asset Management publisher pack for SAP to manage and optimize your SAP licenses. Get comprehensive visibility into your SAP license compliance and uncover potential savings.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 13
breadcrumb: [Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Software Asset Management publisher pack for SAP

Use the Software Asset Management publisher pack for SAP to manage and optimize your SAP licenses. Get comprehensive visibility into your SAP license compliance and uncover potential savings.



**Note:** You can use the SAP publisher pack to manage and optimize licensing for SAP NetWeaver 7.4, SAP\_BASIS 740, and later versions.

**Note:** To use the publisher pack, install the Software Asset Management Professional for SAP plugin \(com.sn\_samp\_sap\).

## Supported license types

The SAP publisher pack supports licensing for named users, engine measurement, third-party access, and full-usage equivalent.

-   **Named Users**

    SAP named users are the members in your organization who use SAP applications. You can purchase different types of named user licenses and then assign each license to a named user.

    The SAP publisher pack supports named user licenses for both SAP ERP Central Component \(ECC\) applications and SAP S/4HANA applications. Different named user license types are supported based on the application type. SAP ECC applications support various named user license types, including Professional, Limited Professional, and Employee Self Service. SAP S/4HANA applications support only the Developer Access, Enterprise Management for Professional Use, Enterprise Management for Functional Use, Enterprise Management for Productivity Use, Technical SAP Engine User, and Technical Use named user license types. The ServiceNow AI Platform supports all named user types for both SAP ECC applications and SAP S/4HANA applications.

-   **Engines \(automated, calculated, and self-declared\)**

    SAP engines, also known as packages, are optional applications that require additional licenses. Every engine has a unique license metric that is used to calculate the license usage for the engine. Examples of license metrics include the number of employees or number of contracts.

    License usage is calculated through either an automated SAP engine measurement, calculation based on multiple engine measurements plus an indicator, or a manual self-declaration process.

    -   If an engine is supported by the SAP engine measurement process, Software Asset Management automatically calculates the license usage for that engine.
    -   If an engine is identified to be composed of multiple engine measurements, Software Asset Management calculates this value if the indicator license metric is also available.
    -   If an engine isn’t supported by the SAP engine measurement process, you must manually enter the license usage information for that engine using the self-declaration process. For information on how to self-declare your SAP engine license usage, see [Self-declaring SAP engine license usage](self-declaring-sap-engine-usage.md).
    To view the complete list of engines that are supported by each process, see [Engine &amp; Self-Declaration Product Measurement](https://support.sap.com/en/my-support/systems-installations/system-measurement/engine-self-declaration-product-measurement.html) in the SAP Support Portal.

    **Important:** You must have an SAP Support Portal account to access the SAP Support Portal.

    The SAP publisher pack supports engine licenses for both SAP ERP Central Component \(ECC\) applications and SAP S/4 HANA applications.

    **Note:** Starting with the Australia release, revenue-based licensing support is enabled for SAP Engine products. You can use higher value revenue-based products for purchased rights and unit cost. For details on enabling the support for revenue-based licensing, see the knowledge base article [KB1641524](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1641524).

-   **Digital Access**

    The Digital Access license applies to indirect usage of SAP systems by people or third-party applications without logging in to the system directly. A few examples for indirect usage of SAP systems are as follows:

    -   Using a third-party application to perform actions in the SAP system
    -   Entering data into the SAP system from a third-party application
    -   Viewing data in the SAP system from a third-party application
    When you have many third-party product integrations with SAP systems, you can avoid unnecessary consumption of your named user license by purchasing Digital Access licenses. In this licensing model, the usage of SAP applications is licensed by the count of the predefined documents created by the third-party application. The details of the predefined document types are stored in the SAP Document Type \[samp\_sap\_document\] table that's installed with the Software Asset Management Professional for SAP \(com.sn\_samp\_sap\) plugin.

    |Document name|Document multiplier|
    |-------------|-------------------|
    |Sales document|1|
    |Purchase document|1|
    |Invoice document|1|
    |Manufacturing document|1|
    |Material document|0.2|
    |Quality Management document|1|
    |Service and Maintenance document|1|
    |Financial document|0.2|
    |Time Management document|1|

    The SAP system stores the digital access data of the supported document types for different users and client systems. Make sure you have any of the following tools to pull the digital access data from the SAP system to your ServiceNow instance:

    -   SAP Passport tool
    -   SAP Estimation tool
    **Note:** When you purchase an SAP Digital Access license, these tools are available for installation without any additional cost. For details on the SAP tools, see [SAP Help Portal](https://help.sap.com/viewer/index).

    When any of the predefined document types are created in the SAP system through a third-party application, the Digital Access licensing cost is applicable. However, there are no additional charges associated with reading, updating, or deleting these documents.

    For the SAP Digital Access software model, digital access usage is calculated as follows:

    1.  The total count of documents of a particular document type created on each SAP system by all your users is calculated.

        Consider a scenario where User A created 5 Material documents, and User B created 5 Material and 10 Sales documents on an SAP system. The total count of Material documents is 10 and Sales documents is 10.

    2.  The license consumption is calculated by multiplying the total count of a particular document type by the Document multiplier.

        Based on the scenario mentioned in the preceding step, licenses consumed by Material documents is 2 \(10\*0.2\) and by Sales documents is 10 \(10\*1\). So, the total Digital Access license consumed is 12.

    **Note:** The SAP Digital Access software model is installed with the Software Asset Management Professional for SAP \(com.sn\_samp\_sap\) plugin.

    Reconciliation for the SAP Digital Access software model is done by comparing the Purchased rights with the licenses that you consumed.

-   **Full Usage Equivalent \(FUE\)**

    The FUE license applies to the users of SAP S/4HANA Cloud applications. FUE is granted to the number of users that are authorized to access specified solution capabilities. A single FUE can be allocated to different use types with a specific weighting factor.

    The FUE framework for licensing provides the required level of access and flexibility to different cloud use types. An FUE license can be distributed to any of the four different cloud use types that have a specified weighting factor.

    -   Self-Service Use: This FUE applies to users that are using the SAP S/4HANA Cloud application through self-service portals, providing access to basic business processes, data viewing, and report generation. This use type is intended for users who mainly access information or engage with the application via predefined self-service features. Additionally, it’s used to display and manage use rights, data consumption, and lightweight tasks.
    -   Core Use: This FUE includes all rights from the Self-Service use type and is designed for users who need restricted access to the SAP S/4HANA Cloud application. Core users can view data, run reports, and run basic business processes. This use type is ideal for users who require access to specific information or perform routine tasks without needing comprehensive functionality.
    -   Advanced Use: This FUE includes all rights from the Core use type and grants users full access to the SAP S/4HANA Cloud application. This type of access enables users to create and edit data, run reports, and use all available business processes. It’s assigned to users who need extensive functionality that is crucial for managing key business operations.
    -   Development Use: This FUE grants authorized users the license to access the development tools provided with the SAP S/4HANA Cloud ABAP Environment.
    The details of the predefined cloud use types are stored in the SAP Cloud Use Types \[samp\_sap\_cloud\_use\_type\] table that's installed with the SAP S/4HANA spoke plugin. For more information, see [License calculation for SAP cloud use types](../reference/license-calculation-sap-cloud.md).

    |Cloud user type|Weighing factor|
    |---------------|---------------|
    |Development User|One FUE = 0.5|
    |Advanced User|One FUE = 1|
    |Core User|One FUE = 5|
    |Self-Service User|One FUE = 30|

    An example of FUE license allocation to different cloud user types:

    40 SAP S/4HANA Cloud users for advanced use = 40 FUE licenses

    75 SAP S/4HANA Cloud users for core use = 15 FUE licenses

    270 SAP S/4HANA Cloud users for self-service use = 9 FUE licenses


## SAP connection with the ServiceNow AI Platform

To start connecting your SAP systems and your ServiceNow instance, [deploy the ABAP program for SAP](../task/import-abap-program-sap.md). Then, follow the steps to [establish an SAP connection](../task/add-sap-connection.md).

The Software Asset Management publisher pack for SAP uses a centralized design. When you import transport files into an SAP client that is considered a central system, the client uses the custom program-selected Remote Function Call \(RFC\) connection list to connect all other clients through RFC from the central system. It then fetches data to store in central system custom tables. To import the transport files, use either the SAP Solution Manager or another SAP client that has RFC connections activated to fetch data into a central system.

After the connection is established, data is pulled into your ServiceNow instance from your SAP system. For a list of all data that is pulled, see [Tables installed with the SAP publisher pack](component-installed-sap-plugin.md).

SAP data is scheduled to be pulled weekly. User activity data, web activity data, and engine usage data are pulled monthly. All user and web activity is deleted after 90 days. Engine usage measurement records in the SAP License Metric Measurement table \[samp\_sap\_license\_metric\_measurement\] are deleted after one year.

When SAP data enters the ServiceNow AI Platform, it’s initially stored in staging tables before it’s transferred to the final SAP tables. To edit the tables where data transfer takes place or to view the transfer logic, see [transform maps](https://www.servicenow.com/docs/access?context=c_CreatingNewTransformMaps&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

**Note:** The user activity and web activity transform maps aren't enabled by default because they may cause performance issues due to the large amount of data. However, you can manually enable these transform maps. To enable the activity transform maps, navigate to **All** &gt; **Software Asset** &gt; **SAP Compliance and Optimization** &gt; **SAP Connections** and select the connection. In the Configuration section, set the **Fetch activity** field to **True** and then select **Update**.

## View SAP license usage and compliance

View your SAP license costs, usage, and compliance using the [Software Publisher Analytics dashboard](../reference/dashboard-sap.md) \(Software Asset Management classic application\) or [publisher overview](../reference/publisher-overview-sap.md) \(Software Asset Workspace\). The dashboard and overview also show how you can optimize license consumption by reassigning user roles in your SAP system. You can view the license optimization details in the Software asset analytics view. For more details, see [Publisher optimizations for SAP](../reference/pub-opt-sap.md).

Reconciliation runs weekly or on demand to determine your license compliance position for all of your SAP products. Reconciliation compares your purchased rights recorded in software entitlements with actual usage data pulled from your SAP systems. You can view reconciliation results for SAP in the License usage view of the Software Asset Workspace. The License usage view shows unlicensed users and engines, digital access licenses available and required, and remediation options to make your license position compliant, potential savings, and more. For more information on the License usage view, see [License usage view](sam-workspace-workbench.md).

To view Software license compliance position reports for SAP, navigate to **License usage** &gt; **Reports** &gt; **Software license compliance position** in the Software Asset Workspace.

-   **[Tables installed with the SAP publisher pack](component-installed-sap-plugin.md)**  
Tables are installed with the Software Asset Management Professional for SAP plugin. The tables store data pulled from the SAP systems.
-   **[Deploy the ABAP program for SAP](../task/import-abap-program-sap.md)**  
To begin establishing a connection between your SAP system and your ServiceNow instance, deploy the Advanced Business Application Programming \(ABAP\) program. Deploying the ABAP program allows data to be shared between SAP and your ServiceNow instance.
-   **[Establish an SAP connection using basic authentication](../task/add-sap-connection.md)**  
After you have deployed the Advanced Business Application Programming \(ABAP\) program in your SAP system, create a connection profile to establish a connection between your SAP system and your ServiceNow instance using basic authentication.
-   **[Establish an SAP connection using OAuth 2.0](../task/add-sap-connection-oauth.md)**  
Create a connection profile to establish a connection between your SAP system and your ServiceNow instance using OAuth 2.0 authentication.
-   **[Create entitlements for SAP](../task/create-entitlement-sap.md)**  
Create software entitlements to record your license information for SAP products. You can create entitlements individually or import them from a spreadsheet.
-   **[Create software models for SAP](../task/add-software-model-sap.md)**  
Create software models to record SAP product information.
-   **[Create a custom SAP named user type](../task/create-named-user.md)**  
Create a custom SAP named user type so that you can track and manage your SAP licenses based on the named user type that is specific to your SAP system.
-   **[Map a role to a named user type](../task/create-named-user-type-role-mapping.md)**  
You can optimize your SAP licenses by mapping roles to a named user type. During reconciliation, discovered user roles and their assigned named user types are compared against these roles to identify user that can be given a lower named user type.
-   **[Create custom SAP price lists](../task/create-sap-pricelist.md)**  
Create custom SAP price lists so that you can track and manage SAP licenses based on the contracts that are specific to your SAP system.
-   **[Import custom SAP named user types](../task/import-custom-sap-named-user-type.md)**  
Import custom SAP named user types into your ServiceNow® instance so that you can track and manage SAP licenses based on the named user types that are specific to your SAP system.
-   **[Import custom SAP price lists](../task/import-custom-sap-price-list.md)**  
Import custom SAP price lists into your ServiceNow® instance so that you can track and manage SAP licenses based on the contracts that are specific to your SAP system.
-   **[SAP USMM-based optimization](usmm-optimization.md)**  
Optimize licensing through SAP User License Measurement \(USMM\) rules that map roles to the Named User Type for an SAP client.
-   **[User transaction activity for named user types](sap-named-user-transaction-activity.md)**  
Determine license optimizations for your SAP named user types based on your SAP user transaction activity.
-   **[Self-declaring SAP engine license usage](self-declaring-sap-engine-usage.md)**  
You can self-declare the license usage for any SAP engines that cannot be measured by the automated SAP engine measurement process. Use this information to gain more comprehensive visibility into your SAP license compliance position so that you can optimize your licensing costs.
-   **[Software Publisher Analytics dashboard for SAP in Software Asset Management classic](../reference/dashboard-sap.md)**  
View your license compliance position for SAP on the Software Publisher Analytics dashboard in the Software Asset Management classic application.
-   **[Publisher overview for SAP in the Software Asset Workspace](../reference/publisher-overview-sap.md)**  
View license usage information related to SAP in the publisher overview for SAP in the Software Asset Workspace.

**Parent Topic:**[Supported software publisher licenses](sam-publisher-packs.md)

