---
title: Change Management integration with Software Asset Management
description: The Change Management integration with Software Asset Management \(SAM\) displays the projected licensing cost implication of a change.
locale: en-US
release: australia
product: Change Management
classification: change-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Change management integrations, Reference, Change Management, IT Service Management]
---

# Change Management integration with Software Asset Management

The Change Management integration with Software Asset Management \(SAM\) displays the projected licensing cost implication of a change.

This integration focuses on the projected license cost change when a change is proposed to one or more configuration item \(CI\) processor resources \(CPU or CPU Core\) running software licensed by the processor.

This integration requires the Software Asset Management Professional \(com.snc.samp\) and Change Management - License Change Projections \(com.sn\_samp\_change\) plugins.

**Note:** You need to request the activation of the Change management – License Change Projections plugin \(com.sn\_samp\_change\) through the HI Service Portal.

When a change request is in the **New** state, users can propose a change to the CPU or CPU Cores of a CI using **Propose Change** or **Mass Update CI**. Those proposed changes are captured in an XML field that is then passed to Software Asset Management when the change request transitions into its first approval state. Once Software Asset Management performs the projected licensing cost change, those results are displayed in a new form section called License change projection.

The License change projection form section displays the license projection change summary for every CI in scope for the change. The left side of the section displays fields relaying the current spend, projected spend, the spend change, and the number of impacted installations. On the right is a bar graph providing a visual representation of that information.

For a more detailed breakdown of the license change projections, a related list can be added to the Change Request form called **CI Projection Summary**. This related list provides a CI-by-CI breakdown of the license change projection summary information and provides easy access to the Software Asset Management CI Project Summary record and additional data.

**Parent Topic:**[Change management integrations](change-mgmt-integrations.md)

**Related topics**  


[Managing proposed changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/c_ProposedChanges.md)

[Mass Update CI](bulk-ci-change.md)

