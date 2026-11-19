---
title: Element definitions and variables
description: An element definition is a configuration item that is assessed in the business impact analysis. The element definitions are also recovered in the business continuity plan. If you have the administrator role, you can set up an element variable that is required for a particular dependency of an element.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/element-definitions.html
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Explore, Business Continuity Management, Governance, Risk, and Compliance]
---

# Element definitions and variables

An element definition is a configuration item that is assessed in the business impact analysis. The element definitions are also recovered in the business continuity plan. If you have the administrator role, you can set up an element variable that is required for a particular dependency of an element.

The BCM administrator can configure the element definitions in the Business Continuity Management application. These element definitions are defined in the Business Continuity Management application:

-   Applications
-   Business Processes
-   Computer Room
-   Datacenter Zone
-   Datacenters
-   Employees
-   Linux Server
-   Locations
-   Software
-   Vendors
-   Web Server
-   Windows Server

The example shows the element definitions in an instance.

\[Omitted image "element-definitions.png"\] Alt text: Element definitions in an instance.

The example shows the configuration of an element definition by the Business Continuity Management administrator.

\[Omitted image "element-definition-new-record.png"\] Alt text: Element definition.

## Configuration of an element definition

For more information on configuring an element definition with the BCM administrator role, see [Configure element definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/configure-element-definition-bia-uib-ws.md).

**Note:** Starting with the Xanadu release, the element definition filter for the Hardware element definition has been updated. You can now add a Windows server asset in the Windows server element definition or a Linux server asset in the Linux server element definition. However, you cannot add the Windows server asset or the Linux server asset in the filter of the Hardware element definition.

## Configuration of an element variable

As a functional system administrator, you can set up an element variable that is required for a particular dependency of an element. The example shows an administrator's view of the element variable record.

\[Omitted image "new-element-variable.png"\] Alt text: Configuration of an element variable.

For more information on how to configure an element variable in the Business Continuity Management application with an administrator role, see [Configure element variables for element definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/configure-element-variable-uib-ws.md).

