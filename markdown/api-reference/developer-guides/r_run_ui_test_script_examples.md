---
title: UI Test Script examples
description: Reference example scripts to use in a Run UI Test Script step.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/developer-guides/r\_run\_ui\_test\_script\_examples.html
release: australia
product: Developer Guides
classification: developer-guides
topic_type: reference
last_updated: "2026-06-25"
reading_time_minutes: 3
keywords: [Run UI Test Script, examples, ATF, UI testing]
breadcrumb: [Run UI Test Script Developer Guide, Developer guides, API implementation and reference]
---

# UI Test Script examples

Reference example scripts to use in a Run UI Test Script step.

These examples include:

-   Element verification,
-   filling and saving records,
-   waiting for async conditions,
-   impersonation,
-   file uploads,
-   step outputs,
-   parameter values,
-   and scoped queries.

## Assert that a heading is visible on the current page

```
const heading = screen.getByRole('heading', { name: 'My Application' });
expect(heading).toBeVisible();
```

## Navigate to a record, fill a field, and save

```
await sn_atf.navigate('/incident.do?sys_id=-1');

// Update Caller
const caller = screen.getByRole('searchbox', { name: 'Caller' });
await user.click(caller);
await user.type(caller, 'Abel Tuter');
await user.tab();

// Update Short description
const short_desc = screen.getByRole('textbox', { name: 'Short description' });
await user.click(short_desc);
await user.type(short_desc, 'Cannot connect to VPN');

// Click Submit
await sn_atf.delay(1000);
const [submitBtn] = screen.getAllByRole('button', { name: 'Submit' });
await user.click(submitBtn);
await waitFor(() => {
  const numField = screen.getBySelector('[name="incident.number"]');
  expect(numField.value).toMatch(/^INC/);
}, { timeout: 10000 });
```

## Test as an impersonated user

```
// Accepts a user_name or sys_id. The iframe reloads automatically.
// The original session is always restored when the step ends.
await sn_atf.impersonate('beth.anglin');
await sn_atf.navigate('/now/sow/home');
const listTab = await screen.findByRole('tab', { name: 'List', timeout: 10000 });
await user.click(listTab);
const incidentItem = await screen.findByRole('treeitem', { name: 'Incidents', timeout: 10000 });
expect(incidentItem).toBeVisible();
```

## Upload an attachment to the current form

```
// Pass a sys_id to copy an existing attachment server-side (no file bytes transferred).
// Pass a File object (from sn_atf.getAttachmentFile) to upload through REST.
await sn_atf.navigate('/incident.do?sys_id=' + steps('PREVIOUS_STEP_SYS_ID').record_id);
await sn_atf.upload(steps('PREVIOUS_STEP_SYS_ID').attachment_sys_id);
await screen.findByText('evidence.pdf');
```

## Wait for an async condition by using waitFor

```
await sn_atf.navigate('/incident.do?sys_id=<sys_id>');
await screen.findByRole('heading', { name: /INC/ });
const [updateBtn] = screen.getAllByRole('button', { name: 'Update' });
await waitFor(
  () => expect(updateBtn).toBeEnabled(),
  { timeout: 10000 }
);
```

## Access step outputs and parameter values

```
// steps() retrieves output variables from a prior step by its sys_id.
// params() retrieves parameter values when running a parameterized test.
// Both support dotwalking for reference fields, for example
// steps('...').assigned_to.department.name.
// Use == or String() for comparisons — not ===.
const dept = String(steps('PREVIOUS_STEP_SYS_ID').assigned_to.department.name);
const expected = String(params('expected_department'));
expect(dept == expected).toBe(true);
```

**Note:**

`steps(SYS_ID)` takes the sys\_id of the step record, not the step result. Find it in the URL when you open the step record.

## Verify an element on a classic form

```
await sn_atf.navigate('/incident.do?sys_id=<sys_id>');
const heading = await screen.findByRole('heading', { name: /INC/ });
expect(heading).toBeVisible();
const shortDesc = screen.getByRole('textbox', { name: 'Short description' });
expect(shortDesc).toBeVisible();
```

## Navigate to a record, fill a field, and save

```
await sn_atf.navigate('/incident.do?sys_id=<sys_id>');
await screen.findByRole('heading', { name: /INC/ });
const shortDesc = screen.getByRole('textbox', { name: 'Short description' });
await user.tripleClick(shortDesc);
await user.type(shortDesc, 'Updated by ATF');
const [updateBtn] = screen.getAllByRole('button', { name: 'Update' });
await user.click(updateBtn);
await screen.findByRole('heading', { name: /INC/ });
```

**Note:**

On classic forms, `findByLabelText` can throw a "found multiple elements" error because ServiceNow uses both `<label for>` and `aria-labelledby` associations at the same time. Prefer `getByRole('textbox', { name: '...' })` for text inputs, or `getByRole('searchbox', { name: '...' })` for reference fields. Classic forms also render every action button — Submit, Update, Delete — in both the header and the footer. Use `getAllByRole` and destructure to take the first one.

## Wait for an async condition

Use `waitFor` to poll a condition that is not simply a new element appearing. The callback is retried until it stops throwing or the timeout expires.

```
await sn_atf.navigate('/incident.do?sys_id=<sys_id>');
await screen.findByRole('heading', { name: /INC/ });
const [updateBtn] = screen.getAllByRole('button', { name: 'Update' });
await waitFor(
  () => expect(updateBtn).toBeEnabled(),
  { timeout: 10000 }
);
```

## Test as an impersonated user

```
await sn_atf.impersonate('beth.anglin');
await sn_atf.navigate('/now/sow/home');
const listTab = await screen.findByRole('tab', { name: 'List', timeout: 10000 });
await user.click(listTab);
const incidentItem = await screen.findByRole('treeitem', { name: 'Incidents', timeout: 10000 });
expect(incidentItem).toBeVisible();
```

## Upload an attachment

```
// Copy an existing attachment to the current form (no file bytes transferred)
await sn_atf.navigate('/incident.do?sys_id=<sys_id>');
await sn_atf.upload('<source_attachment_sys_id>');
await screen.findByText('<file_name>;);
```

## Upload to a Workspace record

```
await sn_atf.navigate('/now/sow/record/incident/<sys_id>');
const result = await sn_atf.uploadInWS('<source_attachment_sys_id>');
expect(result.name).toBe('evidence.pdf');
```

## Use step outputs with dotwalking

```
// steps(<step_sys_id>) — use the sys_id shown in the step record's URL
const assigneeDept = String(steps('abc123def456abc123def456abc12345').assigned_to.department.name);
expect(assigneeDept).toBe('IT');
```

## Use parameter set values

```
// In a parameterized test, read values from the active parameter row
await sn_atf.navigate('/incident.do?sys_id=-1');
const shortDesc = screen.getByRole('textbox', { name: 'Short description' });
await user.type(shortDesc, String(params('description')));
const [submitBtn] = screen.getAllByRole('button', { name: 'Submit' });
await user.click(submitBtn);
await waitFor(() => {
  const numField = screen.getBySelector('[name="incident.number"]');
  expect(numField.value).toMatch(/^INC/);
}, { timeout: 10000 });
```

## Use within to scope queries

```
// Scope queries to a specific section of the page to avoid ambiguous matches
const form = screen.getBySelector('form');
const shortDesc = within(form).getByRole('textbox', { name: 'Short description' });
expect(shortDesc).toBeVisible();
```

## Find the visible instance of a duplicated element

```
// The page renders two elements with the same text; find the visible one
const matches = await screen.findAllByText('Number');
const label = matches.find(el => isVisible(el));
expect(label).toBeTruthy();
```

