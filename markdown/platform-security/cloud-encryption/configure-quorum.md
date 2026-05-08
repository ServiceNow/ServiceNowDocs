---
title: Configure Quorum Control Policy Settings
description: Follow these steps to configure Quorum Control Policy Settings.
locale: en-US
release: australia
product: Cloud Encryption
classification: cloud-encryption
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Quorum Control Policy, Cloud Encryption with Key Management, Encryption]
---

# Configure Quorum Control Policy Settings

Follow these steps to configure Quorum Control Policy Settings.

## Before you begin

Roles required: sn\_kmf.admin

## About this task

**Warning:** You must sign a legal addendum to activate the key withdrawal functionality. The Quorum Control Policy Settings option becomes available when the withdrawal feature is enabled, otherwise the module is not visible on the app menu. After key withdrawal, your instance is no longer available until the encryption key is active again.

## Procedure

1.  Request the key withdrawal functionality from Customer Service and Support.

2.  Navigate to **Cloud Encryption Key Management** &gt; **Quorum Control Policy Settings**.

3.  Select the **Quorum control enabled** check box.![Displays the Quorum control enabled selection.](../quorum-control-policy-activate.png)

    Additional fields appear that are required to configure quorum control.![Quorum Control Policy Settings configuration.](../image/quorum-config-settings.png)

4.  Fill in the fields to complete the form.

<table id="choicetable_jby_cys_lrb"><thead><tr><th align="left" id="d105721e104">

Field

</th><th align="left" id="d105721e107">

Description

</th></tr></thead><tbody><tr><td id="d105721e113">

**Approvers**

</td><td>

Designate the members of the quorum from the list of users. Select the lock icon ![Lock icon.](../../key-management-framework/image/lock-icon.png) to open the user directory. There is no limit to the number of approvers that can be selected.

</td></tr><tr><td id="d105721e128">

**Minimum number of approvers to achieve quorum**

</td><td>

Designate the minimum number of approvers required to achieve quorum. For example, if there are nine approvers selected, a minimum of five may be configured for quorum. When five approvals are received in the system, quorum is reached and the withdraw operation starts.**Note:** The minimum number of required approvers is two.

</td></tr><tr><td id="d105721e140">

**Requests expire after the specified duration \(hours\)**

</td><td>

Set a numeric value in hours that is the maximum time allotment for the minimum number of approvals to be obtained. After the time frame expires, the quorum requests also expire. A new quorum request is required to continue with a withdrawal request.

</td></tr></tbody>
</table>5.  Click **Submit**.

    A confirmation message is displayed.


## What to do next

The withdrawal actions are available in [Key management operations](key-mgmt-operations-ce.md#).

**Parent Topic:**[Quorum Control Policy](../concept/quorum-ctrl-policy.md)

