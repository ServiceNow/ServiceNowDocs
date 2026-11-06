---
title: Create custom Scan Engine definitions
description: The Scan Engine contains preexisting base system definitions and you can create your own.Platform owners and ServiceNow administrators can create custom health checks using plain language to encode your organization's best practices without as automated health checks without writing code. You don't need scripting expertise or deep knowledge of ServiceNow's data schema, as the AI agent guides you through the entire workflow.Create a custom health check using plain language to encode your organization's best practices and validate it before publishing.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/impact/create-scan-engine-definitions.html
release: australia
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 11
keywords: [health checks, custom checks, AI authoring, best practices, Impact, custom health check, authoring, AI, dry-run]
breadcrumb: [Customize Scan Engine definitions, Activate Scan Engine and review settings, Configuring Impact, Impact]
---

# Create custom Scan Engine definitions

The Scan Engine contains preexisting base system definitions and you can create your own.

## Before you begin

Role required: Scan Engine Admin \(`sn_se.scan_engine_admin`\).

## Procedure

1.  Navigate to **ALL** &gt; **Impact** &gt; **Platform Health** &gt; **Definitions**.

2.  Select **New**.

3.  Fill in the following fields as needed.

<table id="choicetable_p4w_2cx_2hc"><thead><tr><th align="left" id="d50525e103">

Field/Selection

</th><th align="left" id="d50525e106">

Description

</th></tr></thead><tbody><tr><td id="d50525e112">

**Number**

</td><td>

The unique identifier of the definition. This number is generated automatically.**Note:** Your unique company code will be prefixed to the definition number. You can find your company code by navigating to the `sys_properties` table, then searching for `glide.appcreator.company.code` property.

</td></tr><tr><td id="d50525e129">

**Active**

</td><td>

Select to have the Scan Engine evaluate records to see if there are any findings during a scan.

</td></tr><tr><td id="d50525e141">

**Level of Finding**

</td><td>

Select the severity level of the finding for the definition that displays when real-time monitoring is active: -   **Act**: Prevents users from modifying the record until the definition’s conditions are met.
-   **Recommend**: Prevents users from modifying the record unless they provide an exception reason for why the definition was not followed or until the definition's conditions are met.
-   **Suggest**: Prompts users to check if there is a better solution available.
-   **Review**: Calls out less serious items for review. This does not contribute to technical debt.
See [View scan results for Scan Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/viewing-scan-results-scan-engine.md) for additional information.

</td></tr><tr><td id="d50525e181">

**Category**

</td><td>

Upgradeability, manageability, performance, security, or user experienceFor details, see [Customize Scan Engine definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/view-modify-scan-engine-properties.md).

</td></tr><tr><td id="d50525e200">

**Short Description \(Mandatory\)**

</td><td>

A short description of the definition.

</td></tr><tr><td id="d50525e209">

**Reason For Definition**

</td><td>

The purpose the definition was created.

</td></tr><tr><td id="d50525e218">

**Supporting Documentation**

</td><td>

A link to documentation that further explains the finding definition. The link displays as part of the real-time message.

</td></tr></tbody>
</table>4.  On the **Configuration** tab, adjust the values of the following fields to configure how the definition operates and identifies findings within the instance.

<table id="choicetable_kbk_vdx_2hc"><thead><tr><th align="left" id="d50525e239">

Field/Setting

</th><th align="left" id="d50525e242">

Description

</th></tr></thead><tbody><tr><td id="d50525e248">

**Evaluate Definition For**

</td><td>

Dictates the scope of records that are scanned in real-time:-   **All Matching Records**: Scans all applicable records in real-time.
-   **New Records Only**: Scans only new, applicable records in real-time.


</td></tr><tr><td id="d50525e269">

**SN Instance To Run On**

</td><td>

Sets the SN instance that the definition will apply to.-   Run on all non-production instances
-   Run on specified instances
-   Run on production instances only
**Note:** **Run on Specified Instances** activates the **Specific SN Instances to Run On** field.

</td></tr><tr><td id="d50525e296">

**Specific SN Instances to Run On**

</td><td>

-   Sets which specific ServiceNow instances the definition applies to.
-   For this setting to display, the follow must be true:
    -   **Enable Instance Specific Definitions** must be enabled in the Scan Engine properties.
    -   The My SN Instances table must contain at least one instance.
 **Note:** Only instances defined in the My SN Instances table can be selected here.

</td></tr><tr><td id="d50525e330">

**Type of Rule \(Mandatory\)**

</td><td>

Sets the definition’s rule type:-   Fails if script includes text
-   Fails if script excludes text
-   Fail if XML includes text
-   Fail if XML excludes text
-   Fail if conditions match
-   Custom


</td></tr><tr><td id="d50525e361">

**Scan Finding Limit**

</td><td>

-   The maximum number of findings that can be generated for each definition during a scan.
-   The limit is applied per applicable table. Forr example, if the limit is set to 100, a maximum of 100 findings will be generated for each applicable table.
-   Prevents excessive or redundant findings and optimizes scan performance.


</td></tr><tr><td id="d50525e382">

**Propose Fix**

</td><td>

-   Allows a definition to be defined such that it enables the ability to automatically apply recommended changes to objects in your ServiceNow instance.
-   When selected, the **Proposed Fix Script** field displays.


</td></tr><tr><td id="d50525e403">

**Propose Fix Script**

</td><td>

-   Provides a script field for creating a custom function which is used to show users an auto-corrected version of the record they are viewing.
-   This field is only visible if **Propose Fix** is enabled.


</td></tr><tr><td id="d50525e424">

**Search Type \(Mandatory\)**

</td><td>

-   **Regex**: Search by regular expression.
-   **Text**: Search for text.
-   **Custom**: A custom search type using JavaScript.
-   This field is only visible if **Type of Rule** is one of the following:
    -   Fails if script includes text
    -   Fails if script excludes text
    -   Fail if XML includes text
    -   Fail if XML excludes text


</td></tr><tr><td id="d50525e471">

**Custom Rule Variable**

</td><td>

-   Enables the Parameter 1 value string entry field.
-   This field is only visible if **Type of Rule** is set to **Custom**.


</td></tr><tr><td id="d50525e495">

**Parameter 1 Value**

</td><td>

Set a default value here if you want to allow users to change the value of a parameter without modifying a custom script.

</td></tr><tr><td id="d50525e505">

**Parameter 1 Description**

</td><td>

A description of what the Parameter 1 Value is used for.

</td></tr><tr><td id="d50525e514">

**Delta Scans Not Applicable**

</td><td>

This definition will always scan as a full scan, not a delta scan, for all scan types. This means it will scan all records for findings, not just records updated since the previous scan.

</td></tr><tr><td id="d50525e523">

**Return One Finding For The Entire Table**

</td><td>

-   If the definition applies to the entire table and not to specific records, Scan Engine returns one finding record for the table instead of a finding for each record.
-   When possible, the scanned table and scanned record are populated in the finding. If this isn’t possible, the scanned record value will be empty.
 **Note:** If enabled, this definition will not scan in real-time.

</td></tr><tr><td id="d50525e547">

**Search Pattern**

</td><td>

Lets users enter a regular expression to search for findings in Scripts and XML type fields. This field is only available if **Type of Rule** is set to one of the following:

-   Fail if script includes text
-   Fail if script excludes text
-   Fail if XML includes text
-   Fail if XML excludes text
In addition, **Search Type** must be set to **Regex**.

</td></tr><tr><td id="d50525e583">

**Search Function**

</td><td>

Lets users enter a custom function to search for findings in Scripts and XML type fields. This field is only available if **Type of Rule** is set to one of the following:

-   Fail if script includes text
-   Fail if script excludes text
-   Fail if XML includes text
-   Fail if XML excludes text.
In addition, **Search Type** must be set to **Custom**.

</td></tr><tr><td id="d50525e619">

**Search Text**

</td><td>

Enables a field for users to search for text in scripts and XML fields. Enter one or more comma-separated text values.This field is only available if **Type of Rule** is set to one of the following:

-   Fail if script includes text
-   Fail if script excludes text
-   Fail if XML includes text
-   Fail if XML excludes text
In addition, **Search Type** must be set to **Text \(comma separated\)**.

</td></tr><tr><td id="d50525e656">

**Custom Function \(Mandatory\)**

</td><td>

-   Provides a script field to create a custom function for identifying findings.
-   This field is only visible if **Type of Rule** is set to **Custom**.


</td></tr></tbody>
</table>5.  On the **Impact** tab, adjust the values in the following fields as desired to configure the impact level for findings relating to this definition.

<table id="choicetable_y2c_ggx_2hc"><tbody><tr><td id="d50525e692">

**Impact to Instance \(Mandatory\)**

</td><td>

-   Sets a level of impact for the finding within its level of finding. For example, different Act findings can have different impact levels assigned to them. It provides an extra layer of priority for individual definitions.
-   Impacts can be set from 1-10, where 1 is the lowest impact and 10 is the highest.


</td></tr><tr><td id="d50525e710">

**Business Impact**

</td><td>

A description of how a finding for the definition would affect the instance in a business setting.

</td></tr></tbody>
</table>6.  On the **Resolution** tab, adjust the values in the following fields to change how to resolve findings relating to this definition and the estimated time to do so.

<table id="choicetable_hnp_vgx_2hc"><tbody><tr><td id="d50525e732">

**Estimated Time to Resolve Issue**

</td><td>

The estimated time for a single developer to resolve the definition finding in days, hours, minutes, and seconds.

</td></tr><tr><td id="d50525e744">

**Steps To Resolve**

</td><td>

A description of the steps for resolving the finding related to this definition. This description is displayed on real-time messages.

</td></tr></tbody>
</table>7.  Select **Save** in the Additional Actions drop down menu to save the new definition, then configure the Applicable Tables.


**Parent Topic:**[Customize Scan Engine definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/view-modify-scan-engine-properties.md)

## AI definition builder

Platform owners and ServiceNow administrators can create custom health checks using plain language to encode your organization's best practices without as automated health checks without writing code. You don't need scripting expertise or deep knowledge of ServiceNow's data schema, as the AI agent guides you through the entire workflow.

The AI-Assisted Custom Health Check Authoring capability lets you encode your organization's own best practices as automated health checks without writing code or understanding the underlying schema. Using plain language, you describe what you want to check, and an AI agent guides you through authoring, previewing, and publishing a live check.

### Summary

Impact customers have always been able to create custom health checks. Building one meant writing the definition by hand—learning the check format, the query syntax, and the platform tables underneath it. That put custom checks out of reach for most people, and made them slow work for the few who could write them.

The AI Definition Builder removes that manual work. An authorized user describes what they want to monitor in plain language, and the system drafts the check. A new approval workflow then routes it for review before it runs on the instance.

<table id="table_nnj_1qb_lkc"><tbody><tr><td>

Field

</td><td>

Value

</td></tr><tr><td>

Release

</td><td>

Impact Bundle v12.0.0 \(October 2026\)

</td></tr><tr><td>

Product area

</td><td>

Platform Health: Best Practice Checks

</td></tr><tr><td>

Capabilities

</td><td>

CAP36722 \(authoring\), CAP37679 \(approval workflow\)

</td></tr><tr><td>

Audience

</td><td>

Technical writing, go-to-market, product, engineering

</td></tr></tbody>
</table>

What’s new

Create a check by describing it. An authorized user types what they want to check for in their own words. The system drafts the check for them. No syntax, no template to fill in.

The system checks for duplicates first. Before drafting anything, it compares the request against the existing library and points the author to a check that already covers it, rather than creating a near-copy.

Preview before you commit. The draft runs against the live instance in read-only mode and shows a representative sample of the records it would flag. Nothing is logged, tracked, or surfaced as a real finding. The author is approving scope and intent, not responding to actual results.

Review and approval. A check authored by a designated author cannot go live on its own. It moves through a governed workflow: Draft, Pending Approval, then Approved or Rejected. A Scan Engine administrator makes the call.

A full audit trail. Every state change records who acted, when, what action they took, and their comment. Comment history is append-only, so nothing is overwritten.

How the approval flow works

<table id="table_onj_1qb_lkc"><tbody><tr><td>

Step

</td><td>

Who

</td><td>

What happens

</td></tr><tr><td>

Draft

</td><td>

Author

</td><td>

Check is created and edited. Not running on the instance.

</td></tr><tr><td>

Dry Run Validation

</td><td>

System

</td><td>

A dry run is available so the author can validate the check before submitting it for approval.

</td></tr><tr><td>

Pending Approval

</td><td>

System

</td><td>

Check appears in the Pending Definitions list. The approver group is notified.

</td></tr><tr><td>

Approved

</td><td>

Administrator

</td><td>

Check is activated and behaves like any other health check.

</td></tr><tr><td>

Rejected

</td><td>

Administrator

</td><td>

Check moves to a distinct Rejected state.

</td></tr></tbody>
</table>

The author is notified on every state change.

Roles

Scan Engine Definition Author—a new role, assignable to a group. Can create, edit, and submit drafts. Cannot approve or activate definitions, in any configuration.

Scan Engine administrator—the approver. No new role required; this is the existing administrator role. Approves or rejects from the workflow, and can activate approved checks.

The separation is deliberate. Authoring and approving are always two different people.

Where you’ll find it

Authoring starts in Otto, the conversational entry point in Impact. Anyone with the Scan Engine Definition Author role or the Scan Engine administrator role can open Otto and start a definition from there. There is no separate builder page to find and no form to open first.

Two prompts start the work:

Create new scan engine definition — begins a new check. Otto asks what you want to monitor, you answer in your own words, and it drafts the definition from there.

Edit scan engine definition — opens an existing check for revision.

From either prompt, the conversation carries you through drafting, the duplicate check against the existing library, and the dry run validation. When the definition is ready, you submit it for approval from the same place. Scan Engine administrators review submitted checks from a new Pending Approval Definitions entry in the All menu. It opens the definition list filtered to checks awaiting approval, where administrators can approve or reject each one.

That list is the review surface for this release. A dedicated approval queue component on the Impact Health Home and Impact Home \(AI-Native\) pages is a later phase.

[Author a custom health check](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/create-scan-engine-definitions.md)

### Author a custom health check

Create a custom health check using plain language to encode your organization's best practices and validate it before publishing.

#### Before you begin

Role required: \[PLACEHOLDER: confirm required role\]

#### About this task

The custom health check authoring workflow guides you through describing, previewing, refining, and publishing a health check without writing code.

#### Procedure

1.  Describe your check in plain language.

    Write a plain-language description of the health check you want. Example: "Flag all Incidents without a priority assigned."

    The system validates your description against ServiceNow's data schema. It also checks that the check does not duplicate an existing custom check in your instance.

2.  Preview the check with a dry-run.

    Before publishing, review the dry-run preview showing which records your check would find. This lets you validate that the check fires on the right targets and doesn't cast too narrow or too wide a net.

3.  Approve or refine the check.

    After reviewing the dry-run, choose one of the following paths:

    -   Approve: Publish the check as-is. It runs immediately on your instance.
    -   Reject: Discard the draft and start over.
    -   AI-assisted revision: Prompt the agent to refine the check based on what the dry-run showed. For example, "Make the check stricter" or "Only flag records older than 30 days."
    -   Manual editing: Edit the check definition directly in the YAML editor, then re-run the dry-run or publish.
4.  Publish and monitor the check.

    Once published, your custom check runs on a schedule you define and findings appear in the standard \[PLACEHOLDER: confirm surface name - "Impact," "Health platform," or other\] results alongside all other checks. Your check counts toward your organization's custom check limit.


