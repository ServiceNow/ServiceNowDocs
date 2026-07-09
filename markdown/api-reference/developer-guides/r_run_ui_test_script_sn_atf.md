---
title: sn\_atf — utility APIs
description: The sn\_atf API provides utility methods for a Run UI Test Script step: navigation, page evaluation, impersonation, file uploads, and shadow-DOM utilities.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/developer-guides/r\_run\_ui\_test\_script\_sn\_atf.html
release: australia
product: Developer Guides
classification: developer-guides
topic_type: reference
last_updated: "2026-06-25"
reading_time_minutes: 3
keywords: [sn\_atf, navigate, evaluate, impersonate, upload, Run UI Test Script]
breadcrumb: [Run UI Test Script Developer Guide, Developer guides, API implementation and reference]
---

# sn\_atf — utility APIs

The sn\_atf API provides utility methods for a **Run UI Test Script** step: navigation, page evaluation, impersonation, file uploads, and shadow-DOM utilities.

## Navigation

|Method|Description|
|------|-----------|
|sn\_atf.navigate\(url\)|Navigate the tested iframe to a URL, relative or absolute. Awaits full page load.|
|sn\_atf.reload\(\)|Reload the current page in the iframe.|
|sn\_atf.goBack\(\)|Go to the previous page in the navigation history managed by this step.|
|sn\_atf.goForward\(\)|Go to the next page in the navigation history.|

All navigation methods return Promises and resolve when the `load` event of the new page fires. The `screen` object automatically retargets to the new document body after navigation.

```
await sn_atf.navigate('/now/nav/ui/classic/params/target/incident_list.do');
const row = await screen.findByRole('row', { name: /INC0001234/ });
await user.click(row);
await screen.findByRole('heading', { name: /INC0001234/ });
```

## sn\_atf.evaluate\(fn, arg?\)

Runs `fn` inside the JavaScript realm of the tested iframe and returns a Promise with the result. This method mirrors the `page.evaluate()` contract in Playwright.

```
// Read a value from the iframe's context
const title = await sn_atf.evaluate(() => document.title);

// Pass an argument into the iframe context
const attr = await sn_atf.evaluate((sel) => document.querySelector(sel)?.dataset.state, '[data-testid="status"]');
```

The function is serialized through `.toString()` and evaluated in the iframe, so it can't close over variables from the test script scope. Pass data through the `arg` parameter instead.

`fn` can return a plain value or a Promise. When it returns a Promise, `evaluate` awaits it.

## sn\_atf.impersonate\(userId\)

Impersonates a user for the remainder of the step. Accepts a `sys_id` or `user_name`. The iframe reloads automatically after impersonation succeeds, and the original session is always restored when the step ends, whether the step passes, fails, or times out.

```
await sn_atf.impersonate('fred.luddy');
// Or by sys_id:
await sn_atf.impersonate('6816f79cc0a8016401c5a33be04be441');

// Now interact as that user
const btn = await screen.findByRole('button', { name: 'Create Incident' });
expect(btn).toBeEnabled();
```

Impersonation requires the ATF runner session to have the `impersonator` role.

## File uploads

|Method|Signature|Description|
|------|---------|-----------|
|`sn_atf.upload(source)`|`upload(sysId | File)`|Upload to the current classic ServiceNow form. Pass a `sys_attachment` sys\_id to copy server-side, with no bytes transferred, or pass a `File` object to upload through REST.|
|`sn_atf.uploadInWS(source, table?, sysId?)`|`uploadInWS(sysId | File, tableName?, recordSysId?)`|Upload to a Workspace record. `table` and `sysId` are inferred from the current URL when omitted.|
|`sn_atf.uploadInSP(source, table?, sysId?)`|`uploadInSP(sysId | File, tableName?, recordSysId?)`|Upload to a Service Portal form record. `table` and `sysId` are read from the URL query parameters when omitted.|
|`sn_atf.uploadInSCVariable(source, variableName)`|`uploadInSCVariable(sysId | File, variableName)`|Upload to a service catalog attachment variable in the classic catalog. `variableName` is the column name, for example `'proof_of_id'`.|
|`sn_atf.uploadInSPVariable(source, variableName, opts?)`|`uploadInSPVariable(sysId | File, variableName, { timeout? })`|Upload to a Service Portal catalog attachment variable. `variableName` is the column name without the `sp_formfield_` prefix.|

sn\_atf.upload\(\) returns Promise&lt;void&gt;, not Promise&lt;\{ sysId, name, size \}&gt;. Only uploadInWS, uploadInSP, uploadInSCVariable, and uploadInSPVariable return \{ sysId, name, size \}.

```
// Copy an existing attachment to the current form (no bytes transferred)
await sn_atf.upload('a1b2c3d4e5f67890a1b2c3d4e5f67890');

// Upload a File retrieved from another attachment
const file = await sn_atf.getAttachmentFile('a1b2c3d4e5f67890a1b2c3d4e5f67890');
await sn_atf.uploadInWS(file);
```

## sn\_atf.getAttachmentFile\(sysId\)

Fetches the bytes of a `sys_attachment` record through the REST API and returns a `Promise<File>` with the correct name and content type. Use this method to read an attachment from one record and upload it to another.

```
const file = await sn_atf.getAttachmentFile('a1b2c3d4e5f67890a1b2c3d4e5f67890');
await sn_atf.upload(file);
```

## DOM utilities

|Method|Description|
|------|-----------|
|`sn_atf.querySelector(root, selector)`|Shadow-DOM-piercing `querySelector`. Finds the first element that matches `selector` under `root`, crossing shadow boundaries.|
|`sn_atf.querySelectorAll(root, selector)`|Shadow-DOM-piercing `querySelectorAll`. Returns all matching elements.|
|`sn_atf.getActiveElement(root?)`|Returns the currently focused element, piercing shadow roots and iframes.|
|`sn_atf.waitForElementToBeRemoved(element, opts?)`|Waits until `element` is removed from the DOM. Resolves immediately if the element is already disconnected.|
|`sn_atf.delay(ms)`|Returns a Promise that resolves after `ms` milliseconds. Prefer `waitFor` or `findBy*` for dynamic waits, and use `delay` only when a fixed pause is unavoidable.|

