---
title: Create an applicative credential alias for NSX-T cluster discovery
description: Create a credential alias and configure an applicative credential to enable the NSX Cluster pattern to authenticate with the NSX-T management cluster.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/discovery-and-service-mapping-patterns/create-applicative-cred-alias-nsx-t.html
release: zurich
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: task
last_updated: "2026-05-03"
reading_time_minutes: 1
breadcrumb: [VMware NSX-T cluster, Available on-premise discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Create an applicative credential alias for NSX-T cluster discovery

Create a credential alias and configure an applicative credential to enable the NSX Cluster pattern to authenticate with the NSX-T management cluster.

## Before you begin

Role required: discovery\_admin

## About this task

The NSX Cluster pattern requires a credential alias that contains exactly one applicative credential record.

## Procedure

1.  Create an alias.

    1.  Navigate to **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

    2.  Select **New**.

    3.  Enter a unique name for the alias and select **Credential** for the alias type in the **Type** field.

    4.  Select **Submit**.

2.  Configure an applicative credential for the alias.

    1.  Navigate to **Discovery** &gt; **Credentials**.

    2.  Select **New**.

    3.  Select **Applicative Credentials**.

    4.  Fill in the fields.

        |Field|Value|
        |-----|-----|
        |Name|Descriptive name for the credential. For example: NSX-T admin.|
        |User name|NSX-T user name with permissions to execute the required API calls.|
        |Password|Password for the NSX-T user.|
        |CI type|Cluster \[cmdb\_ci\_cluster\].|

    5.  Unlock the **Credential alias** field and select the alias you created.

    6.  Select **Submit**.


## What to do next

Create a serverless discovery schedule for the NSX Cluster pattern. For more information, see [Create a serverless schedule for NSX-T cluster discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/create-serverless-schedule-nsx-t.md).

**Parent Topic:**[VMware NSX-T cluster pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/nsx-t-cluster-pattern.md)

