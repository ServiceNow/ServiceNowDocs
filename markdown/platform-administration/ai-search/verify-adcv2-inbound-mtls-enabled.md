---
title: Verify whether inbound mTLS support is enabled for your instance
description: Check whether inbound mTLS support is enabled for your ServiceNow AI Platform instance. You need this feature enabled in order to run crawls for external content connectors.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-11-02"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Install, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Verify whether inbound mTLS support is enabled for your instance

Check whether inbound mTLS support is enabled for your ServiceNow AI Platform® instance. You need this feature enabled in order to run crawls for external content connectors.

## Before you begin

Role required: none

## About this task

To run crawls for external content connectors, your ServiceNow AI Platform instance must have inbound mTLS support enabled. You can check the enablement status for this feature on your instance from a web browser or the curl command-line tool.

If inbound mTLS support isn't enabled on your instance, you can open a service request case to ask Customer Service and Support to enable it for you.

## Procedure

1.  In a web browser, navigate to the `https://<instance-name>.service-now.com/adcv2/supports_tls` status page, where `<instance-name>` is the name of your ServiceNow AI Platform instance.

    You can also access this status page using the curl command-line tool, replacing `<instance-name>` with the name of your ServiceNow AI Platform instance:

    ```
    curl -k "https://<instance-name>.service-now.com/adcv2/supports_tls"
    ```

2.  Check the response from the `adcv2/supports_tls` request.


## What to do next

If the response from the `adcv2/supports_tls` request is `true`, inbound mTLS support is enabled on your instance. You don't need to do anything else.

If the response from the `adcv2/supports_tls` request is anything other than `true`, inbound mTLS support isn't enabled on your instance. Open a service request case at [https://support.servicenow.com/now](https://support.servicenow.com/now) to ask Customer Service and Support to enable inbound mTLS support on your instance.

**Parent Topic:**[Install External Content Connectors](install-ext-cont-connectors.md)

