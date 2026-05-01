---
title: Roles and components of Segment Management
description: The Segment Management application uses roles to provide access to information, identify internal and external users, maintain data security, and establish different types of relationships between segments and partners.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-05-01"
reading_time_minutes: 1
breadcrumb: [Configure Segment Management, Partner Relationship Management, Configure, Sales Customer Relationship Management]
---

# Roles and components of Segment Management

The Segment Management application uses roles to provide access to information, identify internal and external users, maintain data security, and establish different types of relationships between segments and partners.

The Segment Management plugin \(com.snc.segment\_mgmt\) comes with a set of functional roles, each with varying levels of access to segments and records.

## Functional and granular roles

Functional roles help provide authorized partners to maintain data and records in the segment table. A granular model helps to protect data by granting the required level of access to the relevant enterprise or channel partner entities. With this functionality, each role is associated with a set of privileges that determine users’ access to certain information.

You can assign granular policies that authorize individuals to do their jobs efficiently and effectively, which helps to improve customer experience.

## Roles and descriptions

Functional roles are a set of granular roles that are required to perform a function that requires access to multiple entities. The segment management application uses the segment admin \(sn\_seg.segment\_mgmt\_admin\) role to configure and maintain segment data in the segment \(sn\_seg\_segment\) table. The segment admin \(sn\_seg.segment\_mgmt\_admin\) contains the following roles.

-   Segment writer \(sn\_Seg.segment\_mgmt\_writer\)
-   Segment data viewer \(sn\_seg.segment\_mgmt\_data\_viewer\)

The following table lists the granular roles installed with Segment management.

|Role|Description|Inherited roles|
|----|-----------|---------------|
|Segment data viewer \(sn\_seg.segment\_mgmt\_data\_viewer\)|This role provides granular read access to segment data.|None|
|Segment writer \(sn\_seg.segment\_mgmt\_writer\)|This role provides granular read, edit, and write access to segment data.|Segment data viewer \(sn\_seg.segment\_mgmt\_data\_viewer\)|

## System properties

Navigate to **All** &gt; **Partner Relationship Management** &gt; **Properties**.

The Segment admin \(sn\_seg.segment\_mgmt\_admin\) hasread and write access for the \[glide.ui.sn\_seg\_segment\_activity.fields\] property.

**Parent Topic:**[Configure Segment Management](configure-segment-management.md)

**Related topics**  


[Configure Segment Management](configure-segment-management.md)

[Data model for Segment Management](data-model-for-segment-management.md)

