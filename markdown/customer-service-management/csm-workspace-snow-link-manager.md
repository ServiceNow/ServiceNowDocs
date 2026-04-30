---
title: Organize records tabs with ServiceNow Link Manager
description: Use the ServiceNow Link Manager feature to manage and organize browser tabs within a ServiceNow instance.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-11-12"
reading_time_minutes: 2
breadcrumb: [CSM Configurable Workspace features, CSM Configurable Workspace, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Organize records tabs with ServiceNow Link Manager

Use the ServiceNow Link Manager feature to manage and organize browser tabs within a ServiceNow instance.

The ServiceNow Link Manager feature is designed to enhance user productivity by managing and organizing browser tabs within a ServiceNow instance. This feature ensures that links opened within an instance are consolidated into a single workspace. It is supported on the latest versions of Google Chrome, Microsoft Edge, and Mozilla Firefox. ServiceNow Link Manager is useful for users who need to keep track of numerous open tabs during their workday.

## Key features

ServiceNow Link Manager includes the following features:

-   **Tab consolidation**: Automatically consolidates new ServiceNow-related tabs into an existing open ServiceNow tab, preventing browser clutter.
-   **Cross-platform support**: Supports opening shared record links across environments such as Gmail, Microsoft Teams, Microsoft Outlook, and other web platforms linked to ServiceNow.
-   **User-friendly interface**: Easy to enable and disable directly from the Chrome extension settings in the browser.

## Frequently Asked Questions

<table id="table_xbc_wcb_jdc"><thead><tr><th>

Question

</th><th>

Answer

</th></tr></thead><tbody><tr><td>

What happens if I turn off ServiceNow Link Manager?

</td><td>

Turning off ServiceNow Link Manager reverts to the default behavior, where each clicked link opens a new tab.

</td></tr><tr><td>

Is the extension available on other browsers?

</td><td>

The extension is currently supported across multiple browsers - Google Chrome, Mozilla Firefox, and Microsoft Edge.

</td></tr><tr><td>

If I have several tabs open and then enable the ServiceNow Link Manager, what will happen?

</td><td>

The existing tabs remain unchanged. Any new links open within the most recent tab in your current workspace.

</td></tr><tr><td>

Can I choose which tabs to consolidate or does ServiceNow Link Manager automatically consolidate all ServiceNow tabs?

</td><td>

ServiceNow Link Manager automatically consolidates all ServiceNow-related tabs. There is currently no option available to select specific tabs for consolidation.

</td></tr><tr><td>

Does ServiceNow Link Manager affect my non-ServiceNow tabs?

</td><td>

No. ServiceNow Link Manager only affects ServiceNow-related tabs. Non-ServiceNow tabs continue to function as usual.

</td></tr><tr><td>

Will ServiceNow Link Manager slow down my browser performance?

</td><td>

ServiceNow Link Manager is designed to operate efficiently without significantly impacting your browser’s performance. However, if you experience any slowdowns, consider limiting the number of active extensions or tabs.

</td></tr><tr><td>

Can I temporarily disable ServiceNow Link Manager without uninstalling the extension?

</td><td>

Yes, you can easily toggle ServiceNow Link Manager on or off from the extension settings without uninstalling the entire extension.

</td></tr><tr><td>

If I am working with multiple ServiceNow instances, can I customize which instance ServiceNow Link Manager consolidates tabs into?

</td><td>

Currently, ServiceNow Link Manager consolidates tabs within each ServiceNow instance independently. If you have multiple instances open, the link will open in the most recently used instance.

</td></tr><tr><td>

Does the extension work with customized URLs or older browser versions?

</td><td>

ServiceNow Link Manager extension works only with base system workspace URL patterns and doesn’t support customized URLs. It currently supports the following patterns:**CSM workspaces:**

```
"patterns": [
              { 
                "name": "cwf",
                "match": "https://*/now/cwf/*" 
              },
```

**ITSM workspace:**

```
"patterns": [
              { 
                "name": "sow",
                "match": "https://*/now/sow/*" 
              }
```

**Note:** The extension doesn’t work on older browser versions that don't support Manifest V3. Make sure you're using the latest version of Google Chrome, Microsoft Edge, or Mozilla Firefox.

</td></tr><tr><td>

What happens to filters when opening a filtered list URL through ServiceNow Link Manager?

</td><td>

When a filtered list URL redirects to an existing workspace tab, the applied filters are not preserved. The list displays all records, and you must manually reapply filters after the page loads. For more details, see [\[Now Link Browser Extension\] - List Configuration are not working as expected with NowLink Manager](https://support.servicenow.com/kb?id=kb_article_view&sys_kb_id=52faebad471d72d048cb2920326d4365)

</td></tr></tbody>
</table>