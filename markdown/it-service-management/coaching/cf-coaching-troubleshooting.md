---
title: Resolve Coaching issues
description: Resolve common issues when setting up or running Coaching.
locale: en-US
release: australia
product: Coaching
classification: coaching
topic_type: reference
last_updated: "2026-04-04"
reading_time_minutes: 1
breadcrumb: [Reference, Coaching, IT Service Management]
---

# Resolve Coaching issues

Resolve common issues when setting up or running Coaching.

<table id="table_xgp_zw4_sfb"><thead><tr><th>

Issue

</th><th>

Resolution

</th></tr></thead><tbody><tr><td>

Error after creating a coaching opportunity:`You must create a business rule for a non-task type source table to trigger a coaching assessment. For more information, refer to http://servicenow.com/docs/?context=CSHelp:Coaching-Non-Task-Table.`

</td><td>

Create a business rule to initiate the coaching process for a non-task type table. **Copy the Coaching Opportunity creator for Task business rule and modify it for tables that do not extend Task.**

</td></tr><tr><td>

A coaching assessment is not automatically closed after the due date has passed.

</td><td>

Deactivate the **Close assessments after expiration** scheduled job in **System Definition** &gt; **Scheduled Jobs**.

</td></tr><tr><td>

Coaching assessment is not created.

</td><td>

These resolutions are applicable to a coaching assessment not being created:-   Add the trainee as a member of the trainee group.
-   Clear the **Prevent duplicate assessment** check box if the trainee already has a coaching assessment for the same coaching opportunity.
-   Include the trainee in the **Users who should be coached on every opportunity** list when the **Random sample \(%\)** is less than 100.

</td></tr><tr><td>

You want to override ACLs and trainings for the Assigned Training related list on the Coaching Opportunity and Coaching Assessment forms.

</td><td>

Implement Coaching [extension points](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/extension-points.md):-   CoachingExtensionPoint
-   CoachingACLExtensionPoint

</td></tr></tbody>
</table>**Parent Topic:**[Coaching reference](cf-coaching-reference.md)

**Related topics**  


[Using extension points to extend application functionality](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/extension-points.md)

[Using scripted extension points in server-side scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/scripted-extension-points.md)

[Using UI extension points in server-side UI macros](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/ui-extension-points.md)

[Using client extension points in client-side UI scripting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/client-extension-points.md)

