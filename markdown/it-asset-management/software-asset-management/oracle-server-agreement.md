---
title: Oracle DB Server Deployments per Agreement report
description: You can use the Oracle DB Server Deployments per Agreement report to gain visibility into your Oracle Database server deployments across hybrid infrastructures, based on the agreement type.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Software Asset Management publisher pack for Oracle, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Oracle DB Server Deployments per Agreement report

You can use the Oracle DB Server Deployments per Agreement report to gain visibility into your Oracle Database server deployments across hybrid infrastructures, based on the agreement type.

**Note:** The Oracle DB Server Deployments per Agreement report is available only in the Software Asset Workspace. This report is not available in the Software Asset Management classic application.

To view this report, launch the Software Asset Workspace by navigating to **Workspaces** &gt; **Software Asset Workspace** on your ServiceNow instance. From the Software Asset Workspace, navigate to **License usage** &gt; **Reports** &gt; **Oracle DB Server deployments per agreement**.

|Field|Description|
|-----|-----------|
|Name|Name of the Oracle Database server deployment.|
|Product|Oracle product that is running within your deployment. This field is always set to **DB Server**.|
|Version|Oracle Database version that is installed or running on your servers.|
|Edition|Oracle Database edition that is installed or running on your servers.|
|License metric|License metric that the Oracle Database license is counted against when reconciliation runs. The options are **Named User Plus** and **Per Processor**.|
|Agreement type|Agreement type for your Oracle Database server deployment. The options are **ULA** \(Unlimited License Agreement\) and **Generic**.|
|Cloud provider|Cloud provider through which your Oracle Database servers are deployed.|
|Cloud service type|Cloud service model through which your Oracle Database servers are deployed. The options are **PaaS** and **IaaS**.|

**Parent Topic:**[Software Asset Management publisher pack for Oracle](../concept/oracle-publisher-pack.md)

