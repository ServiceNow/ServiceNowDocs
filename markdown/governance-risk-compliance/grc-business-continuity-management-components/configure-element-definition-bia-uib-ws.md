---
title: Configure element definition
description: Configure element definitions to identify the configuration item that has to be assessed in a business impact analysis and recovered in a business continuity plan. Use the Element Definitions module in the Business Continuity Management application navigator to configure an element definition.
locale: en-US
release: xanadu
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [General administration setup for BCM, Configure, Business Continuity Management, Governance, Risk, and Compliance]
---

# Configure element definition

Configure element definitions to identify the configuration item that has to be assessed in a business impact analysis and recovered in a business continuity plan. Use the **Element Definitions** module in the Business Continuity Management application navigator to configure an element definition.

## Before you begin

Role required: sn\_bcm.admin

## About this task

Avoid creating overlapping element definitions where one asset could fit into multiple categories. Each element definition should be unique and not overlap with another. For instance, do not define both server and Linux server as separate element definitions since a Linux server is inherently a server. The BCM application is structured to use only one of these definitions, not both, ensuring that an element definition appears in only one category.

If you want to define Server and Linux Server as distinct element definitions without an overlap, apply a filter to the Server element definition specifying that the class is not Linux. This approach maintains mutual exclusivity between the two definitions.

If you select the Servers asset type as shown in the example and select **Add**, the configuration shows all the servers including Solaris, ESX, Windows, and so on.

![Server type.](../image/ele-def-server-type.png)

If you define the server element as a generic bucket, you can select any of the server types as shown in the example. The Servers asset type has a Linux server as a child item. However, a separate asset type called as Linux server is available in the Asset types list.

![Servers list.](../image/ele-def-servers-allocation.png)

In the list, the asset types are calculated and shown as 2 Linux servers and 4 Servers where one item is a Linux server. It is possible that after the refresh or after reloading the assets, the asset types are recalculated and shown differently. For example, the system may show the asset types as 3 Linux servers and 3 Servers or 0 Linux servers and 6 Servers. The asset types are calculated differently because the element definition of Server also includes the Linux server.

In such scenarios, configuring rules that overlap with other rules may lead to an error. As a workaround, the list items should be configured as mutually exclusive and the filter condition should be configured appropriately as shown in the examples.

![Linux Server.](../image/ele-def-linux-server.png)

In this scenario, the Servers is the parent table and the Linux server is the child table. In the Servers table \(record\), configure a filter condition where the class is not Linux Server by choosing the **Class is not Linux Server** option.

![Class is not Linux Server.](../image/ele-def-class-not-linux-server.png)![Server filter condition.](../image/ele-def-list-server-filter-condition.png)

It means that the Servers element definition includes all servers except the Linux server.

Starting with the Xanadu release, the element definition filter for the Hardware element definition has been updated. You cannot add a Windows server asset or a Linux server asset under the Hardware element as shown in the example.

![Hardware element definition.](../image/ele-def-hardware.png)

However, you can now add a Windows server asset in the Windows Server element definition or a Linux server asset in the Linux Server element definition as shown in the examples.

![Linux server element definition.](../image/ele-def-linux-server-for-hardware.png)![Windows server element definition.](../image/ele-def-windows-server-for-hardware.png)

## Procedure

1.  Navigate to **Business Continuity** &gt; **General Administration** &gt; **Element Definitions**.

2.  Select **New**.

    The example shows the Element Definition record.

    ![Element definition.](../image/element-definition-new-record.png)

    **Note:** The filter condition in the Element definition is used to add specific configuration items \(CIs\) via the pop-up. The **Update dependencies** UI action also considers the element definition's filter and retrieves the related CIs of the configuration item listed in the **Applies to** field of the BIA. These relationships are retrieved from the CI Relationships table.

3.  On the form, fill in the fields.

    For more information on the fields in the form, see [Element definition record form](../reference/element-definition-record-form.md).

4.  Select **Submit**.


-   **[Element definition record form](../reference/element-definition-record-form.md)**  
Use the Element definition record form to configure a recovery tier with a set of business applications by using BCM UIB Workspace.

**Parent Topic:**[General administration setup for BCM](../concept/set-up-bcm-bcmadmin-tasks.md)

