---
title: Mass Update CI
description: The Mass Update CI plugin enable users to apply the same update to a set of CIs for a specific CI class. The Change Management - Mass Update CI plugin is intended to be used when the Change Management - State Model plugin is activated.
locale: en-US
release: australia
product: Change Management
classification: change-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Process a change request, Use, Change Management, IT Service Management]
---

# Mass Update CI

The Mass Update CI plugin enable users to apply the same update to a set of CIs for a specific CI class. The Change Management - Mass Update CI plugin is intended to be used when the Change Management - State Model plugin is activated.

To use these features, activate the Change Management - Mass Update CI plugin.

**Note:** This feature is available for normal and emergency changes only.

When you activate the Change Management - Mass Update CI plugin, the **Mass update CI class** check box appears on the Change Request form. When selected, the **Mass update CI class** tab appears and allows changes to be proposed against the configuration items that match that class associated with the affected CI’s related list in that change.

When the change moves to the Implement state, the required update for each CI related to the Change Request is created. These updates can then be applied in the Implement or Review state.

**Note:** You cannot add or delete a CI when the change request in the **In-progress** state and is not approved.

**Parent Topic:**[Process a change request](../task/t_ProcessAChangeRequest.md)

**Related topics**  


[Activate Change Management - Mass Update CI](../task/t_ActivateChangeManagementBulkCI.md)

[Associate multiple CIs with a change request](c_AffectedCIsAndImpactedServices.md#)

[Legacy: State model and transitions](c_ChangeStateModel.md)

[Configure a form](https://www.servicenow.com/docs/access?context=configure-form-layout&version=australia&pubname=australia-platform-administration&ft:locale=en-US)

