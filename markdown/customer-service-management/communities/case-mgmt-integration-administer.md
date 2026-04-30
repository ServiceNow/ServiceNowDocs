---
title: Administer create case from discussion
description: Configure parameters for the case generated from the community discussion so that it can be routed accordingly.
locale: en-US
release: yokohama
product: Communities
classification: communities
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create a case from a discussion, Configure a community, Communities, Customer Service Management]
---

# Administer create case from discussion

Configure parameters for the case generated from the community discussion so that it can be routed accordingly.

Creating a case from a discussion requires a configuration that maps information from the question in the community to fields on the Case form. The **Create Case** configuration is included with the feature. This configuration defines the source and destination tables and maps source fields to destination fields. This configuration is stored in the CSM Table Map table \[csm\_table\_map\]. The system administrator can modify this configuration as needed.

The **Create Case** configuration uses the Social Q&amp;A Question table \[kb\_social\_qa\_question\] as the source table and the Case table \[sn\_customerservice\_case\] as the destination table. It includes the following mapping information.

|Question information|Case information|
|--------------------|----------------|
|Question|Short description|
|Question author|Contact or consumer|
|Question author's account|Account|
|Opened by|Logged in community user|
|Priority|Low \(priority = 4\)|
|Channel|Community|

To create additional mapping between these tables, add the additional fields to the **Create Case** configuration in the CSM Table Map table. Include these fields as needed on the **Create case from question** record producer.

**Parent Topic:**[Create a case from a discussion](case-management-integration.md)

