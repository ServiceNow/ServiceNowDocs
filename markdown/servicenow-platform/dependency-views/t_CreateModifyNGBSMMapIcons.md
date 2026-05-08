---
title: Create or modify map icons
description: Upload new icons or modify existing icons to customize the icon displayed for a CI in maps in Dependency Views, Service Mapping, and Event Management.
locale: en-US
release: australia
product: Dependency Views
classification: dependency-views
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Administer, Dependency Views, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Create or modify map icons

Upload new icons or modify existing icons to customize the icon displayed for a CI in maps in Dependency Views, Service Mapping, and Event Management.

## Before you begin

Role required: sn\_cmdb\_admin or admin

## About this task

The icons used in Dependency Views maps are listed in the Map Icons module. Records in the **Map Icons** list are arranged by CI classes, such as cmdb\_ci\_linux\_server. The path to the default image files is https://&lt;instance name&gt;.service-now.com/images/app.ngbsm/&lt;image name.svg&gt;. For information about uploading images to the database, see Storing images in the database.

Role required: admin or cmdb\_admin roles are required to access the records in this table \[ngbsm\_icon\] to upload new icons.

## Procedure

-   Navigate to **All** &gt; **Configuration** &gt; **CI Class Manager**, and do the following actions:

    1.  Click **Hierarchy** to display the CI Classes list.

    2.  Select a class to modify the icon for.

    3.  In the class navigator bar, expand **Class Info** and then select **Basic Info**.

    4.  On the Basic Info form, click **Icon**.

    5.  In the Icons dialog box, select an icon and then click **Update**.

    6.  On the **Basic Info** form, click **Update**.

-   Navigate to **All** &gt; **Dependency Views** &gt; **Map Icons**, and do the following actions:

    1.  Click **New** to create a new map icon or click the name of an existing icon in the **Label** column to modify an existing icon.

    2.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |CI Type|Label or the informal name of the CI table that this icon represents in the view.|
        |Icon|Name of the icon.|
        |URL|Path to the icon image using the following format: `/*image name*.svg` Click the lock icon to enter a new path.|

    3.  Fill in the fields on the form, as appropriate.

    4.  Click **Submit** to enter a new icon or click **Update** to modify an existing icon.


## What to do next

You can modify a Dependency Views map indicator to use the new icon.

**Parent Topic:**[Administer Dependency Views](../topic/p_AdministerNGBSM.md)

**Related topics**  


[Create or modify map indicators](t_CreateModifyNGBSMMapIndicators.md)

[Create a predefined filter](create-predefined-filter.md)

[Set a predefined filter as default](set-predefined-filter-default.md)

[Create or modify Map Related Items](t_CreateModifyNGBSMMapRelatedItems.md)

[Create or modify Dependency Views menu actions](t_CreateModifyNGBSMMenuActions.md)

[Condition and script parameters for menu actions](../reference/condition-script-parameters.md)

[Create or edit a dependency type](t_CreateMapScript.md)

