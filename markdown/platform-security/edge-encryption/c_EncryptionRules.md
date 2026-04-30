---
title: Define a custom encryption rule
description: It may be necessary to identify and encrypt sensitive information in HTTP requests on the way to your instance. You can write encryption rules to identify, interpret, and encrypt data in such requests, mapping fields in the request to table-field names on your instance.
locale: en-US
release: zurich
product: Edge Encryption
classification: edge-encryption
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Configuring Edge Encryption, Edge Encryption, Encryption]
---

# Define a custom encryption rule

It may be necessary to identify and encrypt sensitive information in HTTP requests on the way to your instance. You can write encryption rules to identify, interpret, and encrypt data in such requests, mapping fields in the request to table-field names on your instance.

## What is an encryption rule

Encryption rules are scripts executed on the Edge Encryption proxy server to map fields in a request to fields in a table on your ServiceNow instance. An encryption rule tells the Edge Encryption proxy server how to encrypt data in custom payloads.

**Note:** Encryption rules only support ECMAScript 3 and below.

## When to use custom rules

A set of encryption rules is included as part of the Edge Encryption plugin. These rules handle many core platform use cases, such as:

-   Editing a field from the list edit form
-   Updating a record from the record form
-   Managing direct web service
-   Processing data from the REST Application Program Interface \(API\)

Applications created using standard forms and lists should work without custom encryption rules.

If you develop scripts that contain data that should be encrypted, create encryption rules to find and map that data to Glide table-field names. For example:

-   Scripted processors
-   Scripted web services
-   Scripted REST APIs, UIs, or Ajax scripts

## Format of an encryption rule

Rules include three parts:

-   **Condition**: Identifies the type of request.
-   **Action**: Maps fields in the request to fields in a table, encrypting values that map to fields with encryption configurations defined.
-   **Order**: Priority of the rule. The lowest priority rule with a satisfied condition is the only rule that runs. Like business rules, rules run from lowest to highest.

Except for attachment requests, HTTP requests are evaluated by the Edge Encryption proxy server. The Edge Encryption proxy server evaluates all encryption rule conditions in priority order until either all conditions return false, or one condition returns true. When a condition returns true, the action is executed on the request, and the result is forwarded to the instance. No other conditions are evaluated. As a result, encryption rule conditions should be as specific as possible. A generic rule might evaluate as true for a request meant to be processed by another rule, causing the request to be processed by the wrong action. If a generic condition is unavoidable, the rule should be marked with a high-order value so that more specific rules are evaluated first.

## Guidelines for creating encryption rules

Creating efficient, optimized encryption rules can reduce processing time for script validation.

**Overall guideline**: When rules get long, do your best to minimize the number of blocks and break the rules apart whenever possible. Ideally, custom rules should apply to specific use cases, rather than encompassing several cases, with `ifs` or switch statements in the action script.

1.  Split rules whenever possible. For example,
    -   Create different rules for different tables and ensure that each rule runs only on its respective table.
    -   Create different rules for each record producer that you’re targeting, or at least for each subset of record producers. Instead of one rule targeting dozens of `sys_ids`, you could create several different rules targeting smaller subsets of record producers, or even create one rule per `sys_id`.

        **Note:** Creating multiple rules requires more maintenance. The trade-off is that multiple, simpler rules can be validated more efficiently than longer, more complex rules.

2.  Minimize the number of blocks. Because the processing engine scans each block while evaluating scripts, a large number of blocks causes delays in validation. For example,
    -   Replace all `if` blocks with an array lookup, and replace all blocks in the array lookup with just one `if` block.
    -   Combine `if` blocks whenever it’s possible to group them.

## Encryption rule APIs

Encryption rules are written in JavaScript and utilize Edge Encryption APIs to locate and encrypt sensitive information in the body of a request. The API uses expressions similar to xPath to navigate through both JSON and XML content.

Edge Encryption APIs process the request off the stream as it is being written to the output stream. Stream parsing enables encryption rules to be network performant. However, fetching and parsing content from the body multiple times could lead to unexpected results. To void this potential problem, requests should be processed by the action in a single pass.

When creating encryption rules, you can’t use Glide APIs, script includes, business rules, or any global parameters such as *current*. Because the rules are created for HTTP objects, a global request object is available.

When creating encryption rules, you can’t use APIs from the allow list manager or scoped applications.

## Error handling

If an encryption rule condition or action throws an exception, check the proxy log for troubleshooting information.

-   **[Inspect the client request](../task/request-type.md)**  
Before creating a custom encryption rule, you must determine the format of the client request entering the Edge Encryption proxy server.
-   **[Create an encryption rule](../task/t_CreateAnEncryptionRule.md)**  
Encryption rules are used by the proxy to find content in HTTP requests that should be encrypted.
-   **[Encryption rule conditions](c_EncryptionRuleConditions.md)**  
Encryption rule conditions determine if the rule should be executed.
-   **[Encryption rule actions](c_EncryptionRuleActions.md)**  
An encryption rule maps fields in a client request to fields in a table on your instance and identifies fields marked for encryption.
-   **[Encryption rule objects and APIs](api-overview.md)**  
Use encryption rule APIs to parse and encrypt values in requests moving through the Edge Encryption proxy server to the instance.

**Parent Topic:**[Configuring Edge Encryption](edge-config.md)

