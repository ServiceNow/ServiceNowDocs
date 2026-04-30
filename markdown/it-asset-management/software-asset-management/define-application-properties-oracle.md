---
title: Set up domain-specific reconciliation properties for Oracle
description: Use domain separation application properties for Software Asset Management to set up Oracle reconciliation properties for specific domains.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Oracle reconciliation, Software Asset Management publisher pack for Oracle, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Set up domain-specific reconciliation properties for Oracle

Use domain separation application properties for Software Asset Management to set up Oracle reconciliation properties for specific domains.

## Before you begin

To set up domain separation application properties for Software Asset Management, you must activate the Domain Support - Domain Extensions Installer \(com.glide.domain.msp\_extensions.installer\) plugin on your ServiceNow instance.

Role required: sam\_admin

## About this task

Domain separation application properties are available for the Software Asset Management application. These properties correspond directly to the existing Software Asset Management properties and enable you to specify the domain that you want each property to apply to.

Domain separation is supported on the following Oracle reconciliation properties:

-   **Select the level of aggregation for reconciling licenses for Oracle databases and WebLogic servers on VMware** \(**com.snc.samp.oracle.reconlevel**\)
-   **Use host affinity for reconciling licenses for Oracle databases and WebLogic servers on VMware at the vCenter\(s\) aggregation level** \(**com.snc.samp.oracle.hostaffinityenabled**\)

For more information on the existing Software Asset Management properties, see [Software Asset Management properties](../reference/sam-properties.md). For more information on domain separation application properties, see [Domain separation application properties](https://www.servicenow.com/docs/access?context=ds-application-properties&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

## Procedure

1.  From your ServiceNow® instance, navigate to **All** &gt; **Software Asset Management** &gt; **Administration** &gt; **Application Properties**.

2.  From the list of available application properties, select the application property that you want to modify.

3.  In the Application Property Values related list, select the application property value that you want to modify.

    If you do not have any existing application property values or you want to add additional application property values, select **New**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Application Property|Name of the application property that the application property value applies to. This field populates automatically.|
    |Value|Value of the application property. This value must be equivalent to one of the available values in the corresponding Software Asset Management property. For example, you can set the value of the **com.snc.samp.oracle.reconlevel** application property to `esx`, `cluster`, or `vcenter`. See [Software Asset Management properties](../reference/sam-properties.md) for more details on the available values in the Software Asset Management properties.|
    |Domain|Domain that you want the application property value to apply to.|

5.  Depending on whether you are updating an existing application property value or adding a new application property value, select either **Update** or **Submit**.

    If you are updating an existing application property value, select **Update**. If you are adding a new application property value, select **Submit**.


**Parent Topic:**[Oracle reconciliation](../concept/oracle-recon.md)

