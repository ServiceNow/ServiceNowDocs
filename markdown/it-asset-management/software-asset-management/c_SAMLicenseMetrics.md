---
title: Software license metrics
description: License metrics are set in software entitlements and used for reconciliation in various metric groups and software model combinations.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 13
breadcrumb: [Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# Software license metrics

License metrics are set in software entitlements and used for reconciliation in various metric groups and software model combinations.

Each metric group has a set of license metrics that are specific to the publisher.

You can view the Metric Attributes related list in software models to set the attribute value. For more information, see [Software model fields](../reference/software-model-fields.md).

You can also add custom license metrics. For more information, see [Add a custom license metric](../task/add-custom-license-metric.md). You can use the Resource Value \[samp\_sw\_resource\_value\] table to enhance the custom license metric capability by doing a 1:1 calculation between the Unit consumption column in the Resource Value \[samp\_sw\_resource\_value\] table and the Licenses required column in the License Metric Results \[samp\_license\_metric\_result\] table.

Adobe, Citrix, IBM \(includes both IBM and Red Hat\), Microsoft, Oracle, SAP, and VMware publisher packs are available as add-ons. They provide the capability to manage software licensed under the publisher licensing models.

Installing [SaaS License Management](sam-subscription-management.md) adds the Subscription and Consumption metric groups.

You can view descriptions of your license metrics by selecting the reference ![](../image/reference-icon.png) icon next to the **License metric** field in your software entitlements.

<table id="table_zqx_hhf_b1b"><thead><tr><th>

Metric group

</th><th>

License metric

</th></tr></thead><tbody><tr><td>

Adobe **Note:** Adobe license metrics are visible only if the Adobe publisher pack is installed.

</td><td>

-   Per Device: Licenses a device for the number of installations of software.
-   Per User: Licenses a user for the number of installations of software.
-   User Subscription: Licenses a user for the number of activated software subscriptions.

When you run a reconciliation for software models with one or more entitlements, a right is consumed for each active unique software subscription record assigned to a user.

    -   A right is considered **Allocated in use** when a user has both a user allocation and a subscription record.
    -   A right is considered **Not Allocated in use** when a user doesn't have a user allocation but has a subscription record.
    -   A right is considered **Allocated not in use** when a user has a user allocation but doesn't have a subscription record.
If multiple rights are assigned to a user in a user allocation, then the user has the corresponding number of subscriptions for the software model. For example, a user has a user allocation with two rights but only one subscription record related to a software model. In this example, one right is considered **Allocated in use** and the second right is considered **Allocated not in use**.


</td></tr><tr><td>

Citrix **Note:** Citrix license metrics are visible only if the Citrix publisher pack is installed.

A discovery process is required for Citrix data to be collected. Admin users must create a [Discovery schedule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/t_CreateADiscoverySchedule.md) to run on the Citrix Delivery Controller for communication with the Citrix License Server.

See for information on the Citrix discovery pattern and tables.

</td><td>

-   Concurrent User: Licenses the number of simultaneous users accessing the program.
-   Per Device: Licenses a device for the number of installations of software.
-   Per Processor \(CPU count\): Licenses processors on either a physical server or virtual machine.
-   Per User: Licenses a user for the number of installations of software.

If you're reconciling Citrix server software through a client access record, this license metric licenses the users that are accessing the server.

-   Per User/Device: License a unique user or a shared device. If the license is assigned to a user, they have unlimited connections to an unlimited number of devices. If the license is assigned to a device, an unlimited number of users can connect to a single device.

If you create an entitlement with the Citrix metric group and the Per User/Device license metric is specified, the license calculator checks the compliance of all related software models based on the number of distinct users and devices.

If you're reconciling Citrix server software through a client access record, this license metric licenses the users and devices that are accessing the server.


</td></tr><tr><td>

Common

</td><td>

-   Per Core: Licenses cores on a physical server or virtual machine.

    ```
CPU core count * CPU count
    ```

-   Per Device: Licenses a device for the number of installations of software.
-   Per Named Device: Licenses a specific device for the number of installations of software.

**Note:** You must add allocations.

-   Per Named User: Licenses a specific user for the number of installations of software.

**Note:** You must add allocations.

-   Per Processor \(CPU count\): Licenses processors on either a physical server or virtual machine.
-   Per User: Licenses a user for the number of installations of software.
-   User CAL: Licenses each user that accesses your server, regardless of the number of devices that each user is using to access the server.
-   Device CAL: Licenses each device that accesses your server, regardless of the number of users that are using each device to access the server.
-   User/Device CAL: Licenses each user or device that accesses your server.
-   Resource Consumption. Consumption-based license metric that supports CAL reconciliation. A 1:1 ratio calculation between the Unit consumption column in the Resource Value \[samp\_sw\_resource\_value\] table and the Licenses required column in the License Metric Results \[samp\_license\_metric\_result\] table.

</td></tr><tr><td>

Concurrent Licenses **Note:** Concurrent Licenses license metrics are visible only if the Software Asset Management Professional for Engineering Applications \(sn\_samp\_eng\_app\) plugin is activated along with OpenLM and Open iT integration.

</td><td>

These licenses are based on the number of simultaneous users or devices accessing the software.

 -   Floating: Shares and manages a pool of software among users or devices on a network. Checks out a license when a user or device requests access to the software. If there's no license left at the peak of license consumption, the user or device is denied access to the software. The number of rights consumed is based on the peak number of licenses checked out during a specified time.
-   Token: Shares and manages a pool of tokens among users or devices. Checks out a token or a set of tokens when a user or device requests access to the software. If there are no tokens left at the peak of license consumption, the user or device is denied access to the software. The number of rights consumed is based on the peak number of tokens checked out during a specified time.
-   Network: Shares and manages a pool of licenses among users or devices within a specified TCP or IP network. Checks out a license when a user or device requests access to the software. If there's no license left at the peak of license consumption, the user or device is denied access to the software. The number of rights consumed is based on the peak number of licenses checked out during a specified time.

</td></tr><tr><td>

Consumption**Note:** Consumption license metrics are visible only if the SaaS License Management is installed.

</td><td>

SaaS Consumption: Licenses an organization based on the unit of measure for the software units that can be consumed.

</td></tr><tr><td>

CrowdStrike

</td><td>

-   Reserved Hourly Average Sensor: Counts the number of unique active endpoints per clock-hour and averages them over a rolling 28-day period. The count of Reserved Hourly Average Sensor Licenses resets at the start of each clock-hour.
-   Sensor Subscription: Calculates license usage by averaging endpoint counts over four consecutive weeks. Weekly endpoint counts are based on the total number of endpoints consumed in the previous seven days.

 **Note:** These license metrics are available with Yokohama Patch 1, Software Asset Management - SaaS License Management \(sn\_sam\_saas\_int\) 15.0.8, and Software Asset Management \(sn\_itam\_samp\) 2.1.0 version onwards. If you are on any version for Yokohama below Patch 1, refer [KB1801232](https://support.servicenow.com/kb?id=kb_article_view&sys_kb_id=ef634dac83935610cdbbc430feaad3d9).

</td></tr><tr><td>

IBM **Note:** IBM license metrics are visible only if the IBM publisher pack is installed.

</td><td>

-   Authorized User: Licenses each user who is granted access to an IBM software product.
-   Authorized User Value Unit: Licenses the number of select users who are granted access to an IBM software product.
-   Employee User Value Unit: Licenses the total number of users within your organization who are granted access to an IBM software product.
-   External User Value Unit: Licenses the total number of users outside your organization who are granted access to an IBM software product.
-   Per Device: Licenses a device for the number of installations of software.
-   Per Named User: Licenses a specific user for the number of installations of software.
-   Per Processor \(CPU count\): Licenses processors on either a physical server or virtual machine.
-   Per User: Licenses a user for the number of installations of software.
-   Processor Value Unit \(PVU\): Licensing is based on the processor technology and the number of processors that are made available to the program. Full capacity PVU entitlements require licenses for all activated processor cores in the physical hardware environment. Subcapacity PVU entitlements require licenses for less than the full capacity of your server or group of servers.
-   Resource Value Unit \(RVU\): Licensing is based on the number of activated processor cores used or managed by a product. Full capacity RVU entitlements require licenses for all activated processor cores in the physical hardware environment. Subcapacity RVU entitlements require licenses for less than the full capacity of your server or group of servers.
-   Virtual Processor Core \(VPC\): Licenses the number of virtual CPUs \(vCPUs\) that are available to or managed by a product.

**Note:** This license metric is available only if you request and install the IBM License Compliance for Software Asset Management application from the ServiceNow Store.


</td></tr><tr><td>

Microsoft **Note:** Microsoft license metrics are visible only if the Microsoft publisher pack is installed.

</td><td>

-   Device CAL: Licenses the number of device client access licenses to server software.
-   Per Core: Licenses the cores on both the physical server and the virtual cores that support virtual machines and presents a cost-efficient model based on the number of rights used. For information on Per Core for Microsoft SQL Server Enterprise edition with Software Assurance, see [Create entitlements for Microsoft Software Assurance in Software Asset Management classic](../task/create-entitlement-microsoft-sa.md).

**Note:** Per Core \(Physical Core\) and Per Core \(Virtual OSE\) metrics is deprecated from the New York release. Any existing entitlements using Per Core \(Physical Core\) and Per Core \(Virtual OSE\) metrics are replaced with Per Core. You may see a change in your reconciliation results.

-   Per Core \(with CAL\): Licenses physical servers. The number of licenses depends on the number of installs and Operating System Environments \(OSEs\).

Per Core \(with CAL\) licenses at the cluster level only when the physical server is an ESX Server and is a part of a cluster. This license metric uses all processors on every ESX Server within a cluster to determine the total number of cores or processors that must be licensed on the cluster.

**Note:** If vMotion or DRS is enabled on a cluster, any virtual machine can move to any ESX Server within that cluster. The peak capacity of the cores on all the ESX Servers is considered for the rights needed to license the cluster.

-   Per Device: Licenses a device for the number of installations of software.
-   Per Processor: Licenses a set number of processors on a physical server.
-   Per User: Licenses a user for the number of installations of software.
-   Server \(Per Instance\): Licenses a set number of software installations on either a physical server or virtual machine.
-   Server \(Per Server\): Licenses all software installations on a physical server and any virtual machines hosted by the physical server.
-   User CAL: Licenses the number of user client access licenses to server software.
-   User Subscription: Licenses a user for the number of activated software subscriptions.

When reconciliation is run for a software model that has one or more entitlements with the User Subscription license metric, one right is consumed for each active unique software subscription record assigned to a user.


</td></tr><tr><td>

Oracle **Note:** Oracle license metrics are visible only if the Oracle publisher pack is installed.

</td><td>

-   Named User Plus: Licenses the physical host.

If you are reconciling Oracle server software, such as Oracle Database Server or Oracle WebLogic Server, through a client access record, this license metric licenses the users that are accessing the server.

-   Per Processor: Licenses the number of cores on a processor.

**Note:** For the Oracle **Per Processor** license metric, enable Hyper-Threading if you're using a virtual machine \(VM\) running Amazon Web Services \(AWS\).

-   Employee: Licenses the total number of full-time, part-time, and temporary employees, including those employed directly and indirectly through agents, contractors, and consultants according to Oracle's definition of internal business operations.

**Note:** The number of licenses required is determined by the total number of employees and not the number of employees using Oracle Java SE Universal.


 **Note:** You can select the level of aggregation for the reconciliation calculation of VMware -based Oracle instances using the **com.snc.samp.oracle.reconlevel** property. See [Software Asset Management properties](../reference/sam-properties.md).

</td></tr><tr><td>

Red Hat **Note:** Red Hat license metrics are visible only if the IBM publisher pack is installed.

</td><td>

-   Per Socket-pair: Licenses the number of socket pairs on the physical host or the number of virtual machine \(VM\) pairs running a Red Hat Enterprise Linux server on a physical host.
-   Per Core: Licenses the cores on both the virtual cores that support virtual machines and the physical server. It also presents a cost-efficient model based on the number of rights used.

</td></tr><tr><td>

SAP **Note:** SAP license metrics are visible only if the SAP publisher pack is installed.

</td><td>

-   Named User: Licenses the number of named users that can be assigned a Named User Type. The Named User Type is defined by the software model linked to the entitlement.
-   Engine Measurement: Licenses the amount of engine usage.
-   Digital Access: Licenses the indirect usage of SAP applications through a third-party application or a non-SAP intermediary software by the count of documents created by the third-party application.
-   Full Usage Equivalent \(FUE\): Licenses the number of users that are authorized to access specified solution capabilities of SAP S/4HANA Cloud Public Edition.

</td></tr><tr><td>

Subscription**Note:** Subscription license metrics are visible only if the SaaS License Management is installed.

</td><td>

User Subscription: Licenses for the number of users.

</td></tr><tr><td>

VMware **Note:** VMware license metrics are visible only if the VMware publisher pack is installed.

</td><td>

-   Per Application Instance: Licenses the number of application instances.

Applies to VMware products: vCenter Server software.

-   Per Device: Licenses a device for the number of installations of software.

Applies to the VMware suite of products: Horizon FLEX, ThinApp, ThinApp Virtualization Packager, and Mirage Windows Migration.

-   Per Named User: Licenses a specific user for the number of installations of software.

Applies to VMware named users: Horizon Advanced, Horizon Enterprise, Horizon Suite, Mirage, Horizon Socialcast on Premise, Workspace \(Portal\), Workspace Suite, Horizon Air, Horizon Air Desktop DR, ThinApp, ThinApp Virtualization Packager, vRealize Operations for Horizon, User Environment Manager, vRealize Business.

-   Per OSI: Licenses the operating system \(OS\) that is running on a virtual machine \(VM\) or physical host.

Applies to the VMware suite of products: vRealize Operations, vRealize Log Insight, vRealize Automation, vRealize Business for Cloud, and vRealize Code Stream.

-   Per Processor: Licenses the processors \(CPUs\) on a physical host. Each CPU requires one right for every 32 cores. A **Maximum cores per processor** metric attribute with a default value of 32 is automatically created on software models for VMware per processor entitlements. This metric attribute is used during reconciliation to determine license compliance.

Applies to VMware suite products: vSphere, vSphere with Operations Management.

-   Per Core: Licenses the processor cores on a physical host. A minimum of 16 cores must be licensed per processor.

Applies to subscription-based VMware suite products: VMware vSphere Standard \(VVS\) and VMware vSphere Essentials Plus \(VVEP\)


</td></tr></tbody>
</table>-   **[Unlimited software licenses](unltd-allocations-rights.md)**  
Unlimited software licenses help you to create entitlements with unlimited allocations and unlimited rights, allowing you to license any number of software installations with no true-up cost.

**Parent Topic:**[Exploring Software Asset Management](explore-sam-workspace.md)

