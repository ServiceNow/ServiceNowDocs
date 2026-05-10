---
title: Build a flow using the Utility Actions spoke actions
description: Create a flow in Workflow Studio using the Utility Actions spoke actions to create two files; one for incident records and other for user records, and zip these two files.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Utility Actions Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Build a flow using the Utility Actions spoke actions

Create a flow in Workflow Studio using the Utility Actions spoke actions to create two files; one for incident records and other for user records, and zip these two files.

## Before you begin

Role required: admin.

## About this task

This sample flow demonstrates using the Utility Actions spoke actions to create files. You can configure the flow as per your requirement.

## Procedure

1.  Navigate to **All** &gt; **Flow Designer** &gt; **Designer**.

2.  Create a flow.

    For more information, see [Building flows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/flows.md).

3.  In the flow, add these spoke actions or flow logics:

    1.  Look Up Incident Records action to retrieve the incident records.

    2.  Begin File action to create a file that will contain the incident records.

    3.  For Each flow logic to apply the Append to Delimited File action to the list of incident records.

        ![Append to Delimited File spoke action](../image/append-delmt-utility.png)

    4.  Build File action to add rows.

        Each incident record is added as a row in the file.

        ![Build File spoke action](../image/build-file-utility.png)

    5.  Perform similar steps to retrieve records from the User \[sys\_user\] table.

        ![Retrieve user records](../image/user-records-utility.png)

    6.  Begin Zip action to build the ZIP file for the incident and user records.

    7.  Add File To Zip action to add a file containing the incident records to the ZIP file.

        ![Add File To Zip action](../image/add-file-zip-utility.png)

    8.  Add File To Zip action to add file containing the user records to the ZIP file.

        ![Add File To Zip action](../image/add-file2-utility.png)

    9.  Build a Zip action to create the ZIP file containing the incident and user records.

        ![Build File action](../image/build-file-utility.png)

4.  Save, test, and publish the flow to use it.

    ![Sample flow using the Utility Actions spoke actions](../image/flow-utility.png)


