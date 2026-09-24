---
title: Administer create case from discussion
description: Configure parameters for the case generated from the community discussion so that it can be routed accordingly.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/communities/case-mgmt-integration-administer.html
release: brazil
product: Communities
classification: communities
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Create a case from a discussion, Configuring communities, Communities, Customer Service Management]
---

# Administer create case from discussion

Configure parameters for the case generated from the community discussion so that it can be routed accordingly.

**Important:**

Starting with the Brazil release, Communities is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

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

**Parent Topic:**[Create a case from a discussion](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/communities/case-management-integration.md)

