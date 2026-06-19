---
title: Integrate CIM using extension point
description: Integrate CIM with other applications by using the CIMIntegrationAPI extension point. It defines the inbound and outbound extension points for integrating CIM with other applications.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/continual-improvement-management/integrate-extension-api.html
release: zurich
product: Continual Improvement Management
classification: continual-improvement-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Overview, Continual Improvement Management, IT Service Management]
---

# Integrate CIM using extension point

Integrate CIM with other applications by using the CIMIntegrationAPI extension point. It defines the inbound and outbound extension points for integrating CIM with other applications.

## Before you begin

Role required: admin or sn\_cim.improvement\_manager

## About this task

The CIMIntegrationAPI defines the inbound and outbound extension points for integrating CIM with other applications. Inbound integrations enable you to create improvement initiatives from integrated applications. Outbound integrations enable you to create application records from improvement initiatives or CIM tasks.

## Procedure

1.  Navigate to **All** and enter `sys_extension_point.list` in the search field.

2.  In the Extension Points context menu, type `CIMIntegrationAPI` in the search field.

3.  Select **sn\_cim.CIMIntegrationAPI**.

4.  Select **Create Implementation** under Related Links.

    A new instance of the CIMIntegrationAPI is created.

5.  Enter a name for the new API instance.

6.  Save the record.

7.  In the **Script** field, edit the inbound or outbound integrations.

    -   For inbound integrations, add application names in the **var tables** parameter of the getInboundIntegrationTables function.
    -   For outbound integrations, add application names in the **var tables** parameter of the getOutboundIntegrationTables function.
    Enclose the values in single quotation marks and use commas to separate multiple values.

    The following example shows integrating improvement initiatives from change requests with CIM by editing the inbound extension point of CIMIntegrationAPI.\[Omitted image "cim-inbound-eg.png"\] Alt text: Inbound integration of change requests using the CIMIntegrationAPI extension point

8.  Save and update the record.

    For inbound integrations, the **Create Improvement Initiative** related link is added to records of applications integrated with CIM.

9.  For outbound integrations, configure related links on CIM task records to integrated applications.

    For more information, see .


**Parent Topic:**[Continual Improvement Management overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/continual-improvement-management/get-started-cim.md)

