---
title: State flow cleanup
description: The business rules, client scripts, and UI actions that the system creates automatically to perform custom transitions exist only while the state flow records that use them are present.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/service-management-for-the-enterprise/r\_StateFlowCleanup.html
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [State flow customization, Service management states, Service Management]
---

# State flow cleanup

The business rules, client scripts, and UI actions that the system creates automatically to perform custom transitions exist only while the state flow records that use them are present.

When all the state flows on a table are deleted, the system attempts to delete any unnecessary programming elements that were created on that table, using these criteria:

<table id="table_p4b_lnb_br"><thead><tr><th>

Element

</th><th>

Deleted When

</th></tr></thead><tbody><tr><td>

-   UI action
-   Business rule
-   Dictionary override

</td><td>

The state flow that created it is deleted.

</td></tr><tr><td>

Business rule that processes events triggered by a state flow

</td><td>

All state flows for the table specified that have events configured are deleted.

</td></tr><tr><td>

Client script \(onLoad\)

</td><td>

All state flows for the table are deleted.

</td></tr><tr><td>

Client script \(onChange\)

</td><td>

All state flows with field controls are deleted.

</td></tr><tr><td>

Work notes business rule

</td><td>

All state flows with field controls or work notes are deleted

</td></tr></tbody>
</table>**Parent Topic:**[State flow customization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/service-management-for-the-enterprise/c_StateFlowCustomization.md)

**Related topics**  


[State flow customization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/service-management-for-the-enterprise/c_StateFlowCustomization.md)

[Request states](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/service-management-for-the-enterprise/r_SMRequestStates.md)

[Request task states](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/service-management-for-the-enterprise/r_SMRequestTaskStates.md)

