---
title: Code quality rules list in RPA Hub
description: View a list of pre-defined rules that RPA admins can set for the RPA developers to follow as a code quality standard.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Code quality check, Use, RPA Hub, Workflow Data Fabric]
---

# Code quality rules list in RPA Hub

View a list of pre-defined rules that RPA admins can set for the RPA developers to follow as a code quality standard.

<table id="table_ucf_k2x_2rb"><thead><tr><th>

 

</th><th>

Name of the rule

</th><th>

Description

</th></tr></thead><tbody><tr><td>

CQR0011

</td><td>

Activity naming convention

</td><td>

Inspects if the activities naming convention is as per the defined Regular expression.

</td></tr><tr><td>

CQR0002

</td><td>

Empty activities

</td><td>

Inspects if there are any empty activities in the automation.

</td></tr><tr><td>

CQR0005

</td><td>

Hard-coded passwords

</td><td>

Inspects if there are any hard-coded passwords in the automation.

</td></tr><tr><td>

CQR0009

</td><td>

Infinite loop

</td><td>

Inspects the possibility of an infinite loop sequence in the automation.

</td></tr><tr><td>

CQR0012

</td><td>

Nested activities

</td><td>

Inspects if the depth of nested activities is as per the defined value. Activities are nested when you add another activity within the activity.

For example, if 'Activity A' calling 'Activity B', 'Activity B' calling 'Activity C', and so on.

</td></tr><tr><td>

CQR0006

</td><td>

Startup activity

</td><td>

Inspects if an activity is marked as the start activity for the automation.

</td></tr><tr><td>

CQR0001

</td><td>

Try Catch - Exception handling

</td><td>

Inspects if the 'On Error' and 'Error Message' output ports of the Try Catch component are not used in the automation.

</td></tr><tr><td>

CQR0003

</td><td>

Unreferenced activities

</td><td>

Inspects if there are any activities that are not referenced in the automation.

</td></tr><tr><td>

CQR0004

</td><td>

Unused components

</td><td>

Inspects if there are any components that are not referenced in the automation.

</td></tr><tr><td>

CQR0008

</td><td>

Unused plugins or user plugins

</td><td>

Inspects if there are any plugins or user plugins that are not referenced in the automation.

</td></tr><tr><td>

CQR0007

</td><td>

Unused variables or global objects

</td><td>

Inspects if there any variables or global objects that are not referenced in the automation.

</td></tr><tr><td>

CQR0010

</td><td>

Variable naming convention

</td><td>

Inspects if the variables naming convention is as per the defined Regular expression.

</td></tr></tbody>
</table>**Parent Topic:**[Code quality check in RPA Hub](../concept/code-quality-check-rpa.md)

**Related topics**  


[Code quality check in RPA Hub](../concept/code-quality-check-rpa.md)

[View the code quality rules list in RPA Hub](../task/view-cqr-rpa.md)

[Code quality rule form in RPA Hub](../task/edit-cqr-rpa.md#)

