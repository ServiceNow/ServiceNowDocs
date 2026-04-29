---
title: Add images to a network inventory record
description: Add image to a network inventory record. You can distinguish the network asset with the uploaded image.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Geo map, Network visualization view, Use, Telecommunications Network Inventory]
---

# Add images to a network inventory record

Add image to a network inventory record. You can distinguish the network asset with the uploaded image.

## Before you begin

Role required: sn\_ni\_core.inventory\_admin, sn\_ni\_core.inventory\_agent, sn\_ni\_core.inventory\_template\_manager, sn\_ni\_core.telco\_inventory\_catalog\_manager

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the list icon \(![List icon.](../image/ni-workspace-list-icon.png)\) and then go to **Network Sites** &gt; **All Sites**.

    You can select the type of inventory that you want to add an image.

3.  Open the record that you want to add image.

4.  On the **Media** tab, select **New**.

5.  On the **Details** tab, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Image name.|
    |Record Table|Table name where you want to upload the image. For example, if you add an image to a network site, select **Network Site** \(cmdb\_ci\_ni\_site\).|
    |Acquisition Date|The date on which the network resource legally acquired by the organization.|
    |State|Current state of the image. Select **Active** to display the image in the inventory record.|
    |Media Type|Type of media file.|
    |Description|Brief description about the image.|
    |Default|Select this check box to display the image on the inventory record.|
    |Acquired by|Name the person who acquired this image.|
    |Record ID|Inventory record.|
    |Image|Select **Add Image** to upload the file.|
    |View Type|Select the view type if you upload multiple images.|
    |Sequence|Select sequence if you upload multiple images.|

6.  Select **Save**.


## Result

The image is added to the network inventory record.

**Parent Topic:**[Geo map](../concept/using-network-site-map.md)

**Related topics**  


[View details of the geo map](view-details-network-site-map.md)

