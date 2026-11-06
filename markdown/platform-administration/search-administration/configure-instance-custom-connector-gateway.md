---
title: Configure your ServiceNow AI Platform instance to support the Custom Connector Gateway
description: Configure settings in your ServiceNow AI Platform instance to satisfy the prerequisites for the Custom Connector Gateway.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-administration/search-administration/configure-instance-custom-connector-gateway.html
release: australia
product: Search Administration
classification: search-administration
topic_type: task
last_updated: "2026-09-28"
reading_time_minutes: 1
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI]
breadcrumb: [Custom Connector Gateway external content connector, Configure, External Content Connectors, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure your ServiceNow AI Platform instance to support the Custom Connector Gateway

Configure settings in your ServiceNow AI Platform instance to satisfy the prerequisites for the Custom Connector Gateway.

## Before you begin

Role required: admin

## About this task

The Custom Connector Gateway external content connector depends on a number of settings in your ServiceNow AI Platform® instance. Before you can create a Custom Connector Gateway connector, you must first configure your instance to meet all of the connector's prerequisites.

This configuration involves installing multiple plugins that are required by the Custom Connector Gateway connector.

## Procedure

1.  In Application Manager, install all of the following plugins on your instance.

    -   Code Signing framework \(com.glide.code\_signing\)
    -   Glide Hermes Message Queue \(com.glide.hermes\)
    -   ServiceNow IntegrationHub ETL Consumer - Kafka \(com.glide.hub.etl\_consumer.kafka\)
    -   ServiceNow IntegrationHub Kafka Consumer \(com.glide.hub.kafka\_consumer\)
    -   ServiceNow IntegrationHub Action Step - Kafka Producer \(com.glide.hub.action\_step.kafka\)
    -   ServiceNow IntegrationHub Flow Trigger - Kafka \(com.glide.hub.flow\_trigger.kafka\)
    -   Certificate based authentication \(com.glide.auth.mutual\)
    -   Internal Service to Service Security Standard \(com.glide.kaa\)
    -   ITOM Cloud Services Core \(sn\_itom\_cloud\_svc\)
    Some of these plugins may already be installed on your instance. You only need to install the ones that aren't installed already. For instructions on installing a plugin on your instance, see [Install an application or plugin](https://www.servicenow.com/docs/r/platform-administration/application-manager/installing-applications-in-application-manager.html).


## What to do next

With the prerequisites configured, a connector administrator can create a Custom Connector Gateway connector on your instance. For details on creating the connector, see [Create a Custom Connector Gateway external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/create-ext-cont-connector-custom-connector-gateway.md).

**Parent Topic:**[Custom Connector Gateway external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/custom-connector-gateway-external-content-connector.md)

