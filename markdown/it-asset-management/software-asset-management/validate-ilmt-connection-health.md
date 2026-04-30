---
title: Validate your ILMT connection health
description: Validate the health of your ILMT connections to help improve the success of each connection. Use the results to evaluate how you can resolve unsuccessful connections, such as adjusting the connection response time or fixing errors related to invalid hardware serial numbers.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [IBM License Metric Tool \(ILMT\) and BigFix Inventory integrations, Software Asset Management publisher pack for IBM, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Validate your ILMT connection health

Validate the health of your ILMT connections to help improve the success of each connection. Use the results to evaluate how you can resolve unsuccessful connections, such as adjusting the connection response time or fixing errors related to invalid hardware serial numbers.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Software Asset** &gt; **Integration - ILMT/BigFix Inventory** &gt; **Connection Health**.

2.  Select **Validate**.

    The Connection Healths list reloads with the latest status of each ILMT connection.

3.  Verify the status of each connection using the **Status** field.

    If the **Status** field is set to **Failed**, refer to the corresponding **Information** field for more details about why that connection has failed and what actions you can take to help it establish successfully.

    For example, if a connection has failed due to a timeout issue, the **Information** field indicates that the connection has timed out. The **Information** field also suggests a recommended timeout value to help prevent the connection from failing again.


**Parent Topic:**[IBM License Metric Tool \(ILMT\) and BigFix Inventory integrations](../concept/ibm-ilmt-bigfix-inventory-integration.md)

