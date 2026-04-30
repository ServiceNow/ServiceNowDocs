---
title: Fulfillment tables
description: To enable a production instance to enforce entitled usage of your ServiceNow Store App, you configure the tables where only record owners or subscribed app users can make updates.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Anatomy of an application, Learning about developing on the ServiceNow AI Platform, Building applications]
---

# Fulfillment tables

To enable a production instance to enforce entitled usage of your ServiceNow Store App, you configure the tables where only record owners or subscribed app users can make updates.

For any table that you, the developer, create or extend to support a custom application, you can specify that the table is a fulfillment table. In a fulfillment table, only a subscribed fulfiller user can perform a fulfiller action \(typically, create/update/delete a not-own record\).

In contrast, for a table that is not a fulfillment table, any user—even a user who is not subscribed—can act as a requester. The intent is to allow the usage admin to enable subscription enforcement on any production instance that implements the application.

## Ownership of records in a fulfillment table

To enable the system to identify a fulfiller action, you define how to determine ownership of any record in the table. The developer of the application specifies the set of conditions that determine whether a user owns the record. For example, **UserA** owns a record in a task table if **UserA** opened the record or another resource opened the record on behalf of **UserA**.

For task-extended tables, time cards, and apps that require a subscription, the system sets the table as a fulfillment table by default and auto-assigns the ownership condition. For tables that you create to support your app, you can mark the table as a fulfillment table and can specify the ownership condition \(for example, use the filter **\[opened\_by\]\[is\]\[currentUser\] OR \[caller\_id\]\[is\]\[currentUser\]**\).

## System default conditions for ownership

|Action|Ownership condition \[owner\_condition\]|
|------|----------------------------------------|
|task extension|opened\_by \(read-only\)|
|catalog request|requested\_for \(read-only\)|
|other tables in apps that require a subscription|sys\_created\_by \(read-only\)|
|tables created by developer for app that requires a subscription|Specified by developer|

