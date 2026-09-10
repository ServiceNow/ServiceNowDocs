---
title: Configure the Party Relationship Center
description: Configure node settings to control which fields appear on the entity node cards in the Party Relationship Center.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-media-technology/c360-configure-prc.html
release: australia
topic_type: task
last_updated: "2026-09-01"
reading_time_minutes: 2
keywords: [party relationship centre, configure PRC, node settings, PRC configuration]
breadcrumb: [Configure, Telecommunications Customer 360, Telecommunications, Media, and Technology \(TMT\)]
---

# Configure the Party Relationship Center

Configure node settings to control which fields appear on the entity node cards in the Party Relationship Center.

## Before you begin

-   Role required: `sn_telecom_c360.admin`
-   Telco GenAI \(`sn_telco_genai`\) must be installed. The Telecom Customer Enterprise Graph, which drives entity traversal in the node map, ships with Telco GenAI.

## About this task

The Party Relationship Center uses the following configuration tables:

-   **Node model**

    The top-level template. The base system ships one record: the generic node model. It acts as a bridge between variables and settings.

-   **Node variable**

    Defines the display attributes available to node settings — for example, header, subheader, status field, and contextual side panel properties. Variables belong to a node model. The base system ships four variables for the generic node model. Add a variable here only if you need a display attribute that does not already exist.

-   **Node setting**

    Binds a context table \(the entity's source table\) to the variables and specifies the field value for each variable. Each entity type in the node map has one node setting record. The base system ships node setting records for all entities in the base system relationship network. To change what a node displays, modify the relevant node setting record.


## Procedure

1.  Navigate to **All** &gt; ****.

2.  Open the generic node model record.

    The base system ships one node model record. Variables and node settings for all entity types are accessible from the related lists on this record.

3.  In the **Node Settings** related list, open the node setting record for the entity type you want to configure.

    The base system ships node setting records for the following entities: consumer, account, billing account, billing account related party, sold product, and service problem case. To add a node setting for a new entity type, select **New** in the related list.

4.  In the **Context table** field, confirm or select the source table for this entity type.

5.  Set the field value for each display variable.

    The fields available for selection depend on the context table. Only fields from the context table are shown.

    |Variable|Description|
    |--------|-----------|
    |Header|The primary field displayed on the node card. Used as a search target when an agent searches the node map.|
    |Subheader|The secondary field displayed on the node card. Also used as a search target.|
    |Status field|A value displayed prominently on the node card to indicate the entity's current state.|
    |Contextual side panel properties|Fields shown in the side panel when a node is selected. Any field from the context table can be added.|

6.  If you are adding a new node setting, enter a value in the **Order** field to set its priority relative to other node settings for the same context table.

    Higher order values take precedence. To override a base system node setting, use a higher order value than the base system record.

7.  Confirm that the **Active** check box is selected.

8.  Select **Update** to save changes to an existing record, or **Submit** to save a new record.


## Result

The node setting is saved and is used for the matching entity type and displays the specified field values on the node card and the contextual side panel.

**Parent Topic:**[Configure Telecommunications Customer 360](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/c360-configure.md)

**Related topics**  


[Party Relationship Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/c360-prc-overview.md)

