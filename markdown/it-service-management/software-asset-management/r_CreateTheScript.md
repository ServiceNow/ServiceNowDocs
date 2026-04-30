---
title: Create a custom script for a legacy Software Asset Management plugin license type
description: By default, the Script field in the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin Software License Calculation form contains information about available variables and an example script.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [License calculations with the legacy Software Asset Management plugin, Legacy Software Asset Management plugin, ITSM Software Asset Management, Asset Management, IT Service Management]
---

# Create a custom script for a legacy Software Asset Management plugin license type

By default, the **Script** field in the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin Software License Calculation form contains information about available variables and an example script.

You can use the example as the basis of the custom script or replace the example entirely.

You can use the following variables in the custom script.

|Variable|Description|
|--------|-----------|
|**found**|Contains a GlideRecord of the software install or software usage record currently being evaluated.|
|**workstation**|Contains a GlideRecord of the workstation referenced by the found record.|
|**user**|Contains a GlideRecord of the user referenced by the found record. Can be null if no user is assigned.|
|**counter\_id**|Contains the sys\_id of the counter running the script.|
|**query\_table**|Identifies the table currently being queried, either Software Installation or Software Usage.|
|**valuation**|Identifies the value in rights that is given to this software install or software usage record.|

The following functions are available as part of the SAMUtil script include and can be used in custom scripts.

**Note:** All of these functions utilize and depend on the variables mentioned above.

|Functions|Description|
|---------|-----------|
|**getWorkstationInstallsOrUsages**|Returns a list of other installs on the given workstation.|
|**getUserInstallsOrUsages**|Returns a list of all other installs belonging to the user.|
|**createCounterViolation**|Returns insert a counter violation for the current counter with the given cause.|

Example:

The following script uses the number of rights equal to the number of CPU sockets on the machine the script is installed on. The **workstation** variable is used to identify any workstation that is in the development environment. If such a workstation is found, the script then assigns a **valuation** equal to the number of CPU sockets on the machine. Otherwise, if the workstation is not in the development environment, then no rights are assigned.

![SAM custom calculation type](../image/SAMCustomCalculationType.png "SAM custom calculation type")

**Parent Topic:**[License calculations with the legacy Software Asset Management plugin](../concept/c_UseLicenseCalculations.md)

