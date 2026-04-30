---
title: Set up the Oracle HCM Cloud spoke
description: Set up the Oracle HCM spoke to integrate your ServiceNow instance with the Oracle REST APIs.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Oracle HCM Cloud Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Oracle HCM Cloud spoke

Set up the Oracle HCM spoke to integrate your ServiceNow instance with the Oracle REST APIs.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Oracle HCM Cloud spoke.
-   Access to the Oracle HCM tenant site.
-   Ensure that OpenSSL is installed on your machine.
-   Role required: admin.

## About this task

Oracle REST APIs mandate a JWT authentication of requests that your ServiceNow instance makes. To set up your Oracle HCM Cloud spoke, you must enable your ServiceNow instance to handle JWT authentication, configure the connection record, and add the roles necessary to execute the Oracle HCM Cloud spoke actions.

