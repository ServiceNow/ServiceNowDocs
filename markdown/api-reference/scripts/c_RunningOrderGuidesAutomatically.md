---
title: Running order guides automatically
description: Service catalog order guides allow customers to make a single service catalog request that can generate several ordered items. Administrators can configure order guides to run automatically, from a workflow or a script to generate a set of ordered items without manually submitting a service catalog request. Administrators can also review and reprocess the order guide failures.Running order guides with a server-side script is more complex than using workflows, but it allows more flexibility and can be used in non-workflow situations.Running an order guide from a workflow is suitable if you include order guides as part of a broader workflow-based process.Order guide processing can fail, for example if the order guide being run does not exist. When a failure occurs during the order guide processing, the Scriptable Order Guide Failures submodule allows you to review and reprocess the failures. A record is created for each failure and once you fix the errors that caused the initial failure, you can reprocess the failed order guides.
locale: en-US
release: australia
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Server-side scripting, Scripting, API implementation, API implementation and reference]
---

# Running order guides automatically

Service catalog order guides allow customers to make a single service catalog request that can generate several ordered items. Administrators can configure order guides to run automatically, from a workflow or a script to generate a set of ordered items without manually submitting a service catalog request. Administrators can also review and reprocess the order guide failures.

As a use case, an onboarding workflow for a new employee can run an order guide to automatically order items for that employee.

**Note:** You can only save catalog items, not the order guide \(that is, initial landing page options\).

**Parent Topic:**[Server-side scripting](c_ServerScripting.md)

## Running order guides from scripts

Running order guides with a server-side script is more complex than using workflows, but it allows more flexibility and can be used in non-workflow situations.

For example, you can use order guide scripts with UI actions or server-side business rules.

**Note:** When order guides run automatically, order guide UI policies are not enforced. Also, options in the Choose Options screen cannot be selected, so make sure that order guide rules define sensible defaults for these options to avoid processing failures.

Use the SNC.ScriptableOrderGuide Java class to run order guides with a script.

Use the SNC.ScriptableOrderGuide\(String orderGuideId\) constructor to create a new ScriptableOrderGuide object.

### Method summary

<table id="table_uzq_cdf_mp"><thead><tr><th>

Method

</th><th>

Return Value

</th><th>

Description

</th></tr></thead><tbody><tr><td>

process\(String json\)

</td><td>

boolean

</td><td>

Runs the order guide using the JSON encoded string parameter as the input for the order guide. Returns true or false depending on whether processing was successful or not.**Note:** Both **opened\_by** and **requested\_for** parameters must be passed to the order guide, and both must have valid user record sys\_id values.

 If processing is successful and a request is created by the order guide, you can retrieve the request GlideRecord using getRequest\(\).

 If the processing fails, you can retrieve the failure GlideRecord using getFailure\(\), then submit the script for reprocessing using reprocess.

</td></tr><tr><td>

reprocess\(GlideRecord failure\)

</td><td>

boolean

</td><td>

Runs the order guide again using the JSON encoded string parameter stored in the failure GlideRecord.

</td></tr><tr><td>

getMessage\(\)

</td><td>

String

</td><td>

Retrieves the message populated after processing or reprocessing.

</td></tr><tr><td>

getRequest\(\)

</td><td>

GlideRecord

</td><td>

Retrieves the request GlideRecord.

</td></tr><tr><td>

getFailure\(\)

</td><td>

GlideRecord

</td><td>

Retrieves the failure GlideRecord from the Scriptable Order Guide Failures \[sc\_script\_order\_guide\_failure\] table.

</td></tr></tbody>
</table>### Script example

This script processes an order guide called IT Onboarding SOG.

```
// Creating the object to later be JSON encoded 
var json = {"opened_by":"62826bf03710200044e0bfc8bcbe5df1","requested_for":"06826bf03710200044e0bfc8bcbe5d8a","department":"221f3db5c6112284009f4becd3039cc9"};
 
var now_GR = new GlideRecord("sc_cat_item_guide");
if (gr.get("name","IT Onboarding SOG")) {
  var sog = new SNC.ScriptableOrderGuide(gr.getValue("sys_id"));
  var result = sog.process(new JSON().encode(json));
  if(!result)
    gs.log("Processing the scriptable order guide failed with message: " + sog.getMessage());
  else { 
    var request = sog.getRequest();
    gs.log("Request created - " + request.sys_id); } }
```

## Running order guides from workflows

Running an order guide from a workflow is suitable if you include order guides as part of a broader workflow-based process.

For example, an activity within an onboarding workflow for a new employee can automatically run an order guide to order items for that employee.

**Note:** When order guides run automatically, order guide UI policies are not enforced. Also, options in the Choose Options screen cannot be selected, so make sure that order guide rules define sensible defaults for these options to avoid processing failures.

To run order guides from a workflow, use the **Scriptable Order Guide** workflow activity.

<table id="table_kcr_hbf_mp"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Order Guide

</td><td>

The name of the order guide that this activity processes. For example, **Example Employee Onboarding IT**.

</td></tr><tr><td>

Script

</td><td>

A script passing information to the order guide. This information is sent as a JSON encoded string parameter assigned to the *answer* variable.The script must meet these requirements:

-   The names of the variables in the script must match the names used within the order guide. For example, if the order guide uses a *department* variable in a rule condition, the script must also pass a **department** parameter.
-   Both **opened\_by** and **requested\_for** parameters must be passed to the order guide, and both must have valid user record sys\_id values.

</td></tr></tbody>
</table>### Results

-   **Success**: the activity successfully processed the order guide. This does not mean a request was created. If a request was created, the request sys\_id is added to the workflow scratchpad under the *sc\_request* variable.
-   **Failure**: while processing the order guide a failure occurred, creating a failure record. If the processing fails, you can view and edit the failure record.

### Workflow example

The **Example Employee Onboarding IT Workflow** workflow uses this example to generate IT catalog items for a new employee as part of an onboarding process.

The activity uses this script to:

1.  Take a JSON string generated previously from the HR change record.
2.  Append the mandatory **opened\_by** and **requested\_for** parameters to that string.
3.  Submit the new string for processing by the order guide.

```
var parameters  = new JSON().decode(current.payload);
 
// Need to amend the json object to include additional values.
parameters.opened_by = current.opened_by + "";
parameters.requested_for = current.opened_for + "";
 
answer = new JSON().encode(parameters);
```

## View order guide failures

Order guide processing can fail, for example if the order guide being run does not exist. When a failure occurs during the order guide processing, the **Scriptable Order Guide Failures** submodule allows you to review and reprocess the failures. A record is created for each failure and once you fix the errors that caused the initial failure, you can reprocess the failed order guides.

### About this task

If a failure occurs, a failure record is created in the Scriptable Order Guide Failures \[sc\_script\_order\_guide\_failure\] table.

To view details of a failure, navigate to **Service Catalog** &gt; **Catalog Administration** &gt; **Scriptable Order Guide Failures**, then open a failure record.

Reprocessing failures: If you have fixed the error that caused the initial failure, you can reprocess failed order guides.

### Procedure

1.  Navigate to **Service Catalog** &gt; **Catalog Administration** &gt; **Scriptable Order Guide Failures**.

2.  Open the failure record.

3.  Click the **Reprocess** related link.

    To reprocess one or more failures:

    1.  Navigate to **Service Catalog** &gt; **Catalog Administration** &gt; **Scriptable Order Guide Failures**.
    2.  Select the check box beside one or more records to reprocess.
    3.  Select **Reprocess** from the **Actions** choice list.

