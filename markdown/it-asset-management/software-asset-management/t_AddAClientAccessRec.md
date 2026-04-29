---
title: Add a software client access record in Software Asset Management classic
description: Add a client access record to track and manage the users or devices that are accessing a particular version of your server software using a client access license \(CAL\).
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 9
breadcrumb: [Using Software Asset Management classic, Software Asset Management, IT Asset Management]
---

# Add a software client access record in Software Asset Management classic

Add a client access record to track and manage the users or devices that are accessing a particular version of your server software using a client access license \(CAL\).

## Before you begin

Role required: sam\_admin

**Note:** You can also use the sam\_user role to view and read client access records. However, you cannot use this role to create client access records.

## About this task

Software Asset Management uses client access records to reconcile server software based on the following license metrics:

<table id="table_tjy_v4m_11b"><thead><tr><th>

Metric group

</th><th>

License metric

</th></tr></thead><tbody><tr><td>

Citrix

</td><td>

-   Per User
-   Per User/Device

</td></tr><tr><td>

Common

</td><td>

-   User CAL
-   Device CAL
-   User/Device CAL

</td></tr><tr><td>

IBM

</td><td>

-   Authorized User
-   Authorized User Value Unit
-   Employee User Value Unit
-   External User Value Unit

</td></tr><tr><td>

Microsoft

</td><td>

-   User CAL
-   Device CAL
-   Per Core \(with CAL\)

</td></tr><tr><td>

Oracle

</td><td>

Named User Plus

</td></tr><tr><td>

CrowdStrike

</td><td>

-   Reserved Hourly Average Sensor
-   Sensor Subscription

 **Note:** These license metrics are available with Yokohama Patch 1, Software Asset Management - SaaS License Management \(sn\_sam\_saas\_int\) 15.0.8, and Software Asset Management \(sn\_itam\_samp\) 2.1.0 version onwards. If you are on any version for Yokohama below Patch 1, refer [KB1801232](https://support.servicenow.com/kb?id=kb_article_view&sys_kb_id=ef634dac83935610cdbbc430feaad3d9).

</td></tr></tbody>
</table>License metrics are set on the [software entitlement](track-software-rights.md) form and can be accessed from the **Metric Attributes** related list on the [software model](record-terms-software-licenses.md) form.

**Important:** You can enable the Software Asset Management application to automatically create client access records for Oracle Database Server using the **Auto-generate client access for allocations** option on the corresponding software model. To use this option, you must request the Data Collection for Oracle Global Licensing and Advisory Services application from the ServiceNow Store. See [Software model fields](../reference/software-model-fields.md) for more details on the **Auto-generate client access for allocations** option. See [Request Data Collection for Oracle Global Licensing and Advisory Services \(GLAS\)](request-data-collection-oracle-glas-app.md) for more details on the Data Collection for Oracle Global Licensing and Advisory Services application.

## Procedure

1.  Navigate to **All** &gt; **Software Asset** &gt; **Administration** &gt; **Client Access** and then select **New**.

2.  On the Client Access form, fill in the fields.

<table id="table_xc3_cpd_c1b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the client access record.

</td></tr><tr><td>

Software model

</td><td>

Software model of the server that you are granting users or devices access to.

</td></tr><tr><td>

Type

</td><td>

Type of CAL that is associated with the client access record. Select one of the following options:-   **User CAL**: Licenses each user that accesses the associated server, regardless of the number of devices that each user is using to access the server.

For example, if two users are accessing Microsoft Windows Server, the corresponding software entitlement must include two User CALs.

If you select this option, you can assign the associated User CALs to specific users. See [step 3](t_AddAClientAccessRec.md#cal-type) for more details.

-   **Device CAL**: Licenses each device that accesses the specified server, regardless of the number of users that are using each device to access the server.

For example, if two devices are accessing Microsoft Windows Server, the corresponding software entitlement must include two Device CALs.

If you select this option, you can assign the associated Device CALs to specific devices. See [step 3](t_AddAClientAccessRec.md#cal-type) for more details.

-   **User/Device CAL**: Licenses each user or device that accesses the associated server.

**Note:** If you are using a Citrix software model, the User/Device CAL type is based on the user/device licenses that are assigned to your users or shared devices.

For example, if two users and two devices are accessing Microsoft Windows Server, the corresponding software entitlement must include two User CALs and two Device CALs.

If you select this option, you can assign the associated User and Device CALs to specific users and devices. See [step 3](t_AddAClientAccessRec.md#cal-type) for more details.

-   **Authorized User**: Licenses each user who accesses an IBM software product.

**Note:** This CAL type is applicable to IBM software only.

-   **Authorized User Value Unit**: Licenses the number of select users who access an IBM software product.

**Note:** This CAL type is applicable to IBM software only.

-   **Employee User Value Unit**: Licenses the total number of users within your organization who access an IBM software product.

**Note:** This CAL type is applicable to IBM software only.

-   **External User Value Unit**: Licenses the total number of users outside your organization who access an IBM software product.

**Note:** This CAL type is applicable to IBM software only.

</td></tr><tr><td>

WebLogic application**Note:** This field appears only if you select an Oracle WebLogic Server software model.

</td><td>

Oracle WebLogic Server application to which your users or devices are granted access.

</td></tr><tr><td>

Database instance**Note:** This field appears only if you select an Oracle Database Server software model.

</td><td>

Oracle database instance that accesses and manages the data in your Oracle database.

</td></tr><tr><td>

Source**Note:** This field appears only if you select an Oracle Database Server software model.

</td><td>

Source of your Oracle data. This field is automatically set to one of the following options:-   **ServiceNow**: Indicates that the client access record data was generated automatically through the SAM - Sync Auto-generated Client Access with DB Server Users scheduled job, which runs daily or on-demand.
-   **Internal**: Indicates that the client access record data was added manually.


</td></tr><tr><td>

Count

</td><td>

Number of unique users or devices that are granted access to the associated server.

 On automatically generated client access records for Oracle Database Server or Oracle WebLogic Server, this field populates automatically based on the number of users or devices that are currently added to the record. See [step 3](t_AddAClientAccessRec.md#cal-type) for more information on how to add users or devices to the client access record.

 **Note:** If you are using a Citrix software model and User/Device CAL type, the **Count** field is based on the number of user/device licenses that are assigned to your users or shared devices.

</td></tr><tr><td>

PaaS**Note:** This field appears only if you select an Oracle Database Server software model.

</td><td>

Option to indicate whether your Oracle database instance is managed by the Amazon Relational Database Service \(RDS\) on Amazon Web Services \(AWS\).

</td></tr><tr><td>

Cost Center

</td><td>

Cost center of the users or devices that are granted access to the associated server.

</td></tr><tr><td>

Department

</td><td>

Business department of the users or devices that are granted access to the associated server.

</td></tr><tr><td>

Location

</td><td>

Geographic location of the users or devices that are granted access to the associated server.

</td></tr><tr><td>

Company

</td><td>

Company of the users or devices that are granted access to the associated server.

</td></tr></tbody>
</table>3.  To assign the associated CALs to specific users or devices, add those users or devices to your client access record based on the CAL type that you selected in the **Type** field.

    By assigning CALs to specific users or devices, you can prevent those users or devices from being counted multiple times across different client access records during reconciliation.

    -   If you set the **Type** field to **User CAL**, **User/Device CAL**, **Authorized User**, **Authorized User Value Unit**, **Employee User Value Unit**, or **External User Value Unit**, add the users that you want to assign your user-based CALs to.

        **Note:** If you are using a Citrix software model and User/Device CAL type, add the users that you want to assign a user/device license to.

        1.  Select the **Users** tab.
        2.  In the **User** field of the Client Access User Breakdowns list, double-click **Insert a new row...**.

            **Note:** If you are using an Oracle Database Server software model, double-click **Insert a new row...** in the **Database user** field of the Client Access User Breakdowns list instead.

        3.  When prompted, search for and select a user that you want to assign a user-based CAL to.
        4.  Select the Save icon \(![Save icon.](../image/save-icon.png)\).

            The **Device**, **Active**, **User Type**, and **Source** fields populate automatically for the specified user. However, you can modify the **Device**, **Active**, and **User type** fields as needed.

        5.  Repeat steps b-d for each user that you want to assign a user-based CAL to.
    -   If you set the **Type** field to **Device CAL** or **User/Device CAL**, add the devices that you want to assign your device CALs to.

        **Note:** If you are using a Citrix software model and User/Device CAL type, add the devices that you want to assign a user/device license to.

        1.  Select the **Devices** tab.
        2.  In the **Device** field of the Client Access Device Breakdowns list, double-click **Insert a new row...**.
        3.  When prompted, search for and select a device that you want to assign a device CAL to.
        4.  Select the Save icon \(![Save icon.](../image/save-icon.png)\).

            The **Active** and **Source** fields populate automatically for the specified device. However, you can modify the **Active** field as needed.

        5.  Repeat steps b-d for each device that you want to assign a device CAL to.
4.  To track and license the configuration items \(CIs\) that the associated server is installed on, add them to the client access record.

    **Important:** This step is not applicable if your client access record is associated with an Oracle WebLogic Server software model or you have enabled the **License all installs accessed by clients** option on the associated software model. If this option is enabled, CIs are licensed based on conditions that you specify on the software model, such as software install conditions. See [Software model fields](../reference/software-model-fields.md) for more details on this option.

    For Windows Server, each server installation requires Per Core \(with CAL\) rights that are licensed separately from the User and Device CAL rights in associated client access records. Other products like Oracle Java do not require rights to be licensed separately for server installations. For example, if you use CALs to license the users and devices that are accessing Oracle Java, you can enable Software Asset Management to automatically mark the corresponding Oracle Java installations as licensed. In this scenario, Software Asset Management licenses the Oracle Java installations as part of CAL licensing.

    To enable this capability, you must add all CIs that a given server is installed on to the associated client access record. By specifying these CIs, you can enable Software Asset Management to determine which server installations your users and devices are connected to. After all users and devices on the client access record are licensed, all server installations on the specified CIs are marked as licensed. No additional licenses are consumed for these installations.

    1.  Select the **Devices with Installations** tab.

    2.  In the **Device** field of the Client Access Installed Devices list, double-click **Insert a new row...**.

    3.  When prompted, search for and select a CI that the associated server is installed on.

    4.  Select the Save icon \(![Save icon.](../image/save-icon.png)\).

        The **Active** field populates automatically for the specified CI. However, you can modify this field as needed.

    5.  Repeat steps b-d for each CI that the associated server is installed on.

5.  Select **Update**.


## What to do next

After you create a client access record, reconciliation runs on the associated server software as a scheduled job or on-demand. You can view your reconciliation results in the [License Workbench](../concept/sam-license-workbench.md). Use these results to determine your license compliance position and to remediate any non-compliance.

You can remediate non-compliance for your server software using the following remediation options:

-   **Purchase Rights**: Generates a purchase order when the number of rights needed is greater than the number of rights owned across all client access records for the specified server software.
-   **Create Allocations**: Allocates rights to unlicensed users or devices that have been added to the client access records for the specified server software.
-   **Remove Allocations**: Removes rights from licensed users or devices when sufficient rights are unavailable.

**Parent Topic:**[Using Software Asset Management classic](../concept/using-sam-classic.md)

