---
title: Discovery with Software Asset Management
description: The table structure for managing software installations behaves differently when the Software Asset Management \(SAM\) application is activated.
locale: en-US
release: yokohama
product: ITOM Visibility
classification: itom-visibility
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Software discovery, Data collected by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Discovery with Software Asset Management

The table structure for managing software installations behaves differently when the Software Asset Management \(SAM\) application is activated.

The presence of this application affects the way Discovery stores the software installation data it returns from a scan and require additional configuration within configuration item \(CI\) records.

The following tables are created when the Software Asset Management plugin is activated:

-   Software Discovery Model \[cmdb\_sam\_sw\_discovery\_model\]
-   Software Model \[cmdb\_software\_product\_model\]
-   Software Installation \[cmdb\_sam\_sw\_install\]

    **Note:** The original schema used by previous versions is not affected when the Software Asset Management plugin is not activated.

    When it runs, Discovery populates the Software Installation \[cmdb\_sam\_sw\_install\] table. The appropriate configuration item \(CI\) references the software data. A business rule on this table runs, searching for a matching record on the Software Discovery Model \[cmdb\_sam\_sw\_discovery\_model\] table. If a record exists in the Software Discovery Model table, then the Software Installation table updates the record. If no record exists in the Software Discovery Model table, then one is created.

    These tables are not used by Discovery with Software Asset Management:

    -   Software \[cmdb\_ci\_spkg\]
    -   Software Model \[cmdb\_software\_product\_model\]
    **Important:** When SAM is installed, the Software Installation \[cmdb\_sam\_sw\_install\] table is the appropriate source for all current software data. This means you need to update any related lists or customized reference fields you added to CI records.


Starting with the Kingston release, the Discovery populates the VMWare License Key \[samp\_vmware\_license\_key\] and VMWare License Key Usage \[samp\_vmware\_license\_key\_usage\] tables. See [Data collected for VMware vCenter Server](../reference/r_VCenterDataCollected-1.md) for more information on where Discovery saves vCenter data.

-   **[Configure a CI to display Software Asset Management data](../task/configure-ci-to-display-sam-data.md)**  
Configure computer configuration item \(CI\) forms to display data from the Software Installations \[cmdb\_sam\_sw\_install\] table.

**Parent Topic:**[Software discovery](c_Software.md)

