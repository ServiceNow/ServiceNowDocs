---
title: Create Help Center content for configurable workspace
description: Create Help Center content to provide your users with helpful information about the page that they are working on within a configurable workspace.
locale: en-US
release: zurich
product: Adoption Services
classification: adoption-services
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Using Help Center, Help Center, In-product help, Adoption services, Configure user experiences]
---

# Create Help Center content for configurable workspace

Create Help Center content to provide your users with helpful information about the page that they are working on within a configurable workspace.

## Before you begin

Create or edit an embedded help record before creating a guidance record by following the steps in [Add custom Embedded Help content](../../help-guided-tours/task/add-custom-help-topic.md) to create content or [Add custom Embedded Help from a copy](../../help-guided-tours/task/add-custom-help-copy.md) to modify existing content.

Role required: admin

## About this task

To create Help Center content, you will create or modify two record types: guidance records and embedded help records. The guidance record enables your content, which is in an Embedded Help record, to display in the Help Center. This procedure explains how to enable displaying existing embedded help content in the Help Center.

## Procedure

1.  Navigate to the configurable workspace page for which you are creating Help Center guidance.

2.  Copy or otherwise take note of the page URL, such as `<instance name>.service-now.com/now/sow/home`.

3.  Select the **Show help** icon \(![](../../../administer/core-configuration/image/help-icon.png)\) in the Unified Navigation menu to expand the Help Center.

4.  Scroll to the bottom of the Help Center and select **Add New Content**.

    A new tab with the Guidance form displays.

5.  Fill in the fields on the Guidance form.

<table id="table_ajy_dmn_jsb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The title of your guidance, which displays in the Help Center.

</td></tr><tr><td>

Type

</td><td>

Select **Embedded Help**.

</td></tr><tr><td>

Roles

</td><td>

The user roles required to see your guidance.**Note:** Help content that is only relevant to your chosen role is supported. For example, users with the ITIL role will only see help created for the ITIL role, previously all help was displayed for all roles.

</td></tr><tr><td>

Application route

</td><td>

Part of the URL for the workspace page that you're targeting, in the format `now/<yourpagename>`.

 Refer to the URL you noted earlier and enter this portion of the URL, for example `now/sow`.

 See the [examples](create-help-center-content.md#example_nln_bm3_kxb) following these steps for more information on identifying the application route from the URL.

 To target all workspace pages use `sn_all`for the application route and context fields.

</td></tr><tr><td>

Embedded help content

</td><td>

The content of your guidance, which is displayed to users in the Help Center. Select an existing embedded help record, or create an embedded help record as described in [Add custom Embedded Help content](../../help-guided-tours/task/add-custom-help-topic.md).

</td></tr><tr><td>

Context

</td><td>

A value found in the URL of the workspace page you're targeting that immediately follows the Application Route. For example, in `now/sow/home`, the context is `home`.

 Refer to the URL you noted earlier and provide only the word immediately following the value entered in the Application Route field. Values depend on the workspace and may also include `list` and `record`.

 See the [examples](create-help-center-content.md#example_nln_bm3_kxb) following these steps for more information on identifying the context from the URL.

 To target help content on all pages in a particular workspace use the appropriate workspace application route, and enter `sn_all` for the context field.

</td></tr><tr><td>

Description

</td><td>

The description of your guidance, which displays in the Help Center as a short description under the title provided in the Name field.

</td></tr><tr><td>

Route parameters

</td><td>

An advanced configuration to display guidance only when users view specific lists or record types within your workspace.

 To provide guidance when a user is viewing a specific list, review the URL you noted earlier and look for the list id number, such as `list-id/d03d64feebd1301080de83402a5228f1`. Then, enter route parameters in the following format: `{"params":{"listId":"d03d64feebd1301080de83402a5228f1"}}`.

 To provide guidance when a user is viewing a specific record type, review the URL you noted earlier and look for the record name, such as `record/problem`. Then, enter route parameters in the following format: `{"params":{"table":"problem"}}`.

 To provide guidance when a user is viewing a related record \(a record accessed from within another record\), look for the second record name in the URL, such as `sub/record/incident`. Then, enter route parameters in the following format: `{"params":{"table":"incident"}}`.

 See the [examples](create-help-center-content.md#example_nln_bm3_kxb) following these steps for more information on identifying route parameters from the URL.

</td></tr><tr><td>

Application

</td><td>

The scope of your application.

</td></tr><tr><td>

Status

</td><td>

The status of your guidance. Select **Published** when the guidance is ready to display in the Help Center.

</td></tr><tr><td>

Active

</td><td>

Indicates that the guidance is active. Keep this option checked when the guidance is published.

</td></tr><tr><td>

ServiceNow® created

</td><td>

Indicates that the guidance was created by ServiceNow®. Reserved for ServiceNow® use only.

</td></tr><tr><td>

Version

</td><td>

The current family release version for your guidance.

</td></tr></tbody>
</table>6.  Select **Submit**.


## Creating guidance for a list in a configurable workspace

To provide guidance when a user is viewing a specific list, review the URL and look for the list id number, such as `list-id/7ae4da1ec3013010965e070e9140dd66`. Then, enter route parameters in the following format: `{"params":{"listId":"7ae4da1ec3013010965e070e9140dd66"}}`.

![A labeled image highlighting parts of the URL used in the guidance record fields.](../image/URL-with-list-id.png "Route parameters for list")

## Creating guidance for a record in a configurable workspace

To provide guidance when a user is viewing a specific record type, review the URL and look for the record name, such as `record/problem`. Then, enter route parameters in the following format: `{"params":{"table":"problem"}}`.

![A labeled image highlighting parts of the URL used in the guidance record fields.](../image/URL-with-record.png "Route parameters record type")

## Creating guidance for a related record in a configurable workspace

To provide guidance when a user is viewing a related record \(a record accessed from within another record\), look for the second record name in the URL, such as `sub/record/incident`. Then, enter route parameters in the following format: `{"params":{"table":"incident"}}`.

![A labeled image highlighting parts of the URL used in the guidance record fields.](../image/URL-with-related-record.png "Route parameters related record")

