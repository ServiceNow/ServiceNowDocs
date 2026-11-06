---
title: Migrate MID Servers to IPKI
description: Move an existing MID Server that uses basic authentication to ServiceNow certificate-based IPKI authentication. Migrating a MID Server to IPKI preserves the user previously set on that MID Server.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/servicenow-platform/mid-server/mid-migrate-basic-to-ipki.html
release: australia
product: MID Server
classification: mid-server
topic_type: task
last_updated: "2026-10-21"
reading_time_minutes: 2
keywords: [iPKI, MID Server migration]
breadcrumb: [MID Server IPKI authentication, Securing and encrypting MID Server data, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Migrate MID Servers to IPKI

Move an existing MID Server that uses basic authentication to ServiceNow certificate-based IPKI authentication. Migrating a MID Server to IPKI preserves the user previously set on that MID Server.

## Before you begin

Role required: admin or agent\_admin

## About this task

You can migrate more than one MID Server at a time, but only after at least one MID Server is already running on IPKI. Until then, you can select and migrate only one MID Server. After one MID Server is confirmed on IPKI, bulk migration becomes available for the rest.

## Procedure

1.  On your instance, navigate to **Workspaces** &gt; **ITOM Infra Services Workspace**.

2.  Select the **MID Servers** icon in the left navigation panel.

3.  Select the **Auth-type migration** tab.

4.  From the **Eligible MID Server** list, select the MID Server you want to migrate, and then select **Migrate**.

    To migrate all MID Servers at once, select **Migrate All**. To migrate only specific MID Servers, select the check boxes next to them, and then select **Migrate**.

    **Note:** The **Eligible MID Server** list shows MID Servers that are on basic authorization. A MID Serverthat isn't validated remains in the list, but the **Migrate** button stays disabled for it until it's validated.

5.  In the **Migrate MID Server** dialog, select **Migrate Server**.

6.  Monitor the migration record until it shows a result of succeeded or failed.

    If the migration record shows failed, read the failure detail on the record, address the cause, and start the migration again. For the messages that the MID Server logs, see [MID Server IPKI reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/mid-server/mid-server-ipki-reference.md).

    If the migration record remains in an intermediate state for more than an hour, an investigation is needed.


## Result

On a successful migration, the status of the MID Server changes to **Certificate issued**. The username and password of the MID Server are removed from `config.xml`, and the MID Server authenticates using IPKI.

\[Omitted image "mid-server-ipki-cert-issued.png"\] Alt text: MID Server status showing Certificate issued after a successful iPKI migration.

To move a MID Server back to basic authentication, see [Revert MID Servers from IPKI to basic authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/mid-server/mid-revert-ipki-to-basic-authentication.md).

**Parent Topic:**[MID Server IPKI authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/mid-server/mid-server-ipki-authentication.md)

