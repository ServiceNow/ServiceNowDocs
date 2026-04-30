---
title: Initiate metadata extraction from a contract
description: Use generative AI capabilities to extract metadata from a signed contract attached in a contract repository record.
locale: en-US
release: zurich
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Contract metadata extraction, Use generative AI skills, Now Assist in CM Pro, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Initiate metadata extraction from a contract

Use generative AI capabilities to extract metadata from a signed contract attached in a contract repository record.

## Before you begin

Ensure that Now Assist has data access or your role. For more information, see [Configure data permissions for Now Assist skills](cmpro-conf-roles-skills.md).

Role required: sn\_cm\_gen\_ai.ai\_contract\_fulfiller

## About this task

You can also configure the system properties to automatically initiate the metadata extraction process once the contract repository record is created. For more information, see [Configure system properties for contract metadata extraction](cncore-conf-sys-prop-na.md).

**Note:** Contract metadata extraction using generative AI capabilities is not available when the Manage contract repository agentic workflow is enabled.

## Procedure

1.  Open a contract repository record where you want to extract information from a contract.

<table id="choicetable_zst_kcr_5bc"><thead><tr><th align="left" id="d196162e98">

Method

</th><th align="left" id="d196162e101">

Steps

</th></tr></thead><tbody><tr><td id="d196162e107">

**Contract Workspace**

</td><td>

1.  Navigate to **All** &gt; **Contract Workspace**.
2.  Select the list icon \(![List icon.](../../legal-request-management/image/lsd-lcc-list-icon.png)\).
3.  Select **Executed contracts**.
4.  Select **All**.
5.  Select the contract repository record.


</td></tr><tr><td id="d196162e155">

**Workspace used by your application**

</td><td>

1.  Navigate to your workspace.
2.  Open a contract request that is in the Closed complete or Contract signed state.
3.  Select the **Contract repository** tab.
4.  Select the contract repository record.


</td></tr></tbody>
</table>2.  Select **Initiate metadata extraction**.

    A message appears stating that the metadata extraction process has been initiated. You receive an email notification when the process is completed.

    The **Review extracted metadata** button appears on initiating the metadata extraction. You can select the button after the metadata extraction is completed.


## What to do next

[Work with extracted metadata](cncore-review-metatdata.md)

**Parent Topic:**[Contract metadata extraction using Now Assist in Contract Management](../concept/cncore-metadata-extract-land.md)

