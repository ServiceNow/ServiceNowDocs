---
title: Updates to the JavaScript engine in Brazil
description: Review the updates to the JavaScript engine on the ServiceNow AI Platform in the Brazil release.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/scripts/updates-javascript-engine.html
release: brazil
product: Scripts
classification: scripts
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [JavaScript engine]
breadcrumb: [JavaScript engine, Write server-side scripts, Scripting, API implementation, API implementation and reference]
---

# Updates to the JavaScript engine in Brazil

Review the updates to the JavaScript engine on the ServiceNow AI Platform in the Brazil release.

The JavaScript engine is built on the open-source Rhino JavaScript engine and customized for scripting on the platform. In the Brazil release, the JavaScript engine was updated to include the following commits from Rhino. For more information about Rhino, see the [Rhino repository](https://github.com/mozilla/rhino) on GitHub.

|Pull request|Description|Applicable JavaScript mode|Update type|
|------------|-----------|--------------------------|-----------|
|\#1949|Infer function names|ECMAScript 2021 \(ES12\)|Feature|
|\#1973|Make the `__parent__` property no longer available in ES6|ECMAScript 2021 \(ES12\)|Feature|
|\#1976|Update `__proto__` support|ECMAScript 2021 \(ES12\)|Feature|
|\#1978|Enhance ISO date parsing with proper millisecond rounding|All modes|Feature|
|\#2004|Implement spread for object literals|ECMAScript 2021 \(ES12\)|Feature|
|\#2027|Clean up wrapping for Java method arguments, constructor arguments, and method return values|All modes|Feature|
|\#2030|Add `ArrayBuffer` transfer methods|ECMAScript 2021 \(ES12\)|Feature|
|\#2041|Optimize `undefined` lookup|All modes|Feature|
|\#2049|Implement `Math.f16round` method|ECMAScript 2021 \(ES12\)|Feature|
|\#1912|Adjust order of evaluation of function arguments to match the specification|All modes|Fix|
|\#1990|Improve super put processing|ECMAScript 2021 \(ES12\)|Fix|
|\#2008|Handle bound arguments correctly when the bound function is `call`|All modes|Fix|
|\#2017|Fix combination of `apply` and `call` in the interpreter|All modes|Fix|
|\#2031|Fix methods so they no longer have a `prototype` property|ECMAScript 2021 \(ES12\)|Fix|
|\#2038|Fix several issues with calling `bind()` in the interpreter|All modes|Fix|
|\#2047|Fix stack generation in interpreted mode|All modes|Fix|
|\#2077|Fix `Array.from` to prioritize iterable over array-like objects|ECMAScript 2021 \(ES12\)|Fix|
|\#2114|Fix the order of evaluation of various operations in compiled mode|All modes|Fix|
|\#1918|Fix performance regression from `LookupResult` change|All modes|Refactor|
|\#1930|Replace internal use of old `FunctionAndThis` methods|All modes|Refactor|
|\#1955|Refactor CallFrame|All modes|Refactor|
|\#1956|Refactor exception handling|All modes|Refactor|
|\#1958|Extract the inner loop of the interpreter to a separate method|All modes|Refactor|
|\#1959|Refactor interpreter dispatch|All modes|Refactor|
|\#1971|Remove leftover code from refactoring to lambda|All modes|Refactor|
|\#1984|Remove `VMBridge`|All modes|Refactor|
|\#2002|Remove unused `call` and `var` handling|All modes|Refactor|
|\#2095|Delegate Java getter and setter calling to `NativeJavaMethod` instead of `MemberBox`|All modes|Refactor|
|\#2105|Clean up symbol implementation in preparation for scope work|ECMAScript 2021 \(ES12\)|Refactor|
|\#2015|Add tests and fix the package and JavaScript version used|All modes|Test|

**Parent Topic:**[JavaScript engine on the platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/c_JS_engine_upgrade.md)

