---
title: Submit a complaint through the Anonymous Report Center portal
description: Submit a complaint anonymously through the Anonymous Report Center \(ARC\) portal to report a compliance violation incident for investigation and resolution.
locale: en-US
release: australia
product: Legal Investigations
classification: legal-investigations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Requests, Legal Investigations, Legal Service Delivery Practice Applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Submit a complaint through the Anonymous Report Center portal

Submit a complaint anonymously through the Anonymous Report Center \(ARC\) portal to report a compliance violation incident for investigation and resolution.

## Before you begin

To file a complaint anonymously, admins must have completed the following tasks:

-   Installed the Anonymous Reporting Center plugin \(com.sn\_anonymous\_report\_center\)
-   Enabled the Ethics Complaints record producer for submission through ARC portal.

    For more information, [Record producers for legal investigations](../reference/record-producers-legal-investigation.md).


Role required: sn\_lg\_ops.legal\_user

## Procedure

1.  Open the Anonymous Report Center portal either via Employee Center portal or using a direct URL.

<table id="choicetable_bkg_zx3_vfc"><thead><tr><th align="left" id="d365460e89">

Option

</th><th align="left" id="d365460e92">

Steps

</th></tr></thead><tbody><tr><td id="d365460e98">

**From Employee Center**

</td><td>

1.  Navigate to **All** &gt; **Self-Service** &gt; **Employee Center**.
2.  In the Employee Center portal, click the **Legal** menu and select the **Ethics and Compliance** option.
3.  In the Ethics and Compliance request category page, click **Anonymous Ethics Complaint**.


</td></tr><tr><td id="d365460e143">

**Using direct URL that does not require a log in**

</td><td>

Navigate to the Anonymous Report Center by accessing your instance URL and adding a /arc suffix. For example, https://example.com/arc

</td></tr><tr><td id="d365460e152">

**From Legal Service Portal**

</td><td>

1.  Navigate to **All** &gt; **Legal Request** &gt; **Legal Service Portal**.
2.  In the Legal Service Portal, click **Service Catalog** and select the **Ethics Requests** category.
3.  In the Ethics Requests category page, click **Anonymous Ethics Complaint**.


</td></tr></tbody>
</table>    If you are using Employee Center or Legal Service Portal, you are signed out of your account to keep your identity anonymous. The Anonymous Report Center portal opens in a new browser tab.

2.  In the Anonymous Report Center portal, click **Submit an Anonymous Report**.

3.  On the Submit an anonymous report page, click **Ethics Complaints**.

4.  On the Ethics Complaints form, fill in the fields.

    Based on the [active record producers for ARC](../reference/record-producers-legal-investigation.md), different sets of fields might appear on the Ethics Complaints form.

    For field descriptions, see [Ethics complaints intake form in the Anonymous Report Center portal](../reference/ethics-complaint-intake-form-arc.md).

5.  Enter the text verification code.

    **Note:** For the text verification code to work, you must install the HR Scoped Security plugin.

6.  Click **Submit**.

7.  To download and save the reported request on your system, in the Thank you for submitting your report dialog box, click **Download report copy**.

8.  Note the report key and report number from the respective fields to access your anonymous report in future to track its progress.


## Result

Either a legal request or a universal request is created based on the [active record producers for legal investigations](../reference/record-producers-legal-investigation.md).

To maintain the anonymity of the requester or requested for users, the request is submitted with the following values for the corresponding fields:

-   **Opened by** is populated as `Guest`.
-   **Requested for** is empty.

-   **[Access your anonymous report from the Anonymous Report Center portal](access-anonymous-complaint-arc.md)**  
You can follow up on your anonymous report to view comments and updates from the legal fulfiller working on it or add comments.

**Parent Topic:**[Submitting a complaint for investigation](../concept/submitting-legal-investigations-request.md)

**Related topics**  


[Submit a complaint through Legal Service Portal](submit-complaint-legal-svc-portal-1.md)

[Submit a complaint through Employee Center](submit-complaint-employee-center.md#)

