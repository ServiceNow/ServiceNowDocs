---
title: Configure elastic connectors for MPN health status collection
description: Configure a connector instance to collect health status data from an MPN Elastic index, and optionally customize the rules used to calculate that status.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-service-ops/telecommunications-service-operations-management/configure-mpn-rag-status-collection.html
release: brazil
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [RAG status, connector instance, MPN]
breadcrumb: [Configure Telecom Assurance, Configure, Telecommunications Service Operations Management]
---

# Configure elastic connectors for MPN health status collection

Configure a connector instance to collect health status data from an MPN Elastic index, and optionally customize the rules used to calculate that status.

## Before you begin

1.  [Create Basic Auth Credentials](https://www.servicenow.com/docs/r/it-operations-management/event-management/create-credentials-basic-auth.html)
2.  [Create HTTP\(S\) Connection](https://www.servicenow.com/docs/r/platform-security/connections-and-credentials/create-https-connection.html)

Role required: `tsom_assurance_admin`

## About this task

Health status collection lets you monitor the health of radio and core server components in your MPN so you can identify and respond to issues.

The connector instance for health status collection is created automatically but is inactive by default. Complete this procedure to activate it.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Integrations** &gt; **Connector Definitions**.

2.  Select **Nokia MPN Pull Connector**.

3.  In the Connector Instances related list, select **Nokia MPN RAG Status**.

4.  Review the **Event collection schedule** field.

    This value defaults to 60 seconds. Change it if you need a different polling interval for this instance.

5.  Customize the classification rules.

    By default, health status is calculated using a predefined rule set stored in the `nokia.rag.rules.default` system property. To override it, enter your own rule set, in the same JSON structure, in the `nokia.rag.rules.override` system property.

    **Note:**

    If the override property is empty or contains invalid data, the system uses the default rule set instead.

6.  Enable the connector instance by selecting the **Active** check box.

7.  Select **Update**.


## Result

The connector instance begins polling the configured MPN Elastic index and calculates a health status for each radio and core server component, using the active rule set.

**Parent Topic:**[Configure Telecom Assurance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-service-ops/telecommunications-service-operations-management/set-up-fault-management.md)

