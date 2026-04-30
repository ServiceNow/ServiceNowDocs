---
title: Enable the display of contract request details
description: As an administrator, enable the display of contract request details in the contract request form by adding related fields to display on the form.
locale: en-US
release: xanadu
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Add and configure contract request functionality, Configure Contract Management Pro, Contract Management Pro, Employee Service Management]
---

# Enable the display of contract request details

As an administrator, enable the display of contract request details in the contract request form by adding related fields to display on the form.

## Before you begin

Role required: admin

## About this task

Display the contract request fields and its values, add the following form headers available in the base system.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Configuration Settings** &gt; **UX Form Header**.

2.  Add UX Form Headers to the contract form by searching for and selecting the related table in the **Table** field.

    |Contract request form fields|Table|
    |----------------------------|-----|
    |**Short description, Priority, Contract state, Parent request, Contract status, and Signature type.**|sn\_cm\_core\_contract\_request|
    |**Participant name**|sn\_cm\_core\_signer\_task|
    |**Name of the document, requester of the contract request, latest version of the document, storage details and the folder where the document is stored**|sn\_cm\_core\_document and select it.|

3.  Select the **UX Header Configurations** tab.

4.  Select **Edit**.

5.  Select your workspace from the Available menu and move it to the Selected menu.

6.  Select **Save**.


**Parent Topic:**[Add and configure contract request functionality](../concept/cncore-uptake-steps.md)

