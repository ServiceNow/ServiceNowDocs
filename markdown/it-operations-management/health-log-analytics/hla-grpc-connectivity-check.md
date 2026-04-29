---
title: Check gRPC and network connectivity for Health Log Analytics on the MID Server
description: Verify that Health Log Analytics can function properly by performing diagnostic tests on the MID Server to check gRPC and network connectivity.
locale: en-US
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [ServiceNow, Health Log Analytics, HLA, gRPC, connection]
breadcrumb: [Set up HLA on your instance, Configuring, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Check gRPC and network connectivity for Health Log Analytics on the MID Server

Verify that Health Log Analytics can function properly by performing diagnostic tests on the MID Server to check gRPC and network connectivity.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

Your organization's network and security configuration may be keeping Health Log Analytics from functioning properly. For example, complex configurations with proxy and firewall settings might block outbound connections. To avoid operational issues, you can test gRPC and network connectivity on the MID Server.

## Procedure

1.  Navigate to **All** &gt; **MID Server** &gt; **Servers**.

2.  Open the relevant MID Server record.

3.  Under Related Links, select **Test gRPC connection**.

    The system performs gRPC connectivity tests, such as domain name resolution, TCP/IP, and HTTP connection. When the testing is complete, the test results are displayed. Successful tests are preceded by a green check-mark, while failed tests are preceded by a red x mark.

    ![gRPC diagnostic test results screen.](../image/hla-grpc-test-results.png)

4.  Fix the issues that caused any tests to fail by following the instructions on the **gRPC diagnostic test results** screen.

5.  Select **Test gRPC connection** again and confirm that all the tests are completed successfully.


**Parent Topic:**[Set up Health Log Analytics on your ServiceNow instance](../concept/hla-implement.md)

