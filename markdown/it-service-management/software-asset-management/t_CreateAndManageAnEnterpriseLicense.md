---
title: Create and manage an enterprise license using the legacy Software Asset Management plugin
description: Enterprise licenses are typically for large customers and provide some flexibility, an agreed upon discount price, and a mechanism for easy administration.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Software licenses in the legacy Software Asset Management plugin, Legacy Software Asset Management plugin, ITSM Software Asset Management, Asset Management, IT Service Management]
---

# Create and manage an enterprise license using the legacy Software Asset Management plugin

Enterprise licenses are typically for large customers and provide some flexibility, an agreed upon discount price, and a mechanism for easy administration.

## Before you begin

Role required: contract\_manager

## About this task

Use the Contract Management application to set a software license as enterprise or subscription for the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin.

## Procedure

1.  Navigate to **All** &gt; **Contract** &gt; **Software Licenses**.

2.  Click **New**.

3.  Select a **License type** of **Enterprise**.

4.  Fill in as many of the remaining fields on the Contract form as you can, and click **Submit**.

5.  Reopen the contract.

6.  In the Assets Covered related list, click **New**.

7.  In **Asset**, select the software covered by the contract.

8.  In **Date added**, select the date the software license was added to the contract.

    The date can be in the past, the present, or the future.

9.  In **Date removed**, select the date asset was, or will be, removed from the contract.

10. Click **Submit**.

11. Navigate to **Software Asset** &gt; **Reconciliation** &gt; **Software Counters**.

12. Click the software you specified.

13. Click **Count Licenses**.

    The licenses are listed under **Software Counter Results**. The licenses display as 0, but you are not out of compliance because you have an enterprise license with an enterprise contract. Once an enterprise contract is associated with software, all users are entitled when the licenses are counted.

    **Note:** In the Software Licenses list, enterprise licenses display **0** in the **Rights** column. The concept of rights is not used with enterprise licenses.


**Parent Topic:**[Software licenses in the legacy Software Asset Management plugin](../concept/c_SoftwareLicenses.md)

