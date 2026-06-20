---
title: Using scripts in a remote record producer
description: As a provider, you can perform complex tasks and gain better control over catalog requests from consumers by using various scripts such as client scripts and UI policy scripts in a remote record producer \(RRP\). Your consumers must approve all scripts to use the RRP.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/service-exchange/service-bridge-v2-add-scripts-to-rrp.html
release: yokohama
product: Service Exchange
classification: service-exchange
topic_type: concept
last_updated: "2025-01-29"
reading_time_minutes: 1
breadcrumb: [Use Service Exchange for providers, Service Exchange for Providers, Service Exchange]
---

# Using scripts in a remote record producer

As a provider, you can perform complex tasks and gain better control over catalog requests from consumers by using various scripts such as client scripts and UI policy scripts in a remote record producer \(RRP\). Your consumers must approve all scripts to use the RRP.

In Service Exchange, you can use scripts in an RRP in the following ways:

-   Creating catalog client scripts. For details, see [Create catalog client scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/service-exchange/service-bridge-v2-create-client-script.md).
-   Adding scripts in variables. For details see [Create variables for remote record producers in Service Exchange for Providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/service-exchange/service-bridge-v2-assign-variables-ser-defn.md).
-   Adding scripts in UI policies. For details, see .

**Note:** Because Service Exchange doesn’t synchronize server-side scripts such as Script Includes, client-side scripts associated with RRPs must either operate solely on the client side or rely on server-side scripts that are installed externally from Service Exchange.

