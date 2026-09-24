---
title: Set up account linking for WhatsApp on NextWave
description: Link WhatsApp customers to contact or consumer records automatically or manually within the NextWave off-Glide architecture.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/messg-whatsapp-nextwave-account-linking.html
release: brazil
topic_type: task
last_updated: "2026-09-18"
reading_time_minutes: 1
keywords: [WhatsApp, account linking, auto account linking, NextWave]
breadcrumb: [WhatsApp on NextWave, Integrating with consumer messaging apps, Integrate, Customer Service Management]
---

# Set up account linking for WhatsApp on NextWave

Link WhatsApp customers to contact or consumer records automatically or manually within the NextWave off-Glide architecture.

## Before you begin

Role required: **sn\_customerservice\_admin**

## About this task

Account linking connects a WhatsApp customer to an existing contact or consumer record in Customer Service Management. On NextWave, the system supports both manual account linking \(an agent verifies and links the customer\) and auto account linking \(the system matches and links the customer based on predefined criteria without manual intervention\).

## Procedure

1.  Auto account linking
2.  Verify that auto account linking is enabled for the WhatsApp channel.

    When auto account linking is active, the system automatically matches incoming WhatsApp customers to existing contact or consumer records based on the customer's phone number or other configured identifiers. No manual intervention is required.

3.  Manual account linking
4.  Open the unlinked WhatsApp interaction in the CRM Workspace.

5.  Use the lookup and verify action to search for and select the contact or consumer record that matches the customer.


## Result

Linked accounts are accessible to the user as intended. The system maintains integrity and security during account linking processes within NextWave.

**Related topics**  


[whatsapp-username-based-customer-identification]

[link-whatsapp-bsuid-to-known-contact]

