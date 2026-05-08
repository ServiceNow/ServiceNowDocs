---
title: Add restricted caller access privileges for accessing the legal request table
description: Create restricted caller access \(RCA\) privileges to ensure authorized access to the legal request table in the Now Assist for Legal Service Delivery \(LSD\) application.
locale: en-US
release: australia
product: Now Assist for Legal Service Delivery
classification: now-assist-for-legal-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configure agentic workflow, Configure, Now Assist for Legal Service Delivery \(LSD\), Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Add restricted caller access privileges for accessing the legal request table

Create restricted caller access \(RCA\) privileges to ensure authorized access to the legal request table in the Now Assist for Legal Service Delivery \(LSD\) application.

## Before you begin

Set the application scope to **Legal Request Management** in the application picker. For more information, see Application picker.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **Application Restricted Caller Access**.

2.  Create an RCA for a script include.

    1.  Select **New**.

    2.  On the form, fill in the fields.

<table id="table_j4f_qxm_y2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Source Scope

</td><td>

Scope of the calling application. Select **Now Assist AI Agents**.

</td></tr><tr><td>

Source Type

</td><td>

Type of record that is calling the application resource.Select **Script Include**.

</td></tr><tr><td>

Source Table

</td><td>

Table that contains the Source record.Select **Script Include \[sys\_script\_include\]**.

</td></tr><tr><td>

Source

</td><td>

Cross-scope record that is accessing a restricted application resource.-   Select Lookup Documents by using the list icon \(![Lookup Documents using list icon](../image/lookup-using-list.png)\).
-   In the field document, search and set the value as **Script Include: AiAgentRuntimeRequest**.


</td></tr><tr><td>

Status

</td><td>

Status of the access request. From the drop-down list, select **Allowed**.

</td></tr><tr><td>

Application

</td><td>

Application of the target resource. The field is automatically set to **Legal Request Management**.

</td></tr><tr><td>

Target Scope

</td><td>

Scope of the requested resource. Select **Legal Request Management**.

</td></tr><tr><td>

Target Type

</td><td>

Type of the requested resource. Select **Table: Legal Request**.

</td></tr><tr><td>

Operation

</td><td>

Operation that was performed on the target resource. Select **Read**.

</td></tr></tbody>
</table>    3.  Select **Submit**.

3.  Create an RCA for a short description.

    1.  Select **New**.

    2.  On the form, fill in the fields.

<table id="table_qt4_my3_cfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Source Scope

</td><td>

Scope of the calling application. Select **Global**.

</td></tr><tr><td>

Source Type

</td><td>

Type of record that is calling the application resource.Select **GlideScopedEvaluator**.

</td></tr><tr><td>

Source Table

</td><td>

Table that contains the Source record.Select **Value \[sys\_variable\_value\]**.

</td></tr><tr><td>

Source

</td><td>

Cross-scope record that is accessing a restricted application resource.-   Select Lookup Documents by using the list icon \(![Lookup Documents using list icon](../image/lookup-using-list.png)\).
-   In the field document, search and set the value as **58d70eff2bb0ea50099bfd2cce91bf1d**.


</td></tr><tr><td>

Status

</td><td>

Status of the access request. From the drop-down list, select **Allowed**.

</td></tr><tr><td>

Application

</td><td>

Application of the target resource. The field is automatically set to **Legal Request Management**.

</td></tr><tr><td>

Target Scope

</td><td>

Scope of the requested resource. Select **Legal Request Management**.

</td></tr><tr><td>

Target Type

</td><td>

Type of the requested resource. Select **Dictionary Entry: Short description**.

</td></tr><tr><td>

Operation

</td><td>

Operation that was performed on the target resource. Select **Read**.

</td></tr></tbody>
</table>    3.  Select **Submit**.

4.  Create an RCA for the description.

    1.  Select **New**.

    2.  On the form, fill in the fields.

<table id="table_kj4_2z3_cfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Source Scope

</td><td>

Scope of the calling application. Select **Global**.

</td></tr><tr><td>

Source Type

</td><td>

Type of record that is calling the application resource.Select **GlideScopedEvaluator**.

</td></tr><tr><td>

Source Table

</td><td>

Table that contains the Source record.Select **Value \[sys\_variable\_value\]**.

</td></tr><tr><td>

Source

</td><td>

Cross-scope record that is accessing a restricted application resource.-   Select Lookup Documents by using the list icon \(![Lookup Documents using list icon](../image/lookup-using-list.png)\).
-   In the field document, search and set the value as **58d70eff2bb0ea50099bfd2cce91bf1d**.


</td></tr><tr><td>

Status

</td><td>

Status of the access request. From the drop-down list, select **Allowed**.

</td></tr><tr><td>

Application

</td><td>

Application of the target resource. The field is automatically set to **Legal Request Management**.

</td></tr><tr><td>

Target Scope

</td><td>

Scope of the requested resource. Select **Legal Request Management**.

</td></tr><tr><td>

Target Type

</td><td>

Type of the requested resource. Select **Dictionary Entry: Description.**

</td></tr><tr><td>

Operation

</td><td>

Operation that was performed on the target resource. Select **Read**.

</td></tr></tbody>
</table>    3.  Select **Submit**.

5.  Create an RCA for a legal request.

    1.  Select **New**.

    2.  On the form, fill in the fields.

<table id="table_gsp_2z3_cfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Source Scope

</td><td>

Scope of the calling application. Select **Global**.

</td></tr><tr><td>

Source Type

</td><td>

Type of record that is calling the application resource.Select **GlideScopedEvaluator**.

</td></tr><tr><td>

Source Table

</td><td>

Table that contains the Source record.Select **Value \[sys\_variable\_value\]**.

</td></tr><tr><td>

Source

</td><td>

Cross-scope record that is accessing a restricted application resource.-   Select Lookup Documents by using the list icon \(![Lookup Documents using list icon](../image/lookup-using-list.png)\).
-   In the field document, search and set the value as **58d70eff2bb0ea50099bfd2cce91bf1d**.


</td></tr><tr><td>

Status

</td><td>

Status of the access request. From the drop-down list, select **Allowed**.

</td></tr><tr><td>

Application

</td><td>

Application of the target resource. The field is automatically set to **Legal Request Management**.

</td></tr><tr><td>

Target Scope

</td><td>

Scope of the requested resource. Select **Legal Request Management**.

</td></tr><tr><td>

Target Type

</td><td>

Type of the requested resource. Select **Table: Legal Request**

</td></tr><tr><td>

Operation

</td><td>

Operation that was performed on the target resource. Select **Read**.

</td></tr></tbody>
</table>    3.  Select **Submit**.

6.  Create an RCA for a category.

    1.  Select **New**.

    2.  On the form, fill in the fields.

<table id="table_pnf_5z3_cfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Source Scope

</td><td>

Scope of the calling application. Select **Global**.

</td></tr><tr><td>

Source Type

</td><td>

Type of record that is calling the application resource.Select **GlideScopedEvaluator**.

</td></tr><tr><td>

Source Table

</td><td>

Table that contains the Source record.Select **Value \[sys\_variable\_value\]**.

</td></tr><tr><td>

Source

</td><td>

Cross-scope record that is accessing a restricted application resource.-   Select Lookup Documents by using the list icon \(![Lookup Documents using list icon](../image/lookup-using-list.png)\).
-   In the field document, search and set the value as **58d70eff2bb0ea50099bfd2cce91bf1d**.


</td></tr><tr><td>

Status

</td><td>

Status of the access request. From the drop-down list, select **Allowed**.

</td></tr><tr><td>

Application

</td><td>

Application of the target resource. The field is automatically set to **Legal Request Management**.

</td></tr><tr><td>

Target Scope

</td><td>

Scope of the requested resource. Select **Legal Request Management**.

</td></tr><tr><td>

Target Type

</td><td>

Type of the requested resource. Select **Table: Category**.

</td></tr><tr><td>

Operation

</td><td>

Operation that was performed on the target resource. Select **Read**.

</td></tr></tbody>
</table>    3.  Select **Submit**.


