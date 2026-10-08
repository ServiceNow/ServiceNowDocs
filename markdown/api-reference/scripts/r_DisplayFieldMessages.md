---
title: Display field messages
description: Rather than use JavaScript alert\(\), for a cleaner look, you can display an error on the form itself. The methods showFieldMsg\(\) and hideFieldMsg\(\) can be used to display a message just below the field itself.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/scripts/r\_DisplayFieldMessages.html
release: brazil
product: Scripts
classification: scripts
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Write client-side scripts, Scripting, API implementation, API implementation and reference]
---

# Display field messages

Rather than use JavaScript alert\(\), for a cleaner look, you can display an error on the form itself. The methods showFieldMsg\(\) and hideFieldMsg\(\) can be used to display a message just below the field itself.

showFieldMsg and hideFieldMsg are methods that can be used with the *g\_form* object.

These methods are used to change the form view of records \(Incident, Problem, and Change forms\). These methods may also be available in other client scripts, but must be tested to determine whether they work as expected.

When a field message is displayed on a form on load, the form scrolls to ensure that the field message is visible. Ensuring that users do not miss a field message because it was off the screen.

The global property *glide.ui.scroll\_to\_message\_field* controls automatic message scrolling when the form field is offscreen \(scrolls the form to the control or field\).

<table id="table_bgp_bwq_bp"><thead><tr><th>

Method Detail

</th><th>

Parameters

</th><th>

Example

</th></tr></thead><tbody><tr><td>

showFieldMsg\(input, message, type, \[scrollform\]\)

</td><td>

-   input — name of the field or control
-   message — message you would like to appear
-   type — 'info', 'error', or 'warning'; defaults to info if not supplied
-   scroll form — \(optional\) Set scrollForm to false to prevent scrolling to the field message offscreen

</td><td>

Error message```javascript
g_form.showFieldMsg('impact','Low impact not allowed with High priority','error');
```

\[Omitted image "ShowFieldMsgError.png"\] Alt text: Low impact not allowed with high priority message.

Informational message

```javascript
g_form.showFieldMsg('impact', 'Low impact response time can be one week','info');
//or this defaults to info type
//g_form.showFieldMsg('impact', 'Low impact response time can be one week');
```

\[Omitted image "ShowFieldMsgInfo.png"\] Alt text: Low impact response time can be one week message.

</td></tr><tr><td>

hideFieldMsg\(input\)

</td><td>

-   input — name of the field or control
-   clearAll — \(optional\) boolean parameter indicating whether to clear all messages. If true, all messages for the field are cleared. If false or empty, only the first message is removed

</td><td>

Removing a message```javascript
//this will clear the first message printed to the field
g_form.hideFieldMsg('impact');
```

</td></tr></tbody>
</table>## Legacy support

The showErrorBox\(\) and hideErrorBox\(\) methods are not recommended.

**Parent Topic:**[Writing client-side scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/client-side-scripting-overview.md)

