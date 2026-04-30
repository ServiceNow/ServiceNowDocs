---
title: Tokenize strings using encryption patterns
description: You can replace string patterns with tokens before they are sent to and stored in the instance.
locale: en-US
release: zurich
product: Edge Encryption
classification: edge-encryption
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configuring Edge Encryption, Edge Encryption, Encryption]
---

# Tokenize strings using encryption patterns

You can replace string patterns with tokens before they are sent to and stored in the instance.

## Before you begin

To use encryption patterns, you must install and set up a MySQL database in your network. This is the same database used for order-preserving encryption. To create or edit encryption patterns, you must be connected to the instance through the proxy.

Role required: security\_admin

## About this task

You can use base system patterns, or create your own patterns. Base system patterns are advanced patterns. Encryption patterns include the following limitations.

-   A pattern of all alpha characters is not allowed.
-   The minimum pattern size is five characters. You can change this setting using a system property.
-   The \* and + quantifiers are forbidden in encryption patterns.
-   Encryption patterns match complete words, not parts of strings embedded in a larger string. Words are defined by spaces and characters not available for inclusion in a pattern.
-   If the same string is sent to the instance multiple times, it is replaced with the same token.
-   Text search on exact matches is supported. The query string is exchanged with a token when sent to the instance, the search is performed on tokens, and when the search results are returned to the proxy server, the tokens are replaced with the clear text. Features such as stemming are not supported.

When using patterns, the clear text never leaves your network. When the proxy server matches a pattern in a request going to the instance, the proxy replaces the string with a token of the same size. The token is sent to instance instead of the clear text string. When the response is sent from the instance to the proxy server, the proxy replaces the token with the string. When viewed through the proxy server, the string displays as clear text.

**Note:** Encrypted fields are not checked for encryption patterns.

## Procedure

1.  Navigate to **All** &gt; **Edge Encryption Configuration** &gt; **Encryption Patterns** &gt; **Create New**.

    Alternatively, you can navigate to **Advanced Patterns** to activate or edit a preconfigured pattern.

2.  Enter the pattern name.

3.  Define the **Edge pattern input type**.

<table id="choicetable_nkx_mdv_s1b"><tbody><tr><td id="d33835e126">

**Basic**

</td><td>

A series of character types. In the **Basic Pattern Input** tab, click **Add** and select a character type.The **Sample pattern** displays the pattern as characters are added.

 Click **New Block** to move the next character to the next line. This enables you to group characters in a long pattern.

 Click **X** to delete the last character in the pattern.

</td></tr><tr><td id="d33835e159">

**Advanced**

</td><td>

A Java RegEx expression. If advanced is selected, you cannot change the input type back to basic.In the **Sample match** field, enter a sample pattern to test the RegEx expression. In the **Pattern** field, enter a Java RegEx expression. Click **Validate** to verify that the expression matches the sample pattern.

</td></tr></tbody>
</table>    The input type defines how you are going to enter the pattern. It does not impact how the pattern is used.

4.  Click **Submit**.


**Parent Topic:**[Configuring Edge Encryption](../concept/edge-config.md)

