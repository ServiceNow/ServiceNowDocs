---
title: Configuring the phone PIN settings for ServiceNow Voice
description: Use a  PIN-based authentication mechanism for enabling a customer contact or consumer to connect with the ServiceNow Voice for CSM  application. 
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Integrating ServiceNow Voice with CSM, Integrating Voice with other applications, ServiceNow Voice, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configuring the phone PIN settings for ServiceNow Voice

Use a  PIN-based authentication mechanism for enabling a customer contact or consumer to connect with the ServiceNow Voice for CSM  application. 

An authentication mechanism for inbound  dialing  enables protecting the details of  customer contacts and consumers from unauthorized users. When using the  ServiceNow Voice for CSM application, you as an administrator can configure the PIN-based authentication mechanism available within the  ServiceNow Voice for CSM application or set up a custom authentication mechanism.

The PIN-based authentication mechanism available within the  ServiceNow Voice for CSM application enables  customer contacts  and  consumers  to use a custom phone PIN for accessing details related to their customer service cases during inbound  dialing.

By default, the  **My Phone PIN**  link in the Additional Configuration section of the setup guide for configuring the Amazon Connect components enables the PIN-based authentication mechanism. For more information about the setup guide, see [Integrate ServiceNow Voice with Amazon Connect](../task/integrate-ccc-amazonconnect.md) .

**Note:** The **My Phone PIN** link for customer contacts and consumers is available only with the sample CSM -specific contact flows.

To enable a PIN-based authentication mechanism, the  **My Phone PIN**  link in the setup guide uses the predefined  Setup PIN  record producer that is configured by default for consumers and customer contacts. As an administrator, you can edit the Setup PIN  record producer to add any additional  ServiceNow roles, include the record producer in a service  catalog, and display the service  catalog  as a module on a customer-facing portal. Customers can then use the module to configure and reset their phone PIN. For more information, see [Record Producer](../../service-catalog-management/concept/c_RecordProducer.md) and [Set up a service catalog](../../service-catalog-management/task/t_SetUpAServiceCatalog.md) . 

**Parent Topic:**[Integrating ServiceNow Voice with CSM](integrating-ccc-csm.md)

