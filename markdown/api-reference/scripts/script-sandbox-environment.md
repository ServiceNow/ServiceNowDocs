---
title: Script sandbox environment
description: The script sandbox environment is a restricted execution context in which untrusted, client-generated scripts run on the server using one of two evaluators: the guarded script evaluator or the script sandbox evaluator.
locale: en-US
release: australia
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2026-04-09"
reading_time_minutes: 3
breadcrumb: [Server-side scripting, Scripting, API implementation, API implementation and reference]
---

# Script sandbox environment

The script sandbox environment is a restricted execution context in which untrusted, client-generated scripts run on the server using one of two evaluators: the guarded script evaluator or the script sandbox evaluator.

## Script sandbox environment overview

When a script is sent to the server, a server-side script evaluator determines whether the script is trusted. Trusted scripts run in the JavaScript engine. Untrusted scripts run in the restricted sandbox environment instead.

**Note:** The sandbox does not apply to script includes, which run in the application scope outside of the sandbox, or to client-side scripts.

Untrusted scripts are client-generated and sent to the server for evaluation in the following ways:

-   Filter or query parameters: Filter and query parameters in URLs can send scripts to the server with HTTP requests, such as when a logged-out user follows a link containing a `javascript:` filter parameter.
-   System APIs: The AJAXEvaluate API call allows the client to run arbitrary scripts on the server and receive a response.

Within the sandbox, the following restrictions apply to scripts:

-   Only business rules marked **Client callable** can be called.
-   Only script includes marked **Sandbox enabled** can be called.
-   Certain API calls, mostly limited to ones dealing with direct database access, aren’t allowed.
-   Data can’t be inserted, updated, or deleted from within the sandbox. For example, any calls to current.update\(\) are ignored.

**Note:** Beginning with the Xanadu release, script includes marked as **Glide AJAX enabled** \(previously named **Client callable**\) aren’t accessible within the sandbox. Only those marked **Sandbox enabled** are available within the sandbox. When upgrading to the Australia release from the Washington DC release or earlier, any script includes marked as **Client callable** are also marked as **Sandbox enabled**.

## Script sandbox evaluators

Beginning with the Australia Patch 2 release, the sandbox uses two evaluators to enforce different levels of restrictions:

-   Guarded script evaluator: Enhances instance security by supporting only a restricted scripting language and rejecting untrusted scripts that are incompatible. Guest transactions are fully enforced immediately. Scripts sent by authenticated users are evaluated differently depending on the instance type.
-   Script sandbox evaluator: Helps prevent executing untrusted scripts on an instance by limiting the APIs available to scripts.

<table id="table_evaluator_comparison"><thead><tr><th>

Characteristic

</th><th>

Guarded script evaluator

</th><th>

Script sandbox evaluator

</th></tr></thead><tbody><tr><td>

Purpose

</td><td>

Provides enhanced security for scripts that run in the sandbox. Uses a domain-specific language \(DSL\) that permits only a small set of JavaScript features.

</td><td>

Supports additional JavaScript but restricts certain APIs for scripts.

</td></tr><tr><td>

JavaScript support

</td><td>

Only a single simple expression or function call and only certain APIs.

</td><td>

Features supported by the JavaScript engine except for certain API and method restrictions.

</td></tr><tr><td>

When it runs

</td><td>

Evaluates untrusted scripts that haven't been granted a guarded-script exemption.

</td><td>

Evaluates untrusted scripts under the following conditions:-   A script has been granted a guarded-script exemption \(manually or automatically\).
-   When guarded script is in Phase 1: Detection, and a script is sent to the server by an authenticated user.

</td></tr><tr><td>

Script includes

</td><td>

Not applicable: script includes run outside the sandbox in the application scope

</td><td>

Not applicable: script includes run outside the sandbox in the application scope

</td></tr></tbody>
</table>For details about each evaluator, including JavaScript restrictions, see the following topics and the [Server-Side Sandbox Runtime Replacement \[KB2944435\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2944435) article on the Now Support Knowledge Base.

-   **[Guarded script evaluator](guarded-script.md)**  
The guarded script evaluator enhances instance security by supporting only a restricted scripting language and detecting or rejecting untrusted scripts that use unsupported JavaScript features.
-   **[Script sandbox evaluator](script-sandbox.md)**  
The script sandbox evaluator helps prevent executing untrusted scripts on an instance by limiting the APIs available to scripts.

**Parent Topic:**[Server-side scripting](c_ServerScripting.md)

