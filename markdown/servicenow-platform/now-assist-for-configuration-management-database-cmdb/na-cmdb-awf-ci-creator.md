---
title: Create a CI using Now Assist
description: The Create configuration item agentic workflow accepts your natural language request to manually generate a valid CI in the class that you specify.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-awf-ci-creator.html
release: zurich
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: task
last_updated: "2025-10-17"
reading_time_minutes: 1
breadcrumb: [Use agentic workflows, Now Assist for Configuration Management Database \(CMDB\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Create a CI using Now Assist

The Create configuration item agentic workflow accepts your natural language request to manually generate a valid CI in the class that you specify.

## Before you begin

Role required:

-   Now Assist for CMDB v2.4 and earlier: sn\_cmdb\_editor
-   Starting with Now Assist for CMDB v2.5: sn\_cmdb\_admin
-   Starting with Now Assist for CMDB v3.0: sn\_cmdb\_editor

## About this task

Occasionally, you might create a CI manually. To help you, the Create configuration item agentic workflow accepts your natural language request and verifies that it understands which class the new CI should belong to. The workflow then checks Identification and Reconciliation engine \(IRE\) rules to determine the required attributes for the CI and requests that information. After you provide sufficient data, the workflow ensures that the proposed CI includes the attributes that you requested, complies with IRE rules, and is not a duplicate. The workflow then creates the CI.

The Create configuration item agentic workflow is particularly useful for adding CIs to tables accessed by Operational Technology because users might add physical CIs while unaware of the importance of managing CI data in the CMDB.

**Note:** The workflow prevents creation of a CI whose class does not have an identification rule. For more information, see [Identification rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/c_IdentificationRules.md).

To learn more about using the Now Assist panel, see [Working in the Now Assist panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/enable-ai-experiences/now-assist-panel-overview.md).

## Procedure

1.  Use either of the following methods to start the process.

    -   While working in the CMDB Workspace, select **Create CI** in the Quick Links section.
    -   While working in the CMDB Workspace, select the Now Assist icon \[Omitted image "ai-sparkle-cmdb.png"\] and then enter `create a ci`.
2.  Enter the class of CI to create and then continue by answering the Now Assist questions.


**Parent Topic:**[Using agentic workflows in Now Assist for CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/now-assist-for-configuration-management-database-cmdb/now-assist-cmdb-using.md)

