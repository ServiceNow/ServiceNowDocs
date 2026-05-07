---
title: Add a custom implementation for device classification
description: Customize the base system classification of an device based on the type, os\_version, and firmware\_version.
locale: en-US
release: australia
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring the Service Graph Connector for Microsoft Excel, Service Graph Connector for Microsoft Excel, Use, Operational Technology Manager, Operational Technology]
---

# Add a custom implementation for device classification

Customize the base system classification of an device based on the type, os\_version, and firmware\_version.

## Before you begin

The base system for the **sn\_otsm\_sgc.SGOTAssetImportExtensionPoint** extension point uses the default implementation script that is shipped with the name of **sn\_otsm\_sgc.SGOTAssetImportUtil**. To add a customized classification, create an implementation for the extension point in the **Service Graph Connector for Operational Technology \(Excel\)** scope.

**Note:** User must have only one implementation of the extension point. If you implement and activate a custom extension point rather than the default one, you must deactivate the default implementation.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Extension Point** &gt; **Scripted Extension points**.

2.  Select **sn\_otsm\_sgc.SGOTAssetImportExtensionPoint**.

3.  Select the **Create Implementation** related link.

4.  Enter a name for the extension point implementation.

5.  In the script field, check that the class object with the following two functions is populated.

    Make sure that the result returned from the **getAssetCMDBSysClassNameWithOtEntityTypeSysId** extension point follows the format mentioned in the comments. Any change in the result string format results in import failure or irregularities. The format should be &lt;cmdb class name&gt;:::&lt;ot entity type sys id&gt;.

<table id="choicetable_thp_13x_drb"><tbody><tr><td id="d80862e121">

**getAssetCMDBSysClassNameWithOtEntityTypeSysId\(/\*string\*/ type, /\*string\*/ osVersion, /\*string\*/ firmwareVersion\)**

</td><td>

Implement this method to return the CMDB sys class name that the device belongs to, along with the OT Entity type sys\_id concatenated with “:::”.For unclassified devices, the OT device type is set to ot\_base.

</td></tr><tr><td id="d80862e135">

**getComputerType\(\(/\*string\*/ operatingSystem\)**

</td><td>

Returns the CMDB sys class name based on the operating system passed.

</td></tr></tbody>
</table>6.  After you make all the desired changes, select **Update**.

    The implementation for the extension point is created.


## What to do next

From the related lists Implementations tab, open the base system extension point implementation to inactivate it.

**Parent Topic:**[Configuring the Service Graph Connector for Microsoft Excel](../concept/configuring-service-graph-connector-for-excel.md)

