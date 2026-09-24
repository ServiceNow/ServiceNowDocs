---
title: Update sets transfer between sandboxes and base instance
description: When a sandbox is ready, update set sources are automatically created on both the sandbox and the base instance, enabling transfers in either direction without manual configuration.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/developer-sandboxes/dsb-update-sets.html
release: brazil
product: Developer Sandboxes
classification: developer-sandboxes
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Explore, Developer Sandboxes, Developing your application, Building applications]
---

# Update sets transfer between sandboxes and base instance

When a sandbox is ready, update set sources are automatically created on both the sandbox and the base instance, enabling transfers in either direction without manual configuration.

When a sandbox is ready, two update set sources are automatically created to enable transfer of completed update sets in either direction without manual configuration:

-   On a sandbox, a source named **Base instance** points to the base instance.
-   On the base instance, a source named **Sandbox: \[sandbox name\]** points to the sandbox.

Use these sources with the standard update set process to retrieve, preview, and commit completed update sets from a sandbox to the base instance. You can also use them to transfer from the base instance to a sandbox. For more information on update sets, see [System update sets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/system-update-sets/system-update-sets.md).

When a sandbox is retired, both sources are removed automatically. The base instance source is deleted, and the sandbox source is dropped along with the rest of the sandbox data. No manual cleanup is needed.

**Note:** Source control is the preferred approach for transferring changes between sandbox and base. Update set sources are available as an alternative for teams that use update-set-based workflows.

