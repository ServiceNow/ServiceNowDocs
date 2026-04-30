---
title: Configure third-party discovery sources for Software Asset Management
description: Set up a third-party discovery source for Software Asset Management to populate the Software Installation \[cmdb\_sam\_sw\_install\] table with software found in your environment.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Software asset connections, Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# Configure third-party discovery sources for Software Asset Management

Set up a third-party discovery source for Software Asset Management to populate the Software Installation \[cmdb\_sam\_sw\_install\] table with software found in your environment.

## Before you begin

To use the features of the Software Asset Management application with any third-party discovery source, you must populate the CMDB application and the related tables that reside on the ServiceNow instance. The Software Asset Management application uses the IRE API to help you populate the Software asset management tables. As the IRE API relies on the configuration item \(CI\) identifiers, the SAM tables require a relationship to the CI for IRE support. For more information on the IRE API, see [Identification and Reconciliation Engine](https://www.servicenow.com/docs/access?context=ire&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

Role required: sam\_developer

## Procedure

1.  Navigate to **All** &gt; **Software Asset** &gt; **Properties**.

2.  Select the **Enable scheduled jobs when using third party Datasource Integration Framework** \[com.snc.samp.ire.datasource.integration\] property.

3.  Run your discovery source to identify software on the CIs.

    The CI is used to construct a payload.

4.  Send the payload to the ServiceNow instance using the IRE REST API.

    For information on a sample payload, see [Sample payload for generic software install records](../reference/payload-details.md).

    In the payload, make sure to send the sys\_class\_name of the CI, so that the CI is not reclassified when an insert or update operation is performed.

    An entry is created in the Software Installation \[cmdb\_sam\_sw\_install\] table with a display name, publisher, and version. Reconciliation is run against the content service and a discovery model is identified for that software. If a discovery model does not exist, a discovery model is automatically created for the software. You can start using the Software Asset Management application.


**Parent Topic:**[Software asset connections](../concept/third-party-discovery-sam.md)

