---
title: Create an encryption rule
description: Encryption rules are used by the proxy to find content in HTTP requests that should be encrypted.
locale: en-US
release: australia
product: Edge Encryption
classification: edge-encryption
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Define a custom encryption rule, Configuring Edge Encryption, Edge Encryption, Encryption]
---

# Create an encryption rule

Encryption rules are used by the proxy to find content in HTTP requests that should be encrypted.

## Before you begin

Role required: security\_admin

Before creating an encryption rule, you must [Inspect the client request](request-type.md) to determine the format.

## About this task

To create or edit encryption rules, you must be connected to the instance through an encryption proxy.

## Procedure

1.  Navigate to **All** &gt; **Edge Encryption Configuration** &gt; **Rules** &gt; **Create New**.

2.  In the **Name** box, enter a name.

3.  In the **Request Type**, select an HTTP method.

    -   **HTTP Post**
    -   **HTTP Get**
    -   **HTTP Put**
    -   **HTTP Patch**
    -   **HTTP Delete**
    **Note:** Pre-Jakarta instances allow only **HTTP Get** and **HTTP Post** methods.

4.  In the **Condition** box, enter a JavaScript statement defining when the rule should run.

5.  In the **Action** box, enter a JavaScript function to be executed when the condition is true.

6.  In the **Order** box, enter the relative priority of the rule.

7.  Click **Submit**, or save the form.


**Parent Topic:**[Define a custom encryption rule](../concept/c_EncryptionRules.md)

