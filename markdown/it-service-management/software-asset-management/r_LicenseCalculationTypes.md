---
title: License calculation types supported by the legacy Software Asset Management plugin
description: Default license calculation types are available with the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [License calculations with the legacy Software Asset Management plugin, Legacy Software Asset Management plugin, ITSM Software Asset Management, Asset Management, IT Service Management]
---

# License calculation types supported by the legacy Software Asset Management plugin

Default license calculation types are available with the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin.

These license types cannot be deleted.

<table id="table_tys_4nd_xq"><thead><tr><th>

Category

</th><th>

License type

</th></tr></thead><tbody><tr><td>

By CPU

</td><td>

-   **By CPU cores**: The counter adds up the total license rights for all software license records of this model. The **CPU Core Count** field on the hardware configuration item determines the number of rights consumed by any software installation located on the configuration item. For that installation, the counter checks for a valid entitlement record on any of the software license records. Applies to software installation data and hardware configuration items.
-   **By number of CPUs**: The counter adds up the total license rights for all software license records of this model. The **CPU Count field** on the hardware configuration item determines the number of rights consumed by any software installation located on the configuration item. For that installation, the counter checks for a valid entitlement record on any of the software license records. Applies to software installation data and hardware configuration items.

</td></tr><tr><td>

By number of points

</td><td>

**Per installation - IBM PVU**: The counter adds up the total license rights for all software license records of this model. The installation count for every hardware configuration item that has IBM PVU software is a point calculation. The CPU type determines the PVU per-core multiplier based on the IBM PVU mapping table. The total number of cores on the configuration item is multiplied with this per-core multiplier to determine how many rights are used by an installation on this configuration item. For that installation, the counter checks for a valid entitlement record on any of the software license records. Applies to software installation data and hardware configuration items.

 This license type is present but does not work until the Software Asset Management plugin [IBM PVU Process Pack](../concept/c_IBMPVUProcessPack.md) is active.

</td></tr><tr><td>

By Client Access License \(CAL\)

</td><td>

-   **CAL \(Device\)**: The counter adds up the total license rights for all software license records of this model. Usage is counted as one installation for every unique configuration item \(device\). For each installation, the counter checks for a valid entitlement record on any of the software license records. The Software Usage \[ast\_usage\] table is used for counting.
-   **CAL \(User\)**: The counter adds up the total license rights for all software license records of this model. Usage is counted as one installation for every unique user. For that installation, the counter checks for a valid entitlement record on any of the software license records. The Software Usage \[ast\_usage\] table is used for counting.

</td></tr><tr><td>

By user

</td><td>

-   **Number of installs per user**: The counter adds up the total license rights for all software license records of this model. It counts an installation when one software installation matches the discovery models that are mapped to this software model for any hardware used by a user. It counts up to the specified amount. For that installation, the counter checks for a valid entitlement record on any of the software license records. Applies to software installation data and hardware configuration items.
-   **Per named user**: The counter adds up the total license rights for all software license records of this model. It counts an installation when there is at least one software installation that matches the discovery models that are mapped to this software model for any hardware used by a unique user. For that installation, the counter checks for a valid entitlement record on any of the software license records. Applies to software installation data and hardware configuration items.
-   **No license needed \(User\)**: The counter adds up the total number of users of this model. It counts an installation when there is at least one software installation that matches the discovery models that are mapped to this software model for any hardware used by a unique user. It applies to software installation data and hardware configuration items. This license type is used for software installations where no license is required, such as open source applications.

 To compare **Number of installs per user** and **Per named user**:

-   **Number of installs per user** counts the number of installs the user has and assigns license cost based on installs per license. For example, UserA has three installs. One license is used by each install, for a total of three licenses.
-   For **Per named user**, there is no install limit for a particular user. For example, UserB, who has three installs, needs only one license for the three installs.

</td></tr><tr><td>

By utilization

</td><td>

-   **Usage \(CPU\)**: The counter adds up the total license rights for all software license records of this model. The counter looks at all of the software usage data mapped to any of the discovery model records of the counter's software model. It counts one installation for every unique configuration item. For that installation, the counter checks for a valid entitlement record on any of the software license records. Applies to software usage data.
-   **Usage \(User\)**: The counter adds up the total license rights for all software license records of this model. The counter looks at all of the software usage data mapped to any of the discovery model records of the counter's software model. It counts one installation for every unique user Accessed From hardware configuration item. For that installation, the counter checks for a valid entitlement record on any of the software license records. Applies to software usage data.

</td></tr><tr><td>

By workstation

</td><td>

-   **Per workstation**: The counter adds up the total number of license rights for all software license records of this model. It counts an installation when there is at least one software installation on a hardware configuration item that matches the discovery models that are mapped to this software model. For each installation, the counter checks for a valid entitlement record on any of the software license records. Applies to software installation data and hardware configuration items.
-   **No license needed \(Workstation\)**This license type is used for software installations where no license is required, such as open source applications.

</td></tr><tr><td>

By Oracle install

</td><td>

-   **Oracle Named User**: Oracle licensing scheme that counts by the number of unique users.
-   **Oracle Named User Plus**: Oracle licensing scheme that counts by the number of unique users and accounts.
-   **Oracle Processor**: Oracle licensing scheme that counts by the number of processors on a server.

 This category and its license types are available when the Oracle Process Pack is activated.

</td></tr></tbody>
</table>**Parent Topic:**[License calculations with the legacy Software Asset Management plugin](../concept/c_UseLicenseCalculations.md)

