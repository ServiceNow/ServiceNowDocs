---
title: Recall campaign tables
description: This section explains the recall campaign tables in Manufacturing Commercial Operations.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Recall campaign data model, Data model, Reference, Manufacturing Commercial Operations]
---

# Recall campaign tables

This section explains the recall campaign tables in Manufacturing Commercial Operations.

## Recall claim plugin

The recall claim feature adds or modifies the existing tables:

-   Planning Item \[sn\_align\_core\_planning\_item\]
-   Task \[sn\_customerservice\_task\]
-   Service Organization Criteria

The recall claim plugin adds the following tables.

<table id="table_sxb_p4l_jfc"><thead><tr><th>

Label

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Recall Campaign\[sn\_rcl\_claim\_mgmt\_rcp\]

</td><td>

It’s the parent table and stores the Recall campaign initiative information.

</td></tr><tr><td>

Recall Campaign Task\[sn\_rcl\_claim\_mgmt\_campaign\_task\]

</td><td>

Stores the task information that must be fulfilled to complete the Recall Campaign process.

</td></tr><tr><td>

Recall Campaign Phase\[sn\_rcl\_claim\_mgmt\_rcp\_phase\]

</td><td>

Stores the information related to the launch of the recall campaign.

</td></tr><tr><td>

Impacted Finished Goods\[sn\_rcl\_claim\_mgmt\_finished\_good\]

</td><td>

Stores the asset information for all the assets impacted by a recall campaign.

</td></tr><tr><td>

Corrective Action\[sn\_rcl\_claim\_mgmt\_ca\]

</td><td>

Stores the remedy procedures to resolve the issues mentioned as part of recall campaign record.

</td></tr><tr><td>

Recall Campaign Phase Task\[sn\_rcl\_claim\_mgmt\_phase\_task\]

</td><td>

Stores the tasks related to a recall Campaign phase.

</td></tr><tr><td>

Corrective Action Labor Charges\[sn\_rcl\_claim\_mgmt\_ca\_labor\_charges\]

</td><td>

Stores the detail of different types of charges to perform the remedy procedures.

</td></tr><tr><td>

Planning Item \[sn\_align\_core\_planning\_item\]

</td><td>

Stores the new item details.

</td></tr><tr><td>

Recall campaign part requirement\[sn\_rcl\_claim\_mgmt\_rcp\_part\_requirement\]

</td><td>

 

</td></tr><tr><td>

Recall campaign part availability\[sn\_rcl\_claim\_mgmt\_rcp\_part\_availability\]

</td><td>

 

</td></tr><tr><td>

Recall phase part allocation\[sn\_rcl\_claim\_mgmt\_phase\_part\_allocation\]

</td><td>

 

</td></tr></tbody>
</table>**Parent Topic:**[Recall campaign data model](recall-claims.md)

