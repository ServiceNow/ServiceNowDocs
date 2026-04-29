---
title: Create custom Scan Engine definitions
description: The Scan Engine contains preexisting base system definitions. However, if your organization has specific scanning needs not met by these definitions, you can create your own.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Scan Engine definitions, Scan Engine, Platform Health, Using Impact, Impact]
---

# Create custom Scan Engine definitions

The Scan Engine contains preexisting base system definitions. However, if your organization has specific scanning needs not met by these definitions, you can create your own.

## Before you begin

Role required: Scan Engine Admin \(`sn_se.scan_engine_admin`\).

**Note:** Guided customers can only have 10 active custom definitions in a single instance. Definitions above that number will be disabled anytime a scan is executed. Total customers \(as well as Guided customers with the Platform Health add-on\) may have unlimited active custom definitions in a single instance.

## Procedure

1.  Navigate to **ALL** &gt; **Impact** &gt; **Platform Health** &gt; **Definitions**.

2.  Select **New**.

3.  Fill in the following fields as needed.

<table id="choicetable_p4w_2cx_2hc"><thead><tr><th align="left" id="d59991e106">

Field/Selection

</th><th align="left" id="d59991e109">

Description

</th></tr></thead><tbody><tr><td id="d59991e115">

**Number**

</td><td>

The unique identifier of the definition. This number is generated automatically.**Note:** Your unique company code will be prefixed to the definition number. You can find your company code by navigating to the `sys_properties` table, then searching for `glide.appcreator.company.code` property.

</td></tr><tr><td id="d59991e132">

**Active**

</td><td>

Select to have the Scan Engine evaluate records to see if there are any findings \(issues\) during a scan.

</td></tr><tr><td id="d59991e144">

**Level of Finding**

</td><td>

Select the severity level of the finding for the definition that displays when real-time monitoring is active: -   **Act**: Prevents users from modifying the record until the definition’s conditions are met.
-   **Recommend**: Prevents users from modifying the record unless they provide an exception reason for why the definition was not followed or until the definition's conditions are met.
-   **Suggest**: Prompts users to check if there is a better solution available.
-   **Review**: Calls out less serious items for review. This does not contribute to technical debt.


</td></tr><tr><td id="d59991e175">

**Category**

</td><td>

The category of the definition: -   **Upgradeability**: Assesses the ease of enhancing a ServiceNow instance or application with new features, improvements, security patches, or compatibility adjustments.
-   **Manageability**: Measures the extent to which ServiceNow instances, applications, or infrastructure can be effectively monitored, configured, and maintained.
-   **Performance**: Measures the efficiency of a ServiceNow instance, encompassing aspects such as speed, responsiveness, resource utilization, and overall dependability.
-   **Security**: Measures implementation of protocols across a ServiceNow instance to prevent unauthorized access, data breaches, cyber-attacks, and potential vulnerabilities.
-   **User Experience**: Evaluates the quality of user interactions with applications, considering ease of use, efficiency, design, responsiveness, accessibility, and its emotional and functional impact.


</td></tr><tr><td id="d59991e212">

**Short Description \(Mandatory\)**

</td><td>

A short description of the definition.

</td></tr><tr><td id="d59991e221">

**Reason For Definition**

</td><td>

Why the definition was created.

</td></tr><tr><td id="d59991e230">

**Supporting Documentation**

</td><td>

A link to documentation that further explains the reason for the definition. The link displays as part of the real-time message.

</td></tr></tbody>
</table>4.  On the **Configuration** tab, adjust the values of the following fields as desired to configure how the definition operates and identifies findings within the instance.

<table id="choicetable_kbk_vdx_2hc"><thead><tr><th align="left" id="d59991e251">

Field/Setting

</th><th align="left" id="d59991e254">

Description

</th></tr></thead><tbody><tr><td id="d59991e260">

**Evaluate Definition For**

</td><td>

Dictates the scope of records that are scanned in real-time:-   **All Matching Records**: Scans all applicable records in real-time.
-   **New Records Only**: Scans only new, applicable records in real-time.


</td></tr><tr><td id="d59991e281">

**SN Instance To Run On**

</td><td>

Sets the SN instance that the definition will apply to.-   Run on all sub-production instances
-   Run on specified instances
-   Run on production instance\(s\) only
**Note:** **Run on Specified Instances** activates the **Specific SN Instances to Run On** field.

</td></tr><tr><td id="d59991e308">

**Specific SN Instances to Run On**

</td><td>

-   Sets which specific ServiceNow instances the definition applies to.
-   For this setting to display, the follow must be true:
    -   **Enable Instance Specific Definitions** must be enabled in the Scan Engine properties.
    -   The My SN Instances table must contain at least one instance.
 **Note:** Only instances defined in the My SN Instances table can be selected here.

</td></tr><tr><td id="d59991e342">

**Type of Rule \(Mandatory\)**

</td><td>

Sets the definition’s rule type:-   Fails if script includes text
-   Fails if script excludes text
-   Fail if XML includes text
-   Fail if XML excludes text
-   Fail if conditions match
-   Custom


</td></tr><tr><td id="d59991e373">

**Scan Finding Limit**

</td><td>

-   The maximum number of findings that can be generated for each definition during a scan.
-   The limit is applied per applicable table — for example, if the limit is set to 100, a maximum of 100 findings will be generated for each applicable table.
-   Prevents excessive or redundant findings and optimizes scan performance.


</td></tr><tr><td id="d59991e394">

**Propose Fix**

</td><td>

-   Allows a definition to be defined such that it enables the ability for it to automatically apply recommended changes to objects in ServiceNow.
-   When selected, the **Proposed Fix Script** field displays.
 **Note:** To use this functionality, you must either purchase the Impact Total package or the Platform Health add-on.

</td></tr><tr><td id="d59991e418">

**Propose Fix Script**

</td><td>

-   Provides a script field for creating a custom function which is used to show users an auto-corrected version of the record they are viewing.
-   This field is only visible if **Propose Fix** is enabled.


</td></tr><tr><td id="d59991e439">

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


</td></tr><tr><td id="d59991e486">

**Custom Rule Variable**

</td><td>

-   Enables the Parameter 1 value string entry field.
-   This field is only visible if **Type of Rule** is set to **Custom**.


</td></tr><tr><td id="d59991e510">

**Parameter 1 Value**

</td><td>

Set a default value here if you want to allow users to be able to change the value of a parameter without modifying a custom script.**Note:** This field is only visible if **Custom Rule** is **Enabled**.

</td></tr><tr><td id="d59991e528">

**Parameter 1 Description**

</td><td>

A description of what the Parameter 1 Value is used for.**Note:** This field is only visible if **Type of Rule** is set to **Custom**.

</td></tr><tr><td id="d59991e545">

**Delta Scans Not Applicable**

</td><td>

This definition will always scan as a full scan, not a delta scan, for all scan types. This means it will scan all records for findings, not just records updated since the previous scan.

</td></tr><tr><td id="d59991e554">

**Return One Finding For The Entire Table**

</td><td>

-   If the definition doesn't apply to specific records within the table, but rather the entire table, the Scan Engine returns one finding record for the table instead of a finding for each record.
-   When possible, the scanned table and scanned record are populated in the finding. If this isn’t possible, the scanned record value will be empty.
 **Note:** If enabled, this definition will not scan in real-time.

</td></tr><tr><td id="d59991e578">

**Search Pattern**

</td><td>

Lets users enter a regular expression to search for findings in Scripts and XML type fields. This field is only available if **Type of Rule** is set to one of the following:

-   Fail if script includes text
-   Fail if script excludes text
-   Fail if XML includes text
-   Fail if XML excludes text
In addition, **Search Type** must be set to **Regex**.

</td></tr><tr><td id="d59991e614">

**Search Function**

</td><td>

Lets users enter a custom function to search for findings in Scripts and XML type fields. This field is only available if **Type of Rule** is set to one of the following:

-   Fail if script includes text
-   Fail if script excludes text
-   Fail if XML includes text
-   Fail if XML excludes text.
In addition, **Search Type** must be set to **Custom**.

</td></tr><tr><td id="d59991e650">

**Search Text**

</td><td>

Enables a field for users to search for text in scripts and XML fields. Enter one or more comma-separated text values.This field is only available if **Type of Rule** is set to one of the following:

-   Fail if script includes text
-   Fail if script excludes text
-   Fail if XML includes text
-   Fail if XML excludes text
In addition, **Search Type** must be set to **Text \(comma separated\)**.

</td></tr><tr><td id="d59991e687">

**Custom Function \(Mandatory\)**

</td><td>

-   Provides a script field to create a custom function for identifying findings.
-   This field is only visible if **Type of Rule** is set to **Custom**.


</td></tr></tbody>
</table>5.  On the **Impact** tab, adjust the values in the following fields as desired to configure the impact level for findings relating to this definition.

<table id="choicetable_y2c_ggx_2hc"><tbody><tr><td id="d59991e723">

**Impact to Instance \(Mandatory\)**

</td><td>

-   Sets a level of impact for the finding within its level of finding. For example, different Act findings can have different impact levels assigned to them. It provides an extra layer of priority for individual definitions.
-   Impacts can be set from 1-10, where 1 is the lowest impact and 10 is the highest.


</td></tr><tr><td id="d59991e741">

**Business Impact**

</td><td>

A description of how a finding for the definition would affect the instance in a business setting.

</td></tr></tbody>
</table>6.  On the **Resolution** tab, adjust the values in the following fields to change how to resolve findings relating to this definition, as well as the estimated time it will take to do so.

<table id="choicetable_hnp_vgx_2hc"><tbody><tr><td id="d59991e763">

**Estimated Time to Resolve Issue**

</td><td>

The estimated time for a single developer to resolve the definition finding in days, hours, minutes, and seconds.

</td></tr><tr><td id="d59991e775">

**Steps To Resolve**

</td><td>

A description of the steps for resolving the finding related to this definition. This description is displayed on real-time messages.

</td></tr></tbody>
</table>7.  Select **Save** in the Additional Actions drop down menu to save the new definition, then configure the Applicable Tables.


