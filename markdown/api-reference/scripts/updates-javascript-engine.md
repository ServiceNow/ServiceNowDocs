---
title: Updates to the JavaScript engine in Australia
description: Review the updates to the JavaScript engine on the ServiceNow AI Platform in the Australia release.
locale: en-US
release: australia
product: Scripts
classification: scripts
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [JavaScript engine, Server-side scripting, Scripting, API implementation, API implementation and reference]
---

# Updates to the JavaScript engine in Australia

Review the updates to the JavaScript engine on the ServiceNow AI Platform in the Australia release.

The JavaScript engine is built on the open-source Rhino JavaScript engine and customized for scripting on the platform. In the Australia release, the JavaScript engine was updated to include the following commits from Rhino. For more information about Rhino, see the [Rhino repository](https://github.com/mozilla/rhino) on GitHub.

|Pull request|Description|Applicable JavaScript mode|Update type|
|------------|-----------|--------------------------|-----------|
|\#2048|Add `Error.isError`|ECMAScript 2021 \(ES12\)|Feature|
|\#2029|Add new `Set` methods|ECMAScript 2021 \(ES12\)|Feature|
|\#2025|Add `Promise.try`|ECMAScript 2021 \(ES12\)|Feature|
|\#1966|Add `TypedArray.from` and `TypedArray.of`|ECMAScript 2021 \(ES12\)|Feature|
|\#1980|Add `Promise.withResolvers`|ECMAScript 2021 \(ES12\)|Feature|
|\#1905|Support `ArrayBuffer` detachment|ECMAScript 2021 \(ES12\)|Feature|
|\#1896|Enhance date string parsing with optional millisecond digits|All modes|Feature|
|\#1751, \#1872|Support `Symbol.hasInstance` on `Function.prototype`|ECMAScript 2021 \(ES12\)|Feature|
|\#1870|Rework `String.prototype.search`, `replace`, `replaceAll`, and `split`|ECMAScript 2021 \(ES12\)|Feature|
|\#2073, \#2107|Support duplicate keys in object literals|ECMAScript 2021 \(ES12\)|Fix|
|\#2097|Calling `eval` of a function returns `undefined`|ECMAScript 2021 \(ES12\)|Fix|
|\#2065|Correct template literal to string conversion|ECMAScript 2021 \(ES12\)|Fix|
|\#2060|Don’t propagate strict mode when compiling scripts|ES5 Standards|Fix|
|\#1979|Support `BigInt.asUintN` and `BigInt.asIntN`|ECMAScript 2021 \(ES12\)|Fix|
|\#1860|Correct `this` in `apply` and `call`|ECMAScript 2021 \(ES12\)|Fix|
|\#1982|Correct `this` in `Array.from`|ECMAScript 2021 \(ES12\)|Fix|
|\#1945|Correct `this` in `require`|ECMAScript 2021 \(ES12\)|Fix|
|\#1774|Don't allow methods to be used as constructors|ECMAScript 2021 \(ES12\)|Fix|
|\#1806|Fix hoisting behavior|All modes|Fix|

**Parent Topic:**[JavaScript engine on the platform](../concept/c_JS_engine_upgrade.md)

