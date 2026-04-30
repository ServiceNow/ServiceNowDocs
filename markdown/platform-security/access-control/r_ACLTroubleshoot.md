---
title: ACL troubleshooting reference
description: ACL troubleshooting includes identifying ACL rule errors and use the debugging tools to fix the ACL related problems.
locale: en-US
release: xanadu
product: Access Control
classification: access-control
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [ACL debugging tools, Advanced ACL configuration, Access Control List Rules, Access Management]
---

# ACL troubleshooting reference

ACL troubleshooting includes identifying ACL rule errors and use the debugging tools to fix the ACL related problems.

## Access analyzer

Access analyzer helps the administrators to view permissions for the selected user, role, or group. It is a diagnostic security tool that provides comprehensive visibility into resource permissions and access controls at the Access Control List \(ACL\) level, enabling you to understand who has access to their resources, identify overly permissive configurations, and maintain least-privilege access principles. To learn more about how to use the tool, see [Access Analyzer](../../../integrate/identity/concept/access-analyzer.md).

## Enable debugging

Enable debugging to help troubleshoot an issue.

|Error or symptom|Solution|
|----------------|--------|
|You cannot access records from a custom table.|Create a table ACL rule for the custom table granting users access to the table. Without an explicit table ACL rule, users must pass the permissions in the table wildcard \(\*\) ACL rule, which by default restricts access to administrators only. Enable [debugging](../concept/c_AccessControlRulesDebug.md) and determine what ACL rules are evaluated for the custom table.|
|You create a custom ACL rule that does not work properly.|The most likely problems are that another rule takes precedence over your custom rule in the processing order or that the user does not meet all the permission requirements for the object type. Enable [debugging](../concept/c_AccessControlRulesDebug.md) and verify that the ACL rule is being evaluated.|
|Your field ACL rule does not work properly.|There is likely a table ACL rule that the user has not met. Enable [debugging](../concept/c_AccessControlRulesDebug.md) and determine what ACL rules are evaluated for the field. Verify that there is not a conflicting table ACL rule or duplicate field ACL rule.|
|Your table ACL rule does not work properly.|There is either an ACL rule higher in the processing order or a duplicate table ACL rule interfering with the table ACL rule. Enable [debugging](../concept/c_AccessControlRulesDebug.md) and determine what ACL rules are evaluated for the table.|
|You can see a field in a list but not in form.|It is possible that the ACL rule conditions or script are being triggered in the list but not in the form. Enable [debugging](../concept/c_AccessControlRulesDebug.md) and determine when the ACL rules evaluate to true. Update the conditions or script to have the same behavior on the list and form.|
|You receive an error message when trying to execute a processor or client-callable script include.|There is an ACL rule for the processor or client-callable script include that the user has not met. If the user should have access to the object, enable [debugging](../concept/c_AccessControlRulesDebug.md) and determine what ACL rules are evaluated for the processor or script include. Update the ACL rule or the user roles as needed to access the object.|

