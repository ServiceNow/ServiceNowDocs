---
title: Test Agent Client Collector connectivity
description: Test the Agent Client Collector \(ACC\) connectivity to identify any proxy issues.
locale: en-US
release: yokohama
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Getting started, Configure, Digital End-User Experience, IT Service Management]
---

# Test Agent Client Collector connectivity

Test the Agent Client Collector \(ACC\) connectivity to identify any proxy issues.

## Before you begin

**Note:** SSL inspection isn’t supported for DEX.

Role required: agent\_client\_collector\_admin

## Procedure

1.  Gather the following information to test communication between the ACC and ServiceNow shared services:

    1.  Copy CNC certificates from the agent to a new folder:

        |OS|Copy from|Paste to|
        |---|---------|--------|
        |Windows|`C:\ProgramData\ServiceNow\agent-client-collector\config\cert\cnc`|Any temp folder|
        |macOS|`/Library/Application Support/ServiceNow/agent-client-collector/cert/cnc`|Any temp folder|

    2.  Copy the gateway URL based on your location:

        -   AMER \(Americas\): itomcnc-prod-gateway.amer.sncapps.service-now.com:443
        -   EMEA \(Europe\): itomcnc-prod-gateway.emea.sncapps.service-now.com:443
        -   APAC \(Asia Paciﬁc\): itomcnc-prod-gateway.apac.sncapps.service-now.com:443
    3.  Navigate to **All** &gt; **sys\_attachment.list**.

    4.  Under **Attachments**, select **File name** in the drop-down menu and search for acc-dex-common.tar.gz.

    5.  Retrieve the following parameters:

        -   Record sys\_id
        -   Hash id
        ![Attachments table with the acc-dex-common.tar.gz record](../image/sys_attachments_table.png)

2.  Test the connection by running one of the following commands from the temp folder that you created:

    -   Without Proxy: `curl --verbose --output acc-dex-common.tar.gz --cert cnc_chain.crt --key priv_key.pem https://<ITOM-Gateway-URL>/content/v1/assets/<attachment_sys_id>/<hash_id>`
    -   With Proxy: `curl --verbose –-proxy <HOST_NAME>:<PORT> --output acc-dex-common.tar.gz --cert cnc_chain.crt --key priv_key.pem https://<ITOM-Gateway-URL>/content/v1/assets/<attachment_sys_id>/<hash_id>`
    The command output is generated.

3.  Confirm that the Content length in the command output matches the Size bytes in the Attachments table \(sys\_attachment\).

    See the preceding image for the location of the Size bytes information in the Attachments table.


Fix your proxy issues if the command output doesn't match the Attachments table entries.

